---
layout:     post
title:      (French) Javascript From Zero to Hero
date:       2019-07-02
summary:
categories: Developper skills
mathjax: true
---
![javascript](/images/javascript.jpg)

# A qui s'adresse ce tutoriel?

Ce tutoriel est accessible à tous et pourra être bénéfique à chacun, que vous n'ayez jamais codé ou si vous ètes un expert, cela va vous permettre de révisé les bases.

Mon objectif  étant de dédiabolisé le code en vous présentant son  fonctionnement et les possibilités offertes par ce langage.

## Qu'est-ce ce que le JavaScript?

Le Javascript est un langage de programmation plutot jeune créé en 1995. Il va nous permettre de créer des pages interactives et « vivantes » à l’aide de **scripts.**

>Un **script**, c’est tout simplement une suite d’instructions qui vont être interprétées par un programme.

Ainsi, pour lire du code JavaScript, il va nous falloir un interpréteur. Heureusement, tous les navigateurs (Google Chrome, Safari, etc.) possèdent leur propre interpréteur JavaScript.

### Le JavaScript est un langage de programmation dit « client-side », c'est à dire que me code va s'effectuer du côté du client, c’est-à-dire sur l’ordinateur de la personne qui va demander la page web.


# Environnement de travail:

### Choisir et utiliser un éditeur de code:

Pour coder en JavaScript, les développeur on besoin d'un **éditeur de texte.** Moi j'utilise *Sublime text* mais il existe de nombreux éditeurs de texte sur le web et la majorité d’entre eux sont gratuits.
![sublime](/images/sublime.png)

Vous pourrez également trouver sur le web de nombreux sites web vous permettant d’écrire du code en JavaScript et d’avoir immédiatement un aperçu du résultat. Je vous recommande
[jsfiddle.net](https://jsfiddle.net/) ou [jsbin.com](https://jsbin.com/?html,output).

### Ou écrire notre code JavaScript?

On va pouvoir placer du code JavaScript à trois endroits différents :

* Dans l’élément `head` d’une page HTML ;
* Dans l’élément `body` d’une page HTML ;
* Dans un fichier portant l’extension « .js » séparé.

Bien que cette dernière méthode soit généralement recommandée, notamment pour des gros projets, parfois vous serez « obligé » d’écrire votre code JavaScript dans votre fichier HTML.

# Les variables en JavaScript:
![var](/images/var.png)

Une **variable JavaScript** est un conteneur servant à **stocker temporairement une information**, comme un nombre ou une chaîne de caractères (c’est-à-dire un texte) par exemple, ici c'est
**firstName**.

![var](/images/var2.png)


Comme son nom l’indique, le propre d’une *variable* est de pouvoir varier, c’est-à-dire de pouvoir stocker (tel une boite)
*différentes valeurs dans le temps, en « écrasant » sa valeur précédente.*

En JavaScript, on déclare une variable avec le mot clef « var » suivi du nom de notre variable. Chaque nouvelle variable doit avoir un nom unique qu’on appelle également en anglais « identifier ».

### Le nom des variables en JavaScript

On doit observer différentes règles lorsque l’on nomme une variable en JavaScript :

Le nom des variables doit commencer par une lettre ;
Le nom ne peut contenir que des lettres (non accentuées), des chiffres ou les signes « _ » et « $ » ;
Le nom des variables est sensible à la casse (« a » est différent de « A ») ;

Le JavaScript possède des mots « réservés » qu’on ne peut utiliser pour créer une variable. Nous verrons ces mots au fil de ce cours. Par exemple, le mot « var » est un mot réservé.

### Déclarer une variable en JavaScript

Il existe différentes façons de déclarer une variable en JavaScript. On va pouvoir :

* Déclarer une variable et lui assigner une valeur immédiatement ;
* Déclarer une variable sans lui assigner de valeur et lui assigner une valeur plus tard ;
* Déclarer plusieurs variables en même temps.

Voyons immédiatement un premier exemple ensemble :

```javascript

//On declare une variable et lui assigner une valeur immédiatement ;
var x = 45;
//On declare une variable sans lui assigner de valeur et lui assigner une valeur ensuite(non recommandée) ;
var age;
age = 25
// On crée une variable vide  à laquelle on affecte une valeur ar la suite (meilleur option)
var ville = "";
ville = "Paris"
// une variable stockant un type particulier: un booléan
var man = true;

```
**Remarque: les types de valeurs et le signe « = »**

La première concerne les valeurs stockées par *les variables.* Vous pouvez remarquer que selon le *type de valeur stockée*(texte, nombre ou booléen), nous allons déclarer nos variables de façon sensiblement différente (utilisation ou non de guillemets ou d’apostrophes). Nous allons y revenir..


La deuxième remarque concerne **le signe « = » (signe égal).**

Faites très attention à la signification de ce signe en JavaScript et en programmation en général, car ce n’est pas le égal mathématique que vous connaissez.

>En effet, en JavaScript, le signe égal est un opérateur d'affectation et non pas d’égalité.

Cela veut dire que ce signe va nous servir à
**affecter (ou assigner) une valeur à une variable, mais non pas que la variable est égale à sa valeur.**

Pour vous donner un exemple concret, en JavaScript, nous allons pouvoir faire cela (ce qui n’aurait aucun sens en mathématiques) :

```javascript
// On stock la valeur 15 a notre variable x
var x = 15;

/*On ajoute 5 à la dernière valeur connue stockée par x;
*x stocke donc maitenant la valeur 30*/
x = x + 5;

// En math, la reponse serait "l'ensemble des solution est nulles"
```
# Les types de valeurs des variables
![var](/images/Data.png)

Les variables en JavaScript peuvent stocker
*différents types de valeurs.*

Par simplification, on parlera **souvent (à tort) de « types de variables » au lieu de parler de « types de valeurs stockées par les variables ».**

### Le type de valeurs Numbers:
![var](/images/number.png)


