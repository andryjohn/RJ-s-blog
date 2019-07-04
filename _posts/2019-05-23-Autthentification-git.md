---
layout:     post
title:    (french) Marre des authentifications répètés à chaque push sur git?
date:       2019-05-21
summary:
categories: Developper skills
mathjax: true
---

>Bon, je me suis retrouvé dans une situation où je ne pouvais utiliser qu'une seule clé pour m'authentifier, et il faut taper son foutu mot de passe à chaque push, et à la longue sa en devenait pénible.

## Sa sent le *déja vue* ?

![mask](/images/push.jpg)


N'ayez crainte, après mainte recherche, bien caché au fin fond de son trou du c* * * , git à une solution spécifique à ce problème,  que je partage ici!


```git
git config credential.helper 'cache --timeout=3600'
```

Et votre authentification sera gardée en mémoire pour une heure. Vous pouvez faire :

```git
git config credential.helper 'cache --timeout=3600'
```

Pour l’étendre à tous les repos de votre machine. *"That's all folks!"*


  <footer><cite title="git">Credit: Andry RAJOHNSON</cite></footer>
