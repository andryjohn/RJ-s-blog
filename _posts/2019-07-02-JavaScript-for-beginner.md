---
layout:     post
title:      (French) JavaScript From Zero to Hero(Part I)
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

---
### Le type de valeurs Numbers:


![numbers](/images/numbers.png)

Le type de valeurs Number va représenter **tout nombre ou chiffre, qu’il soit positif, négatif, entier ou à virgule.**

*Pour affecter une valeur de type Number à une variable, on n’utilise ni guillemet ni apostrophe.*

### Le type de valeurs String:

Le type de valeurs **String** va représenter les chaînes de caractères, c’est-à-dire les textes.

Si l’on veut stocker *une chaîne de caractères dans une variable, il faut entourer notre chaîne par des apostrophes ou des guillemets.*

>Ce sont justement ces apostrophes ou guillemets qui vont indiquer au JavaScript que l’on stocke une valeur de type String.


```javascript

var firstName = "Andry";
var Name = "John";
var gender = "Male"

````
### Le type de valeurs Boolean

Une variable en JavaScript peut encore stocker une valer de type **Boolean**, *c’est-à-dire un booléen.*

![boolean](/images/boolean.png)

Une variable en JavaScript peut encore stocker une valer de type **Boolean**, *c’est-à-dire un booléen.*

Un booléen, en algèbre, est *une valeur binaire (soit 0, soit 1). En informatique, un booléen va être soit la valeur true (vrai), soit la valeur false (faux).*

>Faites bien attention : pour qu’une variable stocke bien un booléen, il faut lui faire stocker la valeur true ou false, sans guillemets ou apostrophes.

Si vous rajoutez des guillemets ou des apostrophes, la variables stockera alors la chaîne de caractères **true ou la chaîne de caractères false.**

```javascript

// a et b sctockent un valeur de type boolean
var a = true, b = false

//c stocke la chaine de caractère true//
var c = "true"

```

### Autres valeurs stockées en JavaScript

Les variables en JavaScript peuvent stocker bien d’autres valeurs n'étant pas de type *String, Number ou Boolean.*

![null](/images/null.png)

Parmi les autres valeurs remarquables, on peut citer la valeur *«null»*, qui correspond **à la non connaissance à priori de la valeur ainsi que la valeur *«undefined»* qui correspond au fait de ne pas avoir défini de valeur pour notre variable.**

Une variable peut encore contenir la valeur « NaN » qui signifie « Not a Number » (« n’est pas un nombre » en Français).

### Tester le type de valeur d’une variable

Pour tester le type de la valeur que contient une variable, on utilise généralement la fonction
`typeof()`. Nous étudierons les fonctions en détail plus tard dans ce cours.

>Attention cependant, cette fonction renvoie parfois des résultats contestables sur certaines valeurs.

Voyons immédiatement un exemple d’utilisation de
`typeof()` ensemble. Pour afficher le résultat de
`typeof(`, nous allons l’utiliser avec une instruction `alert()`.

Le script ci-dessous affichera tous les résultats au sein d’une même instruction `alert()`. Pour faire cela, j’utilise ce qu’on appelle la concaténation (avec les « + ») et la notation `\n` qui sert à créer un retour à la ligne en JavaScript.

```javascript

 var text = "Bonjour", x = 4, b = true, n = null, u, nn = NaN;

        alert("Variable texte : " + typeof(texte) +
              "\nVariable x : " + typeof(x) +
              "\nVariable b : " + typeof(b) +
              "\nVariable n : " + typeof(n) +
              "\nVariable u : " + typeof(u) +
              "\nVariable nn : " + typeof(nn));

````

![type](/images/type.png)

Sans surprise, notre variable `texte` est bien de type String, tandis que nos variables `x` et `b`sont respectivement de type Number et Boolean.

Le résultat renvoyé par `typeof()` est undefined pour notre variable `u` puisqu’on ne l’a pas définie.

En revanche, vous remarquez que le résultat renvoyé pour notre variable `nn` est Number, ce qui est très étrange sachant qu’on lui a justement donné la valeur « Not a Number ».

Enfin, notez également que `typeof()` renvoie Object pour notre variable `n` qui contient la valeur `null`. Ce résultat fait également débat.


# OPERATIONS SUR LES VARIABLES EN JAVASCRIPT

Pour des variables stockant des valeurs de type Number, on va donc pouvoir effectuer les mêmes opérations qu’avec des nombres en mathématiques.

Ainsi, nous allons pouvoir additionner (les valeurs de) deux variables entre elles, les soustraire l’une à l’autre, les multiplier entre elles, etc.

```javascript
var x = 5, y = 18, z = -2;

//on ajoute 1 à la valeur de c qui stocke maitenant 6
x = x + 1;

//On soustrait 4 a x, x vaut maitenant 2
x = x - 4;

y = y * 2 //y contient maintenant 20

/*On multiplie la derniere valeur contenu dan x (4) par la dernière
* valeur contenu dans y (20). On stocke le resultat (80) dans une
*nouvelle variable q'on appelera mult*/

var mult = x * y;

/* On divise la derniere valeur contenue dans y par celle contenu dans z
*On stocke le résultat (20/(-2) = -18) dans une varilable divi */
var div = y / z;

/* le modulo represente le reste de ka division entière d'une nombre par autre
*Par exemple, si on divise 13 par 3 et qu'on ne conserve que la partie entière ,
*le résultat est 4 et il reste 1. 1 est le modulo.*/
var mod = 13 % 3;

```
**Le modulo correspond au reste de la division entière d’un nombre par un autre. On utilise le signe « % » pour le calculer.**

### Priorité de calcul

Faites attention à respecter les priorités de calcul lorsque vous effectuez des opérations sur les variables.

En réalité, c’est très simple puisque ce sont les mêmes qu’en mathématiques : *les parenthèses sont prioritaires sur toute autre opération, puis viennent la multiplication, la division et le modulo et finalement l’addition et la soustraction.*

```javascript
var x = 5, y = 10, z = -2;

// Les priorité de calcul sont les memes qu'ne math
var prior = x + y / ( 4 + z ) % 3;

alert(prior);

```
![prior](/images/prior.png)


Ici, on commence par calculer ce qui est *entre parenthèses*, c’est-à-dire `4 + z` ce qui nous donne `4 + (-2) = 2.`

Ensuite, on divise donc la valeur contenue dans y par 2 ce qui nous donne 5 et on calcule le modulo de 5 par 3 qui est égal à 2.

Finalement, on additionne la valeur contenue dans x et 2 pour arriver au résultat final : `7`.

Faites donc bien attention aux priorités de calcul lorsque vous effectuez des manipulations sur les variables, car le résultat peut s’avérer totalement différent de celui attendu si vous n’en tenez pas compte.


### Opérations simplifiées sur les variables JavaScript

Sachez que l’on peut simplifier l’écriture de *certaines opérations mathématiques sur les variables en JavaScript*, afin de **gagner en temps, en performance et en clarté.**

```javascript
var x = 5, y = , z = -2;
//Equivaut à "x = x + 2", x = x - 3

x += 2;
X -= 3;
// VOUS AVEZ COMPRIS !
x *= 3;
y %= x;
...
```
La suite dans la deuxième partie, si vous ètes arrivé jusque là, bravo!

Dans la deuxième partie, nous allons voir:

* La concaténation
* Présentation des conditions
* Les conditions if, if...else, if...else if...else
* Opérateurs logiques
* Evaluation / Simplification des conditions
* Conditions ternaires
* Switch
* Les boucles
* Découverte des fonctions

## Un excellent "workshop Le Wagon" pour revoir les concepts vus sur ce tutorial!

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/cQZOfeKrWDs' frameborder='0' allowfullscreen></iframe></div>


<footer><cite title="Workshop">Credit: Andry Rajohnson, Fullstack Developer</cite></footer>
