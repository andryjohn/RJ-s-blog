---
layout:     post
title:     (French) Introduction à Git
date:       2019-05-05
summary:
categories: Developper skills
mathjax: true
---
![git](/images/git2.jpeg)
>Le but de Git est de permettre à une équipe de développement de suivre les différentes versions d’un projet pour en gérer l’évolution

Quand on développe un projet il ne suffit pas de coder pour soi dans son coin ni pour l’instant présent, il faut aussi penser aux évolutions possibles du code, aux erreurs que l’on peut faire, aux personnes qui vont aussi travailler sur le projet…


C’est pourquoi il est indispensable de mettre en place dès le début du projet, *un outil* qui permet de gérer tout cela. Ils sont nombreux, avec plus ou moins de fonctionnalités, mais celui dont je vais vous parler aujourd’hui est tout d'abord celui que j'utilise au quotidien mais aussi, il est au top depuis quelques temps déjà et est parti pour servir encore de longues années, il s’agit de Git.

# Qu’est-ce que Git ? Les concepts à comprendre

Git est un logiciel de **gestion de versions** (outil de "versionning") distribué, créé par [Linus Torwalds](https://fr.wikipedia.org/wiki/Linus_Torvalds)  en 2005 et distribué **gratuitement sous licence publique générale GNU version 2.**
Si la fin de la phrase est simple à comprendre (quoi que…), nous allons détailler son début :

## Un outil de gestion de versions

![mark](/images/Version.png)



Le but de Git est de permettre à une équipe de développement de suivre les différentes versions d’un projet pour en gérer l’évolution.

>  Dans cet exemple, nous allons oublié un peu le code et imaginons un exposé sur *l’économie du cacao* en *Côte d’Ivoire* réalisé par 3 lycéens : **Pierre** est en charge de l’exposé en lui-même, **Paul** rédigera *l’introduction* et la conclusion, **Jacques** aura la responsabilité des illustrations et de la mise en page.
Ce faisant , **Pierre** *enregistre* son document sur une clé USB, qu’il transmet à **Paul** y ajoute son *introduction* et sa *conclusion* sans relire le travail de **Pierre**. Il donne ensuite la clé USB à **Jacques** qui fait son travail de mise en forme avant de donner la clé USB au professeur.
Ce denier, consulte le document et s’aperçoit qu’il manque *un chapitre entier*, celui consacré au "commerce équitable." Qui est **fautif** ? (vous avez 3 heures…)



**Git** est là pour répondre à cette question en permettant de garder une copie de toutes les *versions* des documents, avec pour chaque version, l’identité de la personne qui a fait les modifications et les détails de cette modification. Appliquez cela à n’importe quel *projet*, informatique ou non, et vous aurez compris **l’intérêt de Git**.

---

## Le vocabulaire de Git

Nous allons vous initier plusieurs mots que vous ne connaissez peut-être pas, mais qui sont indispensable à la maitrise de git.

![mark](/images/projet.jpeg)

## Dépôt, *repository* ou remote

Je vais encore oser une métaphore simpliste :
>"Quand vous mangez, vous utilisez des couverts. Lorsque vous avez terminé votre repas vous lavez ces couverts et vous les rangez dans un tiroir où d’autres pourront les utiliser.
Un **dépôt** peut être comparé à ce tiroir (si si, il faut nettoyer son code avant de le ranger, tout comme une fourchette). Il s’agit d’un endroit où l’on va stocker les "versions du code", à disposition de tous les participants au projet qui vont venir en faire une copie chez eux et éventuellement faire des mises à jour. "

"*On me dit à l’oreille qu’on ne peut pas faire une copie des fourchettes du tiroir, effectivement toute méthaphore à une limite*."

 Un projet peut avoir un ou une **multitude de dépôts**, en lecture seule ou sur lesquels l’écriture est permise…

## Validation ou commit

Un **commit** n’est ni plus ni moins qu’une *version* du projet, un instantané ( une photo ou un "snapshot" dans le temps) pris à **un instant T**.

   ![mark](/images/git.jpeg)

A chaque fois que vous faites un commit, Git enregistre un «arbre» qui permettra d’identifier vos fichiers modifiés et lui associe un objet *commit*.

## Branche

La vrai force de Git se trouve dans le concept de "branche". Nous venons de voir ce qu’est un *commit*, une *branche* est simplement un pointeur vers un commit.

Puisque chaque commit connaît son précédent, il est possible de remonter de commit en commit pour retracer toute la branche. Pour simplifier, imaginons que nous avons créé un projet et fait 3 commits. Alors que nous ne nous sommes pas souciés de créer une branche, Git l’a fait pour nous. Dès le début le projet possède une branche *par défaut*, appelée **master**. Après nos 3 commits, master pointe vers le dernier commit en date.

---

>Nous souhaitons maintenant créer une branche pour permettre à une autre équipe de developpeur, de crées de nouvelles fonctionnalités sans affecter la branche principale. Git va simplement créer un nouveau pointeur vers le dernier commit de la branche courante (donc master). Nos branches **"master"** et **"feature"** sont pour le moment identiques.
A partir de ce moment précis, la deuxième équipe pourra travailler sur la nouvelle branche récemment crée, sans que la branche principale (master), ne soit affecter. Le travaille fini et validé, elle pourra etre fusionné dans *master*.
![mark](/images/git.png)

---
<footer><cite title="Workshop"> "Anything in the master branch is deployable". Scott Chacon
</cite></footer>


Et c'est la toute la puissance de **Git**, telle une réalité parallèle, ou l'on va pouvoir effectuer des changements, sans que cela n'affectent la branche principale (*master*).

---

# Pour aller plus loin..

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed//hPfgekYUKgk' frameborder='0' allowfullscreen></iframe></div>



