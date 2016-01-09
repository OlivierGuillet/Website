+++
title = "Les différents types d’applications mobiles : natives, web apps, hybrides, Flash"
tags = [
    "mobile",
    "web",
    "development"
]
date = "2012-02-18"
description = "Applications natives, web apps, applications hybrides, applications Flash."
+++

---------- 

## Applications natives

Les applications natives sont des logiciels conçus spécifiquement pour une plate-forme mobile, en utilisant le **SDK** propre à celle-ci. Les applications ainsi crées sont ensuite téléchargeables depuis une plateforme dédiée au système, généralement un magasin d’application type App Store d’Apple ou Android Market.

Ces applications permettent de tirer parti de toute la puissance et toutes les possibilités du device mobile : accélération matérielle, capteurs, caméra, accès aux contacts, au fonctions de téléphonie, etc.

## Web Apps

Il s’agit de **sites web optimisés pour mobile**, souvent conçus pour ressembler à de « vraies » applications.
On accède à ces applications web via le navigateur internet du device mobile.
Aujourd’hui grâce notamment au support d‘**HTML5 et de CSS3** il est possible d’aller assez loin dans l’utilisation des capacités des devices. HTML5 permet notamment de gérer le multitouch, la géolocalisation, l’utilisation de l’accéléromètre, la mise en cache de ressources statiques, et même la synchronisation offline, après que l’appareil ait perdu puis retrouvé sa connexion. HTML5 gère également le stockage de données en local.
Google et Facebook notamment utilisent avec succès cette technologie et proposent des version mobiles de leurs applications web.

Ces applications web peuvent être génériques (toute plate-forme mobile) ou bien dédiées à un type de support particulier, par exemple beaucoup d’applications et de frameworks pour mobiles ne fonctionnent que sur un navigateur basé sur Webkit (iOS, Android, BlackBerry>=6.0, WebOS), exemple : [touch.www.linkedin.com](https://touch.www.linkedin.com/)

Le système iOS permet d’utiliser une web app à la manière d’une application, en plaçant un raccourci vers le site web mobile directement sur le bureau, avec une icône. Le navigateur lance alors la web app en plein écran, comme une vraie application.
Android gère en partie ce mécanisme, il permet la mise en raccourci sur le bureau avec icône, mais le navigateur ne se lance pas en plein écran.

## Applications hybrides

Une application hybride est un **mélange de code natif et d’affichage de vues HTML/javascript**. Concrètement toutes les plateformes mobiles proposent un composant de type WebView, permettant d’afficher du contenu web soit sur une partie de l’écran, soit en plein écran, et en utilisant le moteur HTML du navigateur intégré au système.
Ces applications hybrides peuvent être distribuées sur les stores des systèmes mobiles.

Plusieurs stratégies sont alors possibles, selon que l’on place le curseur plus du côté natif ou plus du côté HTML :

 - ne réaliser que certains écrans voir même que certains composants
   d’IHM en HTML.
 - réaliser touts les écrans en HTML mais garder la logique applicative
   en code natif, notamment les effets de transitions entre écrans et la
   gestion du scrolling.
 - réaliser les écrans en HTML, et les transitions / scrolling en
   javascript. Le code natif peut alors se cantonner à quelques
   composants techniques très ciblés. De la même manière selon les
   applications la logique métier peut être codée en javascript ou bien
   en code natif.

Quelques exemples d’applications hybrides :

 - LinkedIn
 - Microsoft Bing pour mobiles

## Applications Flash

Flash Builder / Flex en version 4.5 permettent de packager des applications Android, iOS, et BlackBerry Tablet OS.
Concrètement ces applications Flash **embarquent le runtime AIR** dans leur code.
Comme pour les applications HTML5/javascript il s’agit d’une solution de développement multiplateformes, qui permet d’accéder à la plupart des ressources des smartphones et tablettes : multitouch, accéléromètre, GPS, bases de données locales SQLite.

Attention cependant Adobe a officiellement **stoppé le développement du SDK Flex pour mobile** et l’a offert à la fondation Apache en novembre 2011, on peut donc légitimement s’interroger sur la pérennité de cette technologie, surtout face à HTML5.

## Politique d’approbation Apple

Apple a modifié à plusieurs reprises sa politique d’approbation des applications iOS, menant de nombreux développeurs à la confusion.
Le 8 avril 2010, lors de l’annonce de la sortie du SDK iOS 4.0, Apple annonça que seuls les applications développées en Objective-C, C, C++ ou javascript seraient autorisées. Cela stoppait toute possibilité d’applications écrites en Flash, ainsi que de nombreuses solutions de développement multiplateformes telles que Titanium ou MonoTouch.
Le 9 septembre 2010, Apple a modifié ses conditions de services pour autoriser **toutes les technologies de développement d’applications iOS**, à la seule condition que ces applications ne téléchargent pas de code.

---------- 

# Eléments de comparaison

## Coûts de mise en œuvre

Développer une application native pour plusieurs plateformes mobiles peut coûter très cher, de part la multitude de langages et technologies mises en œuvre.
Selon le nombre de plateformes cibles, une technologie web ou même hybride sera souvent moins coûteuse . De plus il sera souvent plus simple de disposer de développeurs maîtrisant les technologies web, que les diverses plateformes mobiles.

## Qualité, rapidité des applications

Difficile de rivaliser avec les applications natives! Celles-ci seront presque toujours plus rapides.
Mais cela dépend fortement du type d’application en jeu et de ses fonctionnalités.
L’autre point à ne pas négliger est que les utilisateurs sont habitués au look’n'feel natif, et qu’il peut être dangereux de trop s’en écarter.

## Publication et mises à jour

Une importante contrainte des applications natives est que celles-ci doivent être approuvées avant diffusion sur leur store respectif (sauf pour Android), ce qui peut s’avérer long et contraignant. Une application hybride permet de limiter ce désagrément, et une web app de s’en affranchir complètement.
Le même problème se pose pour les mises à jour, il n’est souvent pas possible de diffuser un patch correctif en urgence ou même rapidement sur une application native.

## Monétisation

Les magasins d’applications permettent très facilement de vendre les applications, mêmes si Apple, Google et consorts prélèvent leur part sur les prix de vente, généralement autour de 30%.
Même si les stores d’applications web comment timidement à apparaître, leur usage est encore très restreint.
Les stores servent aussi de moteur de recherche et de vitrines pour les applications, et permettent ainsi de les mettre en avant et de les faire découvrir.

## Conclusion

Il n’y a pas aujourd’hui de solution miracle, le choix d’une technologie applicative dépendra de **plusieurs facteurs déterminants** :

 - type d’application (jeux 3D, appli « de gestion », journal en ligne,
   application devant accéder à la caméra ou aux contacts internes du
   téléphone, …)
 - nombre de plateformes mobiles ciblées : plus elles seront nombreuses
   plus les solutions multiplateformes seront intéressantes et rapides à
   mettre en place budget : en général les solutions multiplateformes
   sont moins coûteuses à mettre en place
 - nécessité ou non d’une présence sur les marchés d’applications
 - fréquence des mises à jour (attention au délai d’approbation,
   notamment par Apple) connaissances des équipes de développement : il
   est généralement plus simple de disposer de développeurs maîtrisant
   HTML5/javascript ou Flash que connaissant à la fois java,
   Objective-C, C# voir C++.
   
----------    