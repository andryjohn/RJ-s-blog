---
layout:     post
title:      Fixing Corrupt ZSH History
date:       2019-06-11
summary:
categories: Technique
---
![zshrc](/images/ohmy.png)
```zsh
zsh: corrupt history file /home/andry/.zsh_history
```

---

Few day ago, when I logged into my console, I saw following error message, so I decided to fix it, doing a quick search on google, I was able to reach a [stackoverflow link](https://superuser.com/questions/957913/how-to-fix-and-recover-a-corrupt-history-file-in-zsh/957924#957924) that recommended I run following set of commands
---

```zsh
mv .zsh_history .zsh_history_bad
strings .zsh_history_bad > .zsh_history
fc -R .zsh_history
```

---

I ran them and everything come back again. So I was searching again and found this solution, thanks to [Rishi Baldawa](https://twitter.com/rishibaldawa), ok let's hack!

## Rename:

---

```zsh
mv .zsh_history .zsh_history_bad
```
Well `mv` should be familiar to anyone who's toyed with linux. It moves files from one path to another. Also often used as a cheap was to rename files as we did here. More details on move in the [man page](https://linux.die.net/man/1/mv).

## Sanitize

---

```zsh
strings .zsh_history_bad > .zsh_history
```

`Strings` is interesting. I had not come upon it before. Based on the man page:

>... strings prints the printable character sequences that are at least 4 characters long (or the number given with the options below) and are followed by an unprintable character...


It seems `strings` is a nice way to actually get the printable characters in a file. In our case, this means if the `.zsh_history` was corrupted due to non-printable characters2, this will help parse them out. It also means if you ran any commands with non-printable characters, you've now lost them from your history as well. I'm very unlikely to run printable characters, so this wasn't as big of an issue but this may make past commands for QAs and pen-testers a tad-annoying.

## Parse

---

```zsh
fc -R .zsh_history
```

`fc` was interesting. It doesn't show up in the manpage. I ended up in a searching a fair amount to realize that this is a zsh-built in feature. There's some information about it within zsh documentation.

>...'`fc -R`’ reads the history from the given file

It seems fc will interact with your `zsh_history`. In this case, we are reading from the file and, since no second file was mentioned, putting it back into the same history file. i.e. re-writing history by parsing the same file.

## Cleanup

---

```zsh
rm .zsh_history_bad
```

This wasn't part of the original script but you should always clean-up after yourself. This command deletes the tmp "bad" file that you created in the first step.


# Conclusion

If I power shutdown my VM / linux box while `zsh` is still writing content, I can still corrupt the `zsh_history`. As long as I don't care about any other non-printable characters in the past and open to keep using zsh, I can run the above commands to get back to a happier stage.

<footer>Thanks to Rishibaldawa</footer>



