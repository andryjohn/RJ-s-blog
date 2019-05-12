---
layout:     post
title:      Pourquoi choisir Jekyll pour son site?
date:       2019-05-11
summary:   Jekyll est un générateur de site statiques écrit en Ruby, qui présente de nombreux avantages que je vais vous présenter dans cet article.
categories: Developper skills
mathjax: true
--- 

Il faut savoir que pour créér ce site j'ai choisi d'utiliser [**Jekyll**](https://jekyllrb.com/). Pourquoi ce choix?

Tout d'abord, *Jekyll* est ecrit en [*Ruby*](https://rajohnson-andry.tk/developper/skills/2019/05/03/ruby-on-rails/) , que c’est actuellement un projet *très actif*, et qu’il est compatible avec *Github Pages*, **nativement**, c’est-à-dire que Github détecte, quand vous créez *une branche gh-pages*, que vous allez générer du contenu statique, et le met en production. Si vous voulez en savoir plus c'est [ici](https://rajohnson-andry.tk/developper/skills/2019/05/05/Host-any-front-end/)


## Pourquoi ne pas choisir un CMS comme Wordpress?


Un système de gestion de contenu (CMS) tel que "Wordpress", (*je cite ce dernier du fait de sa popularité auprès des developpeurs et des particuliers, mais il y en a  d'autres tel que Joomla, Drupal, Typo3, Magento, Prestashop*), aurait été parfait. 

Le problème justement réside dans sa popularité et aussi la technologie qu'il embarque. 
Wordpress est écrit en **PHP**, repose sur **une base de données MySQL** et est distribué par l'entreprise américaine [Automattic](https://automattic.com/).
Du fait de sa popularité, (*je n'ai pas les chiffres en téte mais je crois que c'est 30% des sites mondiaux, c'est énorme*), les sites Wordpress subissent des attaques incessantes.


![cms](/images/cms.jpeg)


>**"La vitesse du site"**: Le couple **PHP&MySQL** et **hébergement mutualisé sur OVH**, en plus si vous rajoutez des plugins (inutiles), ne fait pas souvent bon ménage, et cela se fait ressentir par les temps de chargement, un site qui rame comme jamais et ce n'est le top.
 
## Jekyll, comment ça marche ?

Jekyll est un générateur de site statiques écrit en "Ruby". 

Cela peut paraître tout à fait absurde par rapport à un CMS mais cela apporte bien des avantages et notamment le fait qu'il peut etre couplé à [git et github](https://rajohnson-andry.tk/developper/skills/2019/05/05/maitrise-de-git/). Et c'est la, tout l'intérets, je m'explique:

**Github** est une architecture qui tourne autour de **Git**, un outil open source de *versionning*, c’est-à-dire que le concept de *backup* est compris dans l’outil, en plus de la possibilité de manière assez simple de venir éditer un article comme celui-ci par exemple.

Les pages sont **statiques**, il n’y a donc pas mieux en termes de vitesse et de sécurité pour les visiteurs et l'utilisateur.
Pas besoin de disposer d’un *serveur surdimensionné*, car les pages sont statiques, et les serveurs aiment bien ça, le contenu statique. En plus, [**Github pages**](http://localhost:4000/developper/skills/2019/05/05/Host-any-front-end/) est **gratuit**, oui vous avez bien lu, c'est *entièrement gratuit.*


![free](/images/free.jpeg)



Vous avez une copie entière de votre site sur votre ordinateur.
Vous pouvez faire tourner votre site en local avant de le lancer en production. Pour chaque version. Et c'est tout simplement génial.

Et dès que vous déployez le site, si il n’y a pas d’erreurs, il est mis en ligne automatiquement.

> Aucun paramétrage nécessaire pour indiquer à Github : “Hey, j’ai foutu un Jekyll sur ce repo, déploie-le moi dude”. Il le trouve, et il le lance. Et c'est tout!

Pour d’autres services, il est possible de les déployer aussi sur Github (ou d’autres outils tels que des Gitlabs), mais cela implique soit de passer par un outil de CI (Intégration Continue) qui va détecter les changements du dépôt Git et générer le site statique, ou de compiler soi-même lors de chaque modification.

Enfin, Jekyll n’est pas limité aux blogs, on peut tout à fait réaliser d'autres projets, de faible envergures, j'entend, tel que les sites personnels, portefolio, site vitrines,  des pages produits en rajoutant les "layouts" correspondants. Il suffit en suite de définir dans chaque "fichier sourc" le layout à utiliser pour sa génération.

<footer>
	<cite title="author">Author: Andry Rajohnson</cite>
</footer>
