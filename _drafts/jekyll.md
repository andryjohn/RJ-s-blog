WordPress, c’est un peu comme un gruyère. Tu auras beau essayer boucher les trous, ça restera un fromage de merde. Je ne peux pas m’en prendre seulement à WordPress ou OVH, c’est une accumulation de petites choses qui font qu’il faut changer le moteur. Et ne pensez pas que je ne porte pas WP dans mon coeur, j’ai déployé de nombreux WP ses dernières années et c’est vraiment simple à prendre en main pour les clients, surtout quand ils veulent pouvoir modifier leurs contenus avec un espace administrateur, toussa.
L’avantage de passer du couple Mutualisé-qui-rame, PHP/MySQL & un tas de plugin inutiles à Github Pages + Jekyll, c’est que :

Github est une architecture qui tourne autour de Git, un outil open source de versionning, c’est-à-dire que le concept de backup est compris dans l’outil, en plus de la possibilité de manière assez simple de venir éditer un article comme celui-ci par exemple.
Les pages sont statiques, il n’y a donc pas mieux en termes de vitesse pour les visiteurs.
Pas besoin de disposer d’un serveur surdimensionné, car les pages sont statiques, et les serveurs aiment bien ça, le contenu statique.
En plus de ne pas avoir besoin d’un serveur surdimensionné, je suis même passé d’une facture de 43€/an d’hébergement à 0€, car Github Pages c’est gratuit.
Vous avez une copie entière de votre site sur votre ordi.
Vous pouvez faire tourner votre site en local avant de le lancer en production. Pour chaque version. Par exemple, si vous faites une modif de CSS ou de JS, vous pouvez tester en local la fonctionnalité avant de la balancer à l’arrache en prod. Ce qui devrait toujours être fait, mais c’est vite fait de vouloir patcher un truc directement via le fichier distant en FTP. Ouais, j’ai fais ça pendant mes années de jeunesse.

J’ai finalement choisi Jekyll, car c’est actuellement le projet le plus actif, et parce qu’il est compatible avec Github Pages, nativement, c’est-à-dire que Github détecte, quand vous créez une branche gh-pages, que vous allez générer du contenu statique.

Et dès que vous déployez le site, si il n’y a pas d’erreurs, il est mis en ligne automatiquement, c’est-à-dire qu’il n’y a aucun paramétrage nécessaire pour indiquer à Github : “Hey, j’ai foutu un Jekyll sur ce repo, déploie-le moi dude”. Il le trouve, et il le lance.

Pour d’autres services, il est possible de les déployer aussi sur Github (ou d’autres outils tels que des Gitlabs), mais cela implique soit de passer par un outil de CI (Intégration Continue) qui va détecter les changements du dépôt Git et générer le site statique, ou de compiler soi-même lors de chaque modification.

Prérequis
Npm (il est compris avec NodeJS)
Jekyll
Un compte GitHub
Du temps
Beaucoup de café
Initialisation de Jekyll
La documentation est très claire, après avoir installé Jekyll, vous devez exécuter les lignes suivantes :


Jekyll est un générateur de site statiques écrit en Ruby.

Cela peut paraître tout à fait absurde par rapport à un CMS mais cela apporte bien des avantages si le projet le permet :

Au final c’est un site statique qui est uploadé sur le serveur (donc pas besoin de Ruby).
C’est difficile de faire plus rapide qu’un site statique.
Dans ce cas, pourquoi passer par un générateur ?

Un générateur permet de gérer plus facilement tous les assets du projet (CSS, JS, images et compression, etc.)
On peu utiliser des layout et des partials pour ne pas avoir à ré-écrire chaque fois son code.
Le contenu de chaque page est séparé de son affichage et lorsqu’on lance la génération du site, le générateur injecte le contenu dans le moule correspondant.
Un exemple simple de blog avec Jekyll
Dans le cas d’un blog, nous avons :

Un fichier de layout général qui contient tout l’HTML principal (doctype, head, métas) avec éventuellement footer, header et sidebars en partials. Ce fichier va également définir le comportement de la page d’accueil (affichage des X derniers posts). Jekyll utilise par défaut Liquid comme langage de templating.
Un autre layout pour l’affichage des billets de blogs.
Un répertoire contenant le contenu proprement dit (les billets).
Plusieurs choix sont possibles, mais par défaut ce sont des fichiers markdown un peu spéciaux. Ils ont un en-tête avec différentes variables pour le titre, l’auteur, la date et éventuellement les catégories du billet.
On peut également définir un layout différent de celui par défaut.
Un fichier de configuration (en yaml) qui va servir de chef d’orchestre et dire à Jekyll quoi faire pour la génération.
Lorsqu’on lance la génération :

Jekyll compile les différents assets suivant les règles prédéfinies ;
Génère les pages HTML à parti des fichiers sources markdown.
Jekyll peut générer également une sitemap, des archives, etc.
Il peut également parser les fichiers sources et transformer par exemple des liens vers flickr en mini-galeries d’images ou des liens youtube en players intégrés à la page. Il existe de nombreux plugins pour cela.
A noter que Jekyll permet aussi d’avoir un mode serveur où la compilation se fait à la volée et où on peut voir les résultats sur un serveur local.

Enfin, il existe des plugins pour pouvoir automatiquement déployer son site via FTP, SFTP, Git etc.

Jekyll est notamment très bien intégré à Github et c’est la solution recommandée pour générer les pages de présentation d’un projet.

Jekyll n’est pas limité aux blogs, on peut tout à fait réaliser un portfolio ou des pages produits en rajoutant les layouts correspondants. Il suffit en suite de définir dans chaque fichier source le layout à utiliser pour sa génération.


