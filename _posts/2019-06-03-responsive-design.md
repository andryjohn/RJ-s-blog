---
layout:     post
title:      Responsive design
date:       2019-06-03
summary:   
categories: Technique
---


![apple](/images/responsive.jpeg)
>Les mots « responsive design », en anglais, peuvent être traduits en français par « design adaptable ».
Par extension, le « responsive design » désigne généralement l’ensemble des techniques nous permettant d’adapter nos pages web à toutes les tailles d’écrans afin d’avoir un bon rendu.

La problématique du responsive design est apparue avec l’apparition des *tablettes* et des *Smartphones* pouvant se connecter à Internet : en effet, comment faire pour que mon site s’affiche aussi bien sur un petit écran de téléphone portable que sur un ordinateur de salon ?

Il existe trois façons d’adapter son site afin d’avoir un bon rendu visuel sur toutes les tailles d’écrans :

- Créer un site dédié pour chaque terminal différent (un site mobile, un site pour ordinateur, etc.) ;
- Créer une application mobile en plus de notre site web (gérant l’environnement Androïd et iOS) ;
- Utiliser les outils offerts par le HTML et le CSS et créer une version « responsive » de notre site.

 Nous nous concentrerons sur cette troisième méthode



## LE VIEWPORT

Le « *viewport* » correspond à la taille de la fenêtre web de vos visiteurs.

Une première méthode, très simple, pour commencer à optimiser son site web pour un affichage sur mobile ou tablette est d’utiliser et de manipuler le viewport.

En HTML5, nous pouvons prendre « contrôle » de la taille de la fenêtre grâce à l’élément `meta` et aux attributs `name` et `content`.

On va demander à ce que nos pages web s’adaptent à la taille de la fenêtre de chacun de nos visiteurs, afin que notre contenu la remplisse.

Cela ne va évidemment pas toujours fournir un résultat parfait, mais ce sera déjà un bon début !

---

```html
<head>
  <meta name=viewport content="device-widht, initial-scale=1.0">
</head>

```


Le code `width=device-width` va faire en sorte que la page s’adapte à la taille de l’écran de votre visiteur avec les éléments HTML prenant la place disponible.

Le code `initial-scale=1.0` définit le niveau de zoom initial lorsque la page est chargée par le navigateur.

---

![phone](/images/viewport.png)


## MEDIA QUERIES ET RESPONSIVE DESIGN


Les media queries correspondent à une technique introduite en CSS3 et qui va se servir de la règle CSS `@media`.

Cela va nous permettre par exemple de ne pas afficher certains éléments pour des tailles d’écran trop petites ou de réorganiser nos pages web grâce aux propriétés CSS.

### Utilisation de @media en CSS

Nous allons obligatoirement devoir préciser une chose avec `@media` : le type de media pour lequel les déclarations CSS doivent s’appliquer.

Dans l’immense majorité des cas, nous utiliserons `@media screen`, afin d’appliquer nos propriétés à tous les medias dotés d’un écran (téléphone portable, tablette, ordinateur de bureau, etc.).

Cependant, sachez que l’on peut également utiliser `@media print`, par exemple, afin de n’appliquer certaines règles que pour les imprimantes ou encore @media speech, pour les ordinateurs spéciaux qui vont « lire à haute voix » une page.

Finalement, on peut également utiliser `@media all` pour appliquer des déclarations à tous les types de media.

Avec `@media screen`, nous préciserons également une taille ou un intervalle de tailles d’écran au sein duquel les propriétés vont s’appliquer. C’est cette fonctionnalité qui va nous permettre de créer un site responsive en soi.

Le comportement d'une page type 'AirBnB' avec flexbox et @media 

---
![airbnb](/images/airrespon2.png)

---

![airbnb](/images/airresp.png)


Pour tester sur [codepen](https://codepen.io/andryjohn/pen/xNZYYN)