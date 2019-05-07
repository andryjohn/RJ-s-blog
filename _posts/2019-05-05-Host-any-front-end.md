---
layout:     post
title:      Host any Front End projects for free with github-pages
date:       2019-05-05
summary:   Work in the gh-pages branch of your git project, set up your own domain with a CNAME
categories: Developper skills
mathjax: true
---
![git](/images/github.gif)
Sometimes you want to work on a simple web page, and you don’t want the burden of having to setup some hosting environment.

Once again, [GitHub Pages](https://pages.github.com/) can help you. By creating a repo and working in the **gh-pages branch** instead of **master**, you will automatically get your site up and running.

Bonus point, you can set a **CNAME** to host it under your own domain.

Follow this gist, and do it all from the terminal!

```ruby
# Puts your own GitHub username? & your own project name?
GITHUB_USERNAME="andryjohn"
PROJECT_NAME="jekyllblog"

# We can create GitHub repo from the terminal, with https://github.com/github/hub
# It's really convinient. You can download it with:
brew install hub

# Say you want to work on a minesweep, create the repo:
mkdir -p ~/code/$GITHUB_USERNAME/$PROJECT_NAME && cd $_

# Initialize the git repo and change the branch to gh-pages right away
git init
git checkout -b gh-pages

# Create the GitHub repo. At first usage, it will prompt you for your credentials
hub create

# We will notify GitHub Pages that this is not a Jekyll repo
touch .nojekyll
echo "Hello world" > index.html
git add .
git commit -m "This is not a Jekyll repo"
git push -u origin gh-pages

# You can visualize the GitHub repo with:
hub browse

# Wait a few minutes, and you should see "Hello world" at:
open http://$GITHUB_USERNAME.github.io/$PROJECT_NAME

# Of course, you can set it to answer to a specific CNAME (Then it would drop the
# project name automatically after the slash)
echo "$PROJECT_NAME.rajohnson-andry.tk" > CNAME # Change with your own URL
git add CNAME
git commit -m "Adding CNAME"
git push origin gh-pages

# Now go to OVH / Gandi / or DOT.tk/ like me, if you want a free domain name , your DNS provider and record a CNAME from
# "$PROJECT_NAME" to "$GITHUB_USERNAME.github.io." (trailing dot is *SO* important)
```

You're welcome!

<footer><cite title="Workshop">Credit: Andry Rajohnson</cite></footer>