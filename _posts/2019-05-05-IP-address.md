---
layout:     post
title:   (French)Qu’est-ce qu’une adresse IP, et quelle difference entre IPv4 et IPv6 ?
date:   2019-05-14
summary:
categories: Developper skills
mathjax: true
---

![hacker](/images/Ip.jpg)

---

>Une adresse IP est l’adresse de l’ordinateur afin de s’identifier de manière unique sur internet.


## IPv4

On alloue à l’ordinateur une adresse unique de 32 bits. Pour la rendre plus facilement lisible pour un être humain, on la représente sous forme de 4 groupes de 8 bits.

---
```quote
a.b.c.d
```
---
Chacun des 4 groupes est de 8 bits.
 \\(2^{8}\\) donne 256 possibilités

Chacun des groupes peut donc prendre une valeur positive comprise entre [0, 255]

---
```quote
123.11.67.90
```
---

# Problème ?

Une adresse IP est 32 bits, ce qui donne \\(2^{32}\\) = 4 milliards de valeurs possibles. Mais on est 7,5 milliards sur Terre ! ( voyez par [vous-même!](https://www.worldometers.info/fr/population-mondiale/),c'est impréssionnant) et certaines personnes ont plusieurs machines. Du coup, on a déjà atteint notre limite d’adresses IP possibles.

![people](/images/people.jpeg)

>### Comment peut-on attribuer une adresse unique à tout le monde ?
La solution est de passer de IPv4 (avec une adresse de 32 bits) à …



## IPv6

l’IPv6 (adresse à 128 bits)

Voici une solution pour parer au problème d’attribution d’adresse IP aux différentes machines de la population.

---

```quotes
b:c:d:e:f:g:h:i
```

---

L’ensemble représente 128 bits: en se composant de 8 groupes.

Chacun des groupes est représenté par 1 à 4 nombres décimaux compris entre [0, ffff]

Voici donc à quoi peut ressembler une adresse IPv6


```quotes
2001:1236:12ab:0:0:0:1111:2222
```

---

Par convention, on peut omettre les zéros en doublant “::”, comme ceci


```quotes
2001:1236:12ab::1111:2222
```

---
