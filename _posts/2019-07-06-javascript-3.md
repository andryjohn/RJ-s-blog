---
layout:     post
title:      (Fr) JavaScript From Zero to Hero (Part III)
date:       2019-07-04
summary:
categories: Developper skills
mathjax: true
---
![javascript](/images/javascript.jpg)
>Le *JavaScript* a été construit autour du concept d’objets, tout est "quasiment" avant tout objet :
* Les chaînes de caractères, nombres et booléens peuvent être des objets (ou des valeurs primitives traitées comme des objets) ;
* Les fonctions sont des objets ;
* Les tableaux sont des objets ;
* Les dates sont des objets ;
* Les expressions régulières sont des objets.

### Mais qu’est-ce qu’un objet ?

Comme dans la « vraie » vie, par exemple, un crayon est un objet.

Il existe des crayons de différentes couleurs et de différentes tailles ou formes. La couleur, taille ou forme d’un crayon vont être des propriétés.

>Tous les crayons vont posséder **les mêmes propriétés** (tous les crayons possèdent une taille) mais **les valeurs associées à ces propriétés vont être différentes** (chaque crayon peut avoir une taille différente des autres).

De plus, *un crayon sert à écrire*. "Ecrire" est donc ici *une fonction de l'objet crayon* ou encore ce que nous allons désormais appeler **une méthode**.

### Les objets natifs du JavaScript

En JavaScript, vous devez savoir qu’il existe déjà des objets natifs, c’est-à-dire des objets qui possèdent déjà leurs propriétés et méthodes et qui sont déjà « prêts à l’emploi ».

Nous avons déjà rencontré trois objets natifs du JavaScript dans ce cours : l’objet `String` (qui gère les chaînes de caractères), l’objet `Number` (pour les nombres) et l’objet `Boolean` (pour les booléens).

Il en existe évidemment d’autres, comme l’objet `Array` (qui gère les tableaux) que nous étudierons plus tard.

On appelle également ces objets *des objets globaux* car ils vont nous permettre de créer de nouveaux objets de même « type ».

## Création d’objets en JavaScript

Outre les objets natifs, nous pouvons également créer nos propres objets en JavaScript.

Nous disposons de trois façons pour créer de nouveaux objets :

* On peut utiliser le mot clef new et créer un objet à partir de Object() ;
* On peut créer un objet littéral ;
* On peut définir un constructeur puis créer des objets à partir de celui-ci.


## Créer des objets en utilisant `new Object()`

```javascript

      //On crée un objet en utilisant new Object()
      var me = new Object();

      //On définit des propriétés pour notre objet

      me.lastName = "John";
      me.firstName = "Lennon";
      me.age =45 ;

      //On affiche par ex la valeur liée à firstName
      alert(me.firstName)

```


![object](/images/object.png)


## Créer un objet littéral

>Créer un objet littéral est la manière généralement recommandée de créer un objet, et c’est également la manière la plus simple de procéder.

```javascript
   var me = {
       lastName : "John",
       firstName : "Lennon",
       age : 45,

       //this sert de référence à l'objet utilisé
       id : function(){
            return this.lastName+ ' ' + this.firstName;

       }
   };
       //O affiche le résultat retourné par notre méthode
       alert(me.id());

```
![object](/images/object2.png)

* Notez l’utilisation du mot clef `this` qui fait ici référence à l’objet couramment utilisé qui signifie `this.lastName` va aller rechercher la valeur liée au `lastName` de l’objet `me`, c’est-à-dire `John`.

* `This` est *un mot clef récurrent dans les langages orientés objets* et il est très important de bien en comprendre les différents sens selon les utilisations qui sont faites de celui-ci.

* Notez également qu’il nous faut ajouter une paire de parenthèses afin de bien accéder au résultat retourné par notre méthode `id()`.
Sans l’utilisation de ces parenthèses, cela retournerait la valeur de la propriété `id`, c’est-à-dire tout le script de notre fonction.

## Créer des objets à partir d’un constructeur

La dernière méthode pour créer des objets en JavaScript est de créer un constructeur puis ensuite de créer des objets à partir de celui-ci.

Notre constructeur va lui même contenir des méthodes et des propriétés et les objets que nous allons créer à partir de celui-ci vont en hériter.

>Nous utiliserons cette façon de faire pour des **gros projets** pour lesquels nous aurons à créer beaucoup d’objets similaires.

Parmi les constructeurs natifs du JavaScript, nous avons déjà vu le constructeur
`String()` à partir duquel nous avons créé des objets de type *string*.

Nous avons ensuite pu observer que l’on pouvait toujours accéder aux propriétés et aux méthodes définies dans le constructeur `String()` à travers nos objets de type *string* et même à travers *les valeurs primitives*.

Voici ci-dessous une liste des constructeurs natifs les plus connus et utilisés en JavaScript :

* `Object()`;
* `String()`;
* `Number()`;
* `Boolean()` ;
* `Array()`;
* `RegExp()`;
* `Function()` ;
* `Date()` ;

Essayons de créer un nouveau constructeur ensemble. Tout d’abord, vous devez savoir qu’un constructeur est avant tout une fonction et doit donc être déclaré avec le mot clef `function`.

Ensuite, dans cette fonction constructeur, nous allons définir des propriétés et des méthodes.

```javascript
//On crée un constructeur "Identity()"
function Identity(l, f, a){
    this.lastName = l;
    this.firstName = f;
    this.age = a;
}

//On créé des objects à partir de notre constructeur
var john = new Identity("John", "Lennon", 45);
var ringo = new Identity("Ringo", "Stars", 50);

//Ensuite
alert('Age de John : ' + john.age +
      '\nAge de Ringo : ' + ringo.age);

```

![object](/images/object4.png)

* Ici, nous avons créé un constructeur très simple. Dans ce cas là, le mot clef
`this` va une nouvelle fois faire référence à l’objet sur lequel on travaille actuellement.

* Par exemple, lorsque l’on crée l’objet `john` à partir de notre constructeur, `john` va prendre la place de `this`.

* Ainsi, pour ensuite récupérer le prénom de l’objet `john`, nous n’avons qu’à y accéder via `john.prenom`.

>Notez que lorsqu’on crée un constructeur, nous sommes ensuite obligés d’utiliser le mot clef `new` pour créer de nouveaux objets à partir de celui-ci.

# L’objet String

L’objet `String` est l’objet qui gère *les chaînes de caractères*. Cet objet possède **trois propriétés** et **une vingtaine de méthodes**.

>Comme nous l’avons vu précédemment, nous n’utiliserons pas la fonction constructeur de cet objet pour créer de nouveaux objets de type string : on préfèrera utiliser des valeurs primitives.

Cependant, rappelez vous que nous allons pouvoir utiliser les propriétés et méthodes de cet objet avec nos valeurs primitives.

Les propriétés de l’objet `String` sont les suivantes :

* La propriété `length` qui va nous permettre de connaître la longueur d’une chaîne de caractères ;
* La propriété `prototype` qui nous permet d’ajouter de nouvelles propriétés ou méthodes à un objet ;
* La propriété `contructor` qui va retourner la fonction qui a créé le prototype de l’objet String.

# L'objet Number

L’objet Number sert à gérer les nombres en JavaScript.

>Tout comme pour les chaînes de caractères, nous préférerons utiliser les valeurs primitives plutôt que de créer un nouvel objet de type Number à partir de sa fonction constructeur dans la mesure du possible.

L’objet Number possède cinq propriétés qui lui appartiennent exclusivement. Cela signifie qu’on ne peut les utiliser que sur l’objet Number en soi, et pas sur d’autres objets ou valeurs primitives de type Number :

* Les propriétés `MIN_VALUE` et `MAX_VALUE` vont respectivement retourner le plus petit et le plus grand nombre possible en JavaScript ;
* Les propriétés `NEGATIVE_INFINITY` et `POSITIVE_INFINITY` représentent l’infini côté négatif et positif ;
* La propriété `NaN` représentant une valeur qui n’est pas un nombre.
