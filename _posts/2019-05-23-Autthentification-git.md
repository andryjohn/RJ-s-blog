---
layout:     post
title:      Marre des authentifications répètés à chaque push sur git?
date:       2019-05-21
summary:    
categories: Developper skills
mathjax: true
---

Bon, je me suis retrouvé dans une situation où je ne pouvais utiliser qu'une une clé pour m'authentifier, et il faut taper son  mot de passe à chaque push, et cela en devient pénible à la longue.

Sa sent le *déja vu* ?

--- 

![mask](/images/push.jpg)

---

>Après mainte recherche, bien caché au fin fond de son trou du c* * * , git à une solution spécifique à ce phoblème,  que je partage ici!


```git
git config credential.helper 'cache --timeout=3600'
```

Et votre authentification sera gardée en mémoire pour une heure. Vous pouvez faire :

```git
git config credential.helper 'cache --timeout=3600'
```

Pour l’étendre à tous les repos de votre machine. *That"s all folks!"*
---

  <footer><cite title="git">Credit: Andry RAJOHNSON</cite></footer>