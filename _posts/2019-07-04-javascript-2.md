---
layout:     post
title:      (Fr) JavaScript From Zero to Hero (Part II)
date:       2019-07-04
summary:
categories: Developper skills
mathjax: true
---
![javascript](/images/javascript.jpg)
>Dans cette deuxième partie nous allons voir: **La concaténation, la présentation des conditions,les conditions if, if…else, if…else if…else, les opérateurs logiques,l'évaluation / Simplification des conditions,les boucles.**

##  La concaténation : définition et exemples

Concaténer signifie tout simplement *mettre bout à bout deux chaînes de caractères afin d’en former une troisième, nouvelle.*


>Concaténer, c’est donc « additionner » des chaînes de caractères et en JavaScript, on va pouvoir concaténer grâce à l’opérateur « + ».

Evidemment, nous allons pouvoir appliquer cet opérateur directement à nos variables afin de concaténer leurs contenus respectifs.

```javascript
//La variable espace stocke... un espace
        var lastName = 'John', space = ' ', firstName = 'Lennon';

        /*On peut concaténer et stocker le résultat dans
         *une nouvelle variable*/
        var me = lastName + space + firstName;

        //On peut également concaténer des valeurs entre elles
        var you = 'Karl' + ' ' + 'Marx';

        //On peut encore concaténer des variables et des valeurs;
        var sport = 'crossfit';
        var hobbie = "I love " + sport;

        /*On utilise également la concaténation pour tout afficher
         *au sein d'une même instruciton alert :*/
        alert("Variable me : " + me +
              "\nVariable you : " + you +
              "\nVariable hobbie : " + hobbie);
````

![alert](/images/concatenation.png)

### Qu'avons-nous fait ici ?

* Nous avons utilisé la concaténation pour « additionner » les valeurs contenues dans `lastName`, `space` et dans `name`. Nous avons ensuite stocké le résultat de cette concaténation dans une nouvelle variable `me`.
* Ensuite, nous avons fait de même avec la variable `me` en concaténant cette fois-ci non plus des variables, mais directement des valeurs entre elles.
* Finalement, nous avons concaténé une variable avec une valeur.

>A noter évidemment qu’on **ne concatène jamais véritablement des variables (c’est un abus de langage), mais seulement les valeurs contenues dans ces variables.**

* Et enfin, nous avons utilisé la concaténation pour afficher le contenu de toutes nos variables d’un coup au sein d’un même `alert()`.

>La seule chose à laquelle vous devez faire attention ici est **l’utilisation des apostrophes / guillemets : on ne s’en sert que pour entourer les chaînes de caractères, et non pas pour les variables.**

## Additionner un nombre et une chaîne de caractères

Si l’on tente « d’additionner » un nombre et une chaîne de caractères, *tout ce qu’il y a derrière la chaîne de caractères sera également considéré comme une chaine de caractères par le JavaScript.*

```javascript
            var x = 4 + 2 + "1";
            var y = "1" + 2 + 4;
            var z = 2 + "un" + 4;

            alert("Variable x : " + x +
                  "\nVariable y : " + y +
                  "\nVariable z : " + z);

````
![alert](/images/concatenation2.png)

* Ici, pour notre variable `x`, le JavaScript va commencer par additionner `2 et 4` naturellement, puis va ajouter la chaîne de caractères « 1 » au résultat (c’est-à-dire à 6). Cela donne donc le résultat « 61 ».

* Dans le second cas, le JavaScript va considérer tout ce qui se trouve derrière la chaîne de caractères « 1 » comme une chaîne de caractères, et va donc concaténer 1, 2 et 4 pour donner « 124 ».

On peut également observer plus clairement cela avec notre troisième variable `z`, qui va stocker « 2un4 ».

## Découverte des conditions en JavaScript
En JavaScript, nous allons souvent vouloir effectuer différentes actions selon la valeur d’un paramètre, afin de dynamiser notre site et d’y ajouter une certaine interaction.

>*Par exemple, on va vouloir afficher le message « Bonjour » si il est moins de 18h ou « Bonsoir » dans le cas contraire, ou encore afficher le message « Bonjour john » si votre visiteur à indiqué au préalable qu’il s’appelait John.*

Une façon simple de faire cela est d’utiliser les conditions.

Les conditions vont s’articuler autour d’un **test**. Généralement, nous allons comparer la valeur contenue dans une variable à une certaine autre valeur.

Selon le résultat du test, nous allons ensuite pouvoir exécuter un bloc de code plutôt qu’un autre à l’intérieur de notre condition.

Pour effectuer des comparaisons à l’intérieur d’une condition, nous allons avoir besoin d’opérateurs de comparaison qui sont les suivants:

### Symbole Signification

```quote
==  Est égal à (en valeur)
!=  Est différent de (en valeur)
=== Est égal à (en valeur et en type)
!== Est différent de (en valeur ou en type)
< Est strictement inférieur à
<=  Est inférieur ou égal à
> Est strictement supérieur à
>=  Est supérieur ou égal à
````
>Commencez par noter que pour tester l’égalité, on n’utilise pas le signe « = » qui, rappelons le, est un opérateur d’affectation et non d’égalité au sens mathématique du terme, mais le double égal (==).

Ensuite, deux symbole peuvent vous poser problème : *le triple égal et le point d’exclamation suivi de deux signes égal.*

En utilisant seulement le double égal, nous n’allons tester que l’égalité sur la valeur. Ainsi, si l’on tente de comparer le chiffre 4 à la chaîne de caractères « 4 » de cette manière, le JavaScript renverra le booléen « true » (vrai).

>En revanche, si l’on utilise le triple égal, on va tester à la fois l’égalité sur les valeurs et sur le type de valeurs. Ainsi, si l’on compare le chiffre 4 à la chaîne de caractère « 4 », le JavaScript renverra « false » (faux).

## Le JavaScript et les comparaisons de valeurs

Afin de bien comprendre comment fonctionnent les conditions, il est **indispensable** au préalable que vous compreniez comment le JavaScript effectue des comparaisons entre les valeurs.

Sans cette connaissance, il est impossible de savoir comment *une condition marche véritablement.*

Tout d’abord, vous devez bien comprendre que le JavaScript sait comparer différentes valeurs entre elles.

A chaque fois que l’on va comparer deux valeurs, le JavaScript va renvoyer *un booléen*, c’est-à-dire soit « true », soit « false », selon que la comparaison soit vraie ou pas.

Par exemple, si l’on écrit en JavaScript « 7 < 14 », le JavaScript renverra « true » car 7 est bien inférieur à 14.

>Dans nos conditions, nous n’allons donc pas directement tester si une valeur est **inférieure**, égale ou **supérieure** à une autre, mais tester si le JavaScript nous renvoie *true* ou *false*.

**C’est une distinction très importante que malheureusement très peu de développeurs font ou comprennent.**

Voyons immédiatement plusieurs exemples afin d’être sûrs de bien comprendre comment tout cela fonctionne :

```javascript

 /*Rappelez vous que le égal simple (=) n'est qu'un opérateur
*d'assignation; il sert à stocker une valeur dans une variable*/
     var x = 7, y = 14;

          /*Le JavaScript va analyser "7 < 14" et renvoyer true.
     *Notre variable vrai va donc stocker true*/
    var vrai = x < y;

       /* 14 n'est pas inférieur ou égal à 7. JavaScript
           * renvoie donc false*/
    var faux = 14 <= 7;

     /*On ne compare que les valeurs; JavaScript renvoie true
      *si elles sont égales, false sinon*/
     var egalval = 4 == "4";

     /*On compare valeurs et type; JavaScript renvoie true en
      *cas d'égalité sur les valeurs et les types, false sinon*/
     var egalvaltype = 4 === "4";

     /*On compare les valeurs uniquement. JavaScript renvoie
      *true si elles sont différentes, false sinon*/
     var difval = 4 != "4";

       /*On compare valeurs ou types. Si les valeurs ou les types
           *différent, JavaScript rnevoie true*/
      var difvaltype = 4 !== "4";

            alert("vrai stocke : " + vrai +
                  "\nfaux stocke : " + faux +
                  "\negalval stocke : " + egalval +
                  "\negalvaltype stocke : " + egalvaltype +
                  "\ndifval stocke : " + difval +
                  "\ndifvaltype stocke : " + difvaltype);

````
![compar](/images/comparateur.png)


Dans le code ci-dessus, nous comparons des valeurs entre elles. A la suite de chaque comparaison, le JavaScript renvoie soit true soit false selon que la comparaison soit vraie ou non.

On stocke le résultat renvoyé par le JavaScript dans une variable pour chaque comparaison puis on affiche tout cela grâce à une instruction `alert()`.

Maintenant que vous savez véritablement comment fonctionne le JavaScript avec les opérateurs de comparaisons, nous allons pouvoir aborder sereinement les conditions en soi.

---

## La condition if
« If » en anglais signifie « si ». Avec cette première structure conditionnelle, on va pouvoir tester si une valeur répond à un certain critère, et exécuter un bloc de code le cas échéant.

Par exemple, on peut choisir d’afficher le message « Bonjour » si une variable
`hour` stocke une valeur inférieure à 18.

```javascript
 /*On commence par définir une variable heure.
             *Plus tard, nous utiliserons les fonctions pour
             *toujours avoir l'heure exacte*/
            var hour = 15;

            //On écrit notre première condition if
            if (hour <= 18 == true) {
                alert("Bonjour");
            }

```
![bonjour](/images/bonjour.png)

Dans le cas où le JavaScript renvoie false, rien ne se passe.

```javascript
 /*On commence par définir une variable heure.
             *Plus tard, nous utiliserons les fonctions pour
             *toujours avoir l'heure exacte*/
            var hour = 21;

            //On écrit notre première condition if
            if (hour <= 18 == true) {
                alert("Bonjour");
            }
                    //Rien ne s'affiche!
```
>Dans la pratique, on comparera souvent la valeur renvoyée par le JavaScript à l'issue de la comparaison à la valeur true. Cependant, on peut également évidemment comparer cette valeur à false et exécuter notre bloc de code le cas échéant.

```javascript

            var hour = 21;

            //On écrit notre première condition if
            if (hour <= 18 == false) {
                alert("Bonsoir");
            }

```

![bonsoir](/images/Bonsoir.png)

## La condition if…else

La condition `if…else` (« si… sinon » en Français) va nous permettre d’exécuter un bloc de code si le JavaScript renvoie bien la valeur attendue, et un autre bloc de code s’il ne renvoie pas la valeur attendue.

En reprenant notre exemple précédent, on va donc pouvoir dorénavant afficher « Bonjour » si notre variable contient bien une valeur inférieure à 18 et « Bonsoir » dans le cas contraire.

```javascript
  var hour = 21;

            if (hour <= 18 == true) {
                alert("Bonjour");
            }
            else {
                alert("Bonsoir");
            }
```
![bonsoir](/images/Bonsoir.png)

>Notez dès à présent qu’on n’effectue jamais aucun test au sein du `else`, car le `else` va tout simplement prendre en charge tous les cas non supportés par le `if`.

## La condition if…else if…else

La condition `if…else if…else` signifie « si… sinon si… sinon » en Français.

>Cette condition va être très puissante et très pratique puisqu’elle va nous permettre de gérer autant de cas que l’on souhaite et d’exécuter un code différent pour chaque nouveau cas créé.

**On va pouvoir insérer autant de `else if` que l’on veut au sein de notre condition pour pouvoir gérer un nombre infini de cas.**

```javascript
        var hour = 9;

        if (hour < 12 == true) {
          alert("c'est le matin!");
        }
        else if (hour == 12 == true) {
          alert("il est midi!");
        }
        else if (hour <= 18 == true) {
          alert("c'est l'après midi!")
        }
        else {
          alert("cest le soir");
        }

```
![matin](/images/matin.png)

## Limitations et solutions

Cependant, ce code est encore *loin d’être parfait*. Les plus malins d’entre vous se demandent peut être *comment le JavaScript fait pour savoir si « c’est le matin » ou « c’est l’après midi » lorsque notre variable stocke une valeur inférieure à 12 ?*

La réponse est simple : il ne le sait pas.

>**Le code JavaScript va simplement être lu de façon linéaire et dès qu’un test va être évalué à true, nous allons sortir de la condition.**

Si nous avions construit notre condition différemment, le JavaScript aurait renvoyé le « mauvais » message.

```javascript
        var hour = 9;

        /*if (hour < 12 == true) {
          alert("c'est le matin!");
        }*/
        if (hour <= 18 == true) {
          alert("c'est l'après midi!");
        }

        else if (hour == 12 == true) {
          alert("il est midi!");
        }

        else if (hour <= 18 == true) {
          alert("c'est l'après midi!")
        }
        else {
          alert("cest le soir");
        }

```
![après-midi](/images/amidi.png)

Nous allons pouvoir régler ce premier défaut grâce aux opérateurs logiques, objet du prochain chapitre.


## Operateurs logiques et conditions:

### Les opérateurs logiques

En JavaScript, il existe trois opérateurs logiques très utilisés : l’opérateur logique « ET », l’opérateur logique « OU » et l’opérateur logique « CONTRAIRE » ou « NON ».

```quote

Opérateur logique    Symbole
ET (AND)              &&
OU (OR)               ||
NON                    !

```
### Opérateurs logiques et conditions

Nous allons pouvoir utiliser ces**opérateurs logiques au sein même de nos conditions**, afin de pouvoir par exemple effectuer plusieurs comparaisons au sein d’un même test.

* Plus précisément, l’opérateur logique « ET » va nous permettre de créer *un intervalle de comparaison pour une variable.*

On va par exemple pouvoir tester si la valeur contenue dans une variable
`hour` est comprise entre `0 et 12`.

>Grâce à cet opérateur, nous allons pouvoir lever l’ambiguïté sur certaines valeurs (ambiguïté vue dans la partie précédente) en ne travaillant plus qu’avec des intervalles.

```javascript

    var hour = 9;

     if (hour >= 0 && hour < 12 == true){
      alert("c'est le matin")
     }
     else if (hour === 12 == true) {
       alert("il est midi pile!")

     }
     else if (hour > 12 && hour <= 24 == true) {
       alert ("c'est le soir!")
     }
     else {
       alert("la valeur n'est pas valide..")
     }

```

![matin](/images/matin.png)

* L’opérateur « OU » va nous permettre de *comparer la valeur d’une variable à deux valeurs différentes.* Si l’une des deux comparaisons affiche le résultat attendu, *le reste du code sera exécuté.*

On peut par exemple tester si la valeur contenue dans une variable `hour` est
`inférieure à 0 ou supérieure à 24`.

```javascript
    var hour = 26;
    if (hour < 0 || hour > 24 == true) {
       alert("L'heure est invalide !")
    }
    else {
      alert("l'heure semble valide")
    }

```

![invalide](/images/invalide.png)

* Finalement, l’opérateur logique « NON » va nous permettre de nier une comparaison. Ainsi, des comparaisons évaluées de base à false vont être évaluées à true et inversement.

```javascript
  var hour = 18;

   /* l'opérateur logique "!" inverse la valeur logique
     d'un test. Ici, cela correspond à écrire :
     if(hour > 16 == true)*/
    if (!(hour <= 16) == true) {
      alert("il est plus dde 16h!")
    }
    else {
      alert("Il est moin de 16h!")
    }

```
![16h](/images/16h.png)

>Il est possible que vous ne compreniez pas immédiatement l’utilité de ces opérateurs logiques, notamment en ce qui concerne l’opérateur logique « NON ».
retenez juste que chacun d’entre eux est très puissant et ils vont tous nous être très utiles par la suite.

## Simplifier ses conditions

La façon dont nous avons écrit nos conditions jusqu’à présent est tout à fait valide. Cependant, nous allons pouvoir simplifier cette écriture.

En effet, vous devez savoir que lorsqu’on écrit une condition, le JavaScript va par défaut exécuter le code contenu dans un `if` ou dans un `else if` si la comparaison a été évaluée à `true`.

En d’autres termes, il est inutile de préciser le `== true` dans nos conditions.

```javascript
   var hour = 18;

  //Avant on écrivait :
  if ( hour > 12 == true){
    alert("Il est midi passé!");
  }
  //En simplifiant, ce code équivaut à:
  if (hour > 12) {
    alert("Il est midi passé!");
  }

```
 **A partir de maintenant, je vous encourage fortement pour des raisons de simplicité et de lisibilité à écrire vos conditions de façon abrégée.**


Pour évaluer de cette manière si une comparaison est évaluée à
`false`, nous allons avoir besoin de l’opérateur logique « NON » qui, rappelons le, va inverser la valeur logique d’un test, ce qui donne :

```javascript
   var hour = 18;

   //Avant on écrivait:
   if (hour < 12 == false) {
     alert("Il est midi passé!");
   }
   //Ce code équivaut à:
   if(!(hour < 12)) {
    alert("il est midi passé!")
   }
```

## L’évaluation des valeurs

Il y a un autre point que vous devez connaître afin de véritablement comprendre les conditions : *une valeur peut être évaluée à true ou false même sans opérateur de comparaison.*

Ainsi, toute valeur différente de `null`, `undefined`, `NaN`, `0` et `la chaîne de caractères vide` sera évaluée par défaut par le JavaScript à `true`.

Savoir cela nous permet de comprendre bien des choses et de résoudre certaines situations en JavaScript.

```javascript
var x = 6, y = "";

            //Correspond à if(x == true)
            if (x) {
                alert("x est évaluée à true par le JavaScript");
            }

            if (y){
                alert("y est évaluée à true")
            }
            else{
                alert("y est évaluée à false");
            }

```
![true](/images/true.png)

---

![false](/images/false.png)

Dans le code ci-dessus, la variable `x` contient la valeur `6`. Le code `if(x)` demande à JavaScript de comparer la valeur de `x` à `true` par défaut.

* Si la valeur de `x` a été évaluée à `true`, alors *une boîte d'alerte apparaitra*. Cela va être le cas d'après ce que nous avons dit précédemment.

* En revanche, notre variable `y` contient *une chaîne de caractères vide*. La chaine de caractères vide est par défaut évaluée à `false` par le JavaScript.

* Ainsi, nous allons entrer dans le `else` de notre deuxième condition et exécuter le code qui se trouve à l'intérieur.

## Les boucles en Javascript:

### Présentation des boucles

Les boucles vont nous permettre *d’exécuter un bloc de code un certain nombre de fois, tant qu’une certaine condition est remplie.*

>Par exemple, on va pouvoir exécuter une certaine instruction tant qu’une certaine variable n’aura pas atteint telle ou telle valeur.

**Attention cependant : la condition donnée doit toujours être fausse à un moment donné, sinon la boucle ne s’arrêtera jamais !**

Nous allons étudier trois boucles dans cette partie :

* La boucle `while` (« tant que ») ;
* La boucle `do… while` (« faire… tant que ») ;
* La boucle `for` (« pour »).

#### La boucle "while"

La boucle `while` va nous permettre de répéter une série d’instructions tant qu’une condition donnée est vraie.

```javascript

   //On commence par initialisé un variable

   var count = 0;

   //Tant que...
   while (count < 10){
    //On affiche la valeur de 'count'
    alert('count contient la valeur : ' + count);
   }
    //Et on incrémente cette valeur
                count++; //Equivaut à x = x + 1 ou x += 1

          //Tester le chez vous!!
```
![while](/images/while.png)

* Dans le code ci-dessus, on commence par initialiser une variable
`count` en lui faisant stocker la valeur `0`.

* Ensuite, on crée notre boucle `while`. Tant que `count` contient une valeur `strictement inférieure à 10`, on ne sort pas de la boucle et on retourne au début de celle-ci pour effectuer un nouveau passage.

* A chaque nouveau passage dans la boucle, on demande à afficher la valeur de `count` et on *incrémente* la valeur de `count`, c’est-à-dire on ajoute `1` à cette valeur.

>Comme vous pouvez le voir, pour incrémenter, il suffit d’ajouter deux signes « + » après notre variable.

### La boucle "do… while"

Pour faire très simple, la différence entre la boucle `do… while` et la boucle
`while` va être de même type que ce que nous venons de voir avec l’incrémentation : *cela va être une question d'ordre des opérations.*

>Dans une boucle while, si la condition donnée est fausse dès le départ, la boucle ne sera jamais exécutée.


```javascript

  var count = 100;
         do {
          alert ("count contient la valeur : " + count);
          }
          while (count < 10)
```
![dowhile](/images/dowhile.png)

### La boucle for

La boucle `for` (« pour ») va nous permettre de *répéter une série d’instructions à partir d’une valeur donnée, jusqu’à une certaine valeur seuil.*

>Cette boucle utilise une syntaxe assez condensée qui fait qu’elle est la plus utilisée en JavaScript car elle est la plus simple à écrire, la plus performante et au final la plus lisible.

Dans une boucle `for`, nous allons tout d’abord devoir initialiser une variable, puis poser notre condition, et finalement incrémenter ou décrémenter notre variable.

```javascript
  var i;

            /*i = 0 est appelée phase d'initialisation
             *i < 10 correspond à la condition
             *i++ est la phase d'incrémentation*/

            for(i = 0; i < 10; i++){
                alert ('i contient la valeur : ' + i);
            }

            /*Note : l'incrémentation se fait APRES le passage dans
             *la boucle. Ainsi, i contient 0 lors du premier passage*/
```
* Notez que l’on sépare les différentes phases ou déclarations à l’intérieur de notre boucle `for` par des points virgules.

* Retenez aussi que l’initialisation est exécutée avant tout passage dans la boucle `for`, tandis que l’incrémentation est exécutée à la fin de chaque passage dans la boucle `for`.

* Finalement, notez également que vous n’êtes obligé ni d’initialiser, ni d’écrire la condition, ni d’incrémenter à l’intérieur de la boucle `for`.

## Un excellent "workshop Le Wagon" pour revoir les concepts vus sur ce tutorial!

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/cQZOfeKrWDs' frameborder='0' allowfullscreen></iframe></div>
