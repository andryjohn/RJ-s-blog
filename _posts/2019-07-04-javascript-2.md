---
layout:     post
title:      (Fr) JavaScript From Zero to Hero (Part II)
date:       2019-07-04
summary:
categories: Developper skills
mathjax: true
---
![javascript](/images/javascript.jpg)
>Ce tutoriel est accessible à tous et pourra être bénéfique à chacun, que vous n'ayez jamais codé ou si vous ètes un expert, cela va vous permettre de révisé les bases.

##  La concaténation : définition et exemples

Concaténer signifie tout simplement mettre bout à bout deux chaînes de caractères afin d’en former une troisième, nouvelle.


Concaténer, c’est donc « additionner » des chaînes de caractères.

En JavaScript, on va pouvoir concaténer grâce à l’opérateur « + ».

Evidemment, nous allons pouvoir appliquer cet opérateur directement à nos variables afin de concaténer leurs contenus respectifs.

```javascript
//La variable espace stocke... un espace
        var lastName = 'Lennon', space = ' ', firstName = 'John';

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

Ici, nous avons utilisé la concaténation pour « additionner » les valeurs contenues dans `lastName`, `space` et dans `name`. Nous avons ensuite stocké le résultat de cette concaténation dans une nouvelle variable `me`.

Ensuite, nous avons fait de même avec la variable toi en concaténant cette fois-ci non plus des variables, mais directement des valeurs entre elles.

Finalement, nous avons concaténé une variable avec une valeur. A noter évidemment qu’on ne concatène jamais véritablement des variables (c’est un abus de langage), mais seulement les valeurs contenues dans ces variables.

Finalement, nous avons utilisé la concaténation pour afficher le contenu de toutes nos variables d’un coup au sein d’un même alert().

>La seule chose à laquelle vous devez faire attention ici est l’utilisation des apostrophes / guillemets : on ne s’en sert que pour entourer les chaînes de caractères, et non pas pour les variables.

## Additionner un nombre et une chaîne de caractères

Si l’on tente « d’additionner » un nombre et une chaîne de caractères, tout ce qu’il y a derrière la chaîne de caractères sera également considéré comme une chaine de caractères par le JavaScript.

```javascript
            var x = 4 + 2 + "1";
            var y = "1" + 2 + 4;
            var z = 2 + "un" + 4;

            alert("Variable x : " + x +
                  "\nVariable y : " + y +
                  "\nVariable z : " + z);

````
![alert](/images/concatenation2.png)

Ici, pour notre variable `x`, le JavaScript va commencer par additionner 2 et 4 naturellement, puis va ajouter la chaîne de caractères « 1 » au résultat (c’est-à-dire à 6). Cela donne donc le résultat « 61 ».

Dans le second cas, le JavaScript va considérer tout ce qui se trouve derrière la chaîne de caractères « 1 » comme une chaîne de caractères, et va donc concaténer 1, 2 et 4 pour donner « 124 ».

On peut également observer plus clairement cela avec notre troisième variable `z`, qui va stocker « 2un4 ».

## Découverte des conditions en JavaScript
En JavaScript, nous allons souvent vouloir effectuer différentes actions selon la valeur d’un paramètre, afin de dynamiser notre site et d’y ajouter une certaine interaction.

*Par exemple, on va vouloir afficher le message « Bonjour » si il est moins de 18h ou « Bonsoir » dans le cas contraire, ou encore afficher le message « Bonjour john » si votre visiteur à indiqué au préalable qu’il s’appelait John.*

Une façon simple de faire cela est d’utiliser les conditions.

Les conditions vont s’articuler autour d’un test. Généralement, nous allons comparer la valeur contenue dans une variable à une certaine autre valeur.

Selon le résultat du test, nous allons ensuite pouvoir exécuter un bloc de code plutôt qu’un autre à l’intérieur de notre condition.

Les opérateurs de comparaison
Pour effectuer des comparaiosns à l’intérieur d’une condition, nous allons avoir besoin d’opérateurs de comparaison.

Ces opérateurs sont représentés par les symboles suivants :

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

Dans nos conditions, nous n’allons donc pas directement tester si une valeur est *inférieure*, égale ou *supérieure* à une autre, mais tester si le JavaScript nous renvoie *true* ou *false*.

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



## Un excellent "workshop Le Wagon" pour revoir les concepts vus sur ce tutorial!

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed/cQZOfeKrWDs' frameborder='0' allowfullscreen></iframe></div>
