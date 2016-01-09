+++
title = "Panorama des différentes plateformes mobiles pour smartphones et tablettes"
tags = [
    "mobile",
    "development"
]
date = "2012-02-22"
description = "iOS / Android / Windows Phone / BlackBerry / Bada / Symbian / webOS / Firefox OS / Tizen"
+++

----------

{{< figure src="/img/panorama-plateformes-mobiles/Logo-iOS.jpg" alt="iOS" >}}

[iOS](http://www.apple.com/fr/ios/) est le système d’exploitation intégré à la fois dans **l’iPhone, l’iPod Touch et l’iPad**, et mis au point par **Apple**.

iOS est dérivé de Mac OS X (et donc d’Unix), avec qui il partage le même framework, **Cocoa**, et le langage de programmation associé l’**Objective-C**.
Objective-C est une surcouche du C, en y ajoutant la notion de **programmation object**. Celle-ci est fortement inspiré de celle de SmallTalk, notamment au niveau des design patterns mis en œuvre (MVC, Key-Value Coding).

Le développement d’applications natives s’effectue exclusivement dans l’environnement [Xcode](https://developer.apple.com/xcode/index.php) (gratuit), sur ordinateur Mac.
Apple fournit également un **simulateur d’iPhone et d’iPad** avec son [SDK iOS](https://developer.apple.com/devcenter/ios/index.action).

---------- 

{{< figure src="/img/panorama-plateformes-mobiles/Logo_Android.png" alt="Android" >}}

[Android](http://www.android.com/) est le système d’exploitation conçu par **Google** et l’[Open Handset Alliance](http://www.openhandsetalliance.com/).
Celui-ci équipe aujourd’hui des appareils très variés : smartphones, tablettes, TV, autoradios, montres digitales, …
Android est gratuit pour les constructeurs d’appareils souhaitant l’utiliser, et partiellement open-source.
Concrètement le système d’exploitation s’appuie sur un **noyau Linux optimisé** pour un usage mobile, et sur une **machine virtuelle Java** assez fortement modifiée, nommée **Dalvik JVM**. Celle-ci n’exécute pas les .class habituels mais des fichiers portant l’extension .dex, compilés différemment et optimisés par le [SDK Android](http://developer.android.com/sdk/index.html).
Le développement se fait donc en Java, mais sur cette JVM spécifique à Android. Il n’est de fait pas possible d’utiliser n’importe quelle librairie Java dans une application Android, les librairies Android devant être compilées pour la JVM Dalvik.

Il est possible d’utiliser divers IDE Java pour développer et compiler une application Android, mais Google fournit un [plugin Eclipse](http://developer.android.com/sdk/eclipse-adt.html), dont il serait dommage de se passer.

A noter que Motorola fourni également un IDE dédié au développement Android, regroupant Eclipse et le plugin Android de Google, nommé [Motodev Studio](http://developer.motorola.com/docstools/motodevstudio/).

Il est également possible de développer en code C++ natif, via le [NDK](http://developer.android.com/sdk/ndk/index.html) (Native Development Kit), pour les applications ayant un besoin critique de performances tels les jeux vidéos en 3D.

---------- 

{{< figure src="/img/panorama-plateformes-mobiles/Logo-Windows-Phone-Mango.jpg" alt="Windows Phone" >}}

[Windows Phone 7](http://www.microsoft.com/windowsphone/fr-fr/) a été lancé en novembre 2010 par **Microsoft**, il succède à Windows Mobile en étant plus orienté grand public. Il est basé sur un noyau [Windows CE](http://fr.wikipedia.org/wiki/Windows_CE).

Cet OS mobile équipe uniquement des smartphones, c’est le futur Windows 8 qui est annoncé comme pouvant équiper des tablettes à sa sortie.

Windows Phone 7 dispose d’une IHM conçue nativement pour écrans tactiles multitouch, dénommée **Modern UI** (anciennement Metro), qui se démarque des autres IHM mobiles par l’utilisation de tuiles à la place d’icônes. Ces tuiles peuvent afficher des informations en temps réel, à la manière des widgets Android, et couvrent toute la surface d’affichage, il n’y a donc pas de véritable fond d’écran.

Le développement d’applications pour Windows Phone 7 est possible via deux langages au choix : **C#** et **VB.NET**. Windows Phone 7 supporte deux plateformes de développement, que l’on peut mixer dans la même application, et toutes deux bâties sur le **.NET Compact Framework** :

 - **Silverlight**, utilisée en général pour le développement d’applications
   de gestion.  Les IHM sont donc décrites en XAML. Windows Phone
   utilise une version modifiée de Silverlight, adaptée aux spécificités
   des appareils mobiles.
 - **XNA**, la plateforme dédié au développement de jeux 2D et 3D, ainsi que
   les traitements audio.

Microsoft propose ses [Windows Phone Developer Tools](http://www.microsoft.com/fr-fr/download/details.aspx?id=13890) pour le développement des applications. Ce package, gratuit, comprend :

 - **Visual Studio 2010 Express**, la version légère et gratuite de Visual
   Studio 2010.
 - un émulateur Windows Phone
 - Expression Blend, pour la création des écrans.

Côté navigateur internet, celui-ci était initialement un mix entre IE7 et IE8 ne proposant pas de support HTML5. Depuis la sortie de Windows Phone 7.5 (Mango) celui-ci est basé sur IE9 et supporte partiellement HTML5.

Le futur Windows Phone 8 sera basé sur un noyau Windows NT,  et plusieurs composants de l’OS seront partagés avec Windows 8, ce qui autorisera un portage aisé d’applications entre les deux systèmes. Il est annoncé comme étant rétro compatible avec les applications Windows Phone 7.

Enfin son navigateur sera basé sur IE10, proposant une compatibilité accrue avec HTML5.

---------- 

{{< figure src="/img/panorama-plateformes-mobiles/Logo_Blackberry_OS.jpg" alt="BlackBerry" >}}

Le système BlackBerry, du fabriquant canadien [RIM](http://www.rim.com/) (Research In Motion), fut un précurseur sur le marché des PDA et smartphones. Il fut le premier à proposer la **notification instantanée d’emails**, en mode push.

BlackBerry OS optimise également l’utilisation mobile en **compressant les pages web**, ainsi que les pièces jointes des mails, et permet une **sécurisation** efficace des échanges.

En septembre 2010, RIM a lancé un nouveau système d’exploitation, BlackBerry Tablet OS, qui équipe aujourd’hui uniquement sa tablette BlackBerry PlayBook, mais qui devrait à terme remplacer totalement son BlackBerry OS sous le nom de **BlackBerry 10**.

Pour [développer sur BlackBerry](https://bdsc.webapps.blackberry.com/devzone/), de nombreuses possibilités existent :

 - le [SDK Java](https://bdsc.webapps.blackberry.com/java/), et le
   plugin Eclipse associé, les BlackBerrys disposant d’une JVM
   spécifique.
 - le [SDK pour Adobe AIR](https://bdsc.webapps.blackberry.com/air/),
   afin de développer des applications Flash en Action Script.
 - un nouveau framework présenté fin 2010, [BlackBerry
   WebWorks](https://bdsc.webapps.blackberry.com/html5/), permet de
   développer des applications web en HTML5/CSS3 et javascript. La
   plateforme permet de packager des applications BlackBerry et de les
   déployer sur le BlackBerry App World.

Deux possibilités supplémentaires existent pour réaliser des applications dédiées à la tablette BlackBerry PlayBook, et aux futurs smartphones de RIM :

 - le [SDK natif](https://bdsc.webapps.blackberry.com/native/), pour
   développer en C/C++ via un EDI fourni par RIM.
 - enfin il est possible de packager des [applications
   Android](https://bdsc.webapps.blackberry.com/android/) pour les faire
   tourner sur BlackBerry Tablet OS, RIM espérant ainsi pallier au
   manque d’applications sur sa tablette.

---------- 

{{< figure src="/img/panorama-plateformes-mobiles/Logo_Bada.jpg" alt="Bada" >}}

[Bada](http://www.bada.com/) est le système d’exploitation pour mobiles mis au point par **Samsung** pour équiper une partie de ses smartphones (d’autres tournent sur Android ou Windows Phone). Bada OS est une évolution pour le haut de gamme du système SHP (Samsung Handheld Platform) OS équipant de nombreux appareil Samsung de milieu de gamme. Tous les smartphones Samsung équipés du système Bada ont un nom commençant par *Samsung Wave*. Il devrait disparaître courant 2013 de cette gamme de smartphone au profit de Tizen.

Le système intègre la technologie **TouchWiz** pour l’interface utilisateur, la même que sur les smartphones Android du constructeur coréen.  Le [développement](http://developer.bada.com/apis/index.do) se fait grâce à un SDK en C++ fourni par Samsung et un IDE basé sur Eclipse.

---------- 

{{< figure src="/img/panorama-plateformes-mobiles/Logo_symbian_OS.png" alt="Symbian" >}}

Nokia créa Symbian OS en 1998 en compagnie de Panasonic, Psion,  Ericsson et Motorola. Nokia fut ensuite le principal utilisateur de Symbian pendant de nombreuses années pour équiper ses téléphones mobiles et smartphone,  et racheta tous les droits du consortium **Symbian Ltd** en 2008.

Aujourd’hui, la plateforme pour téléphones mobiles [Symbian](http://symbian.nokia.com/) succède à **Symbian OS et Nokia Series 60**, en unifiant ces deux composantes système.

Auparavant, Symbian OS nécessitait une surcouche pour présenter une ihm aux utilisateurs. Le framework Series 60 de Nokia était alors un de ceux couramment utilisés dans ce but, en compagnie de UIQ et JavaME. Le développement, réputé difficile, était réalisé en C++.  Il peut aujourd’hui être fait principalement avec le framework QT, toujours en C++, via les IDE QT Creator ou Carbide.

La plateforme Symbian, en perte de vitesse,  a été cédée à Accenture en 2011 suite au partenariat de Nokia et Microsoft autour de Windows Phone.

---------- 

{{< figure src="/img/panorama-plateformes-mobiles/Logo_WebOS.png" alt="webOS" >}}

Ce système d’exploitation mobile propriétaire, basé sur un noyau Linux 2.6, a été conçu par [Palm](https://developer.palm.com/), fabriquant américain de PDA, pour équiper ses téléphones mobiles. Suite au rachat de Palm par HP en 2010, le système webOS dans sa dernière version 3.0 équipe également la tablette **HP TouchPad**.

Les applications sont développées principalement en **HTML5, CSS et javascript** (d’où le nom de la plateforme) grâce au SDK nommé [Enyo](https://developer.palm.com/content/resources/develop/quick_start_javascript.html). Il existe également un [kit de développement C/C++](https://developer.palm.com/content/resources/develop/quick_start_c.html) pour le développement OpenGL, principalement jeux vidéos.

En août 2011, devant les faibles ventes de ses appareils, HP a annoncé qu’il arrêtait la fabrication et la commercialisation d’appareils sous webOS. Dans la foulée le constructeur a ouvert le code du système webOS en [open source](http://www.openwebosproject.org/).

----------

{{< figure src="/img/panorama-plateformes-mobiles/Logo-Firefox_OS.jpg" alt="Firefox OS" >}}

Anciennement nommé **Boot To Gecko**, [Firefox OS](http://www.mozilla.org/en-US/firefoxos/) est un système d’exploitation pour smartphones et tablette crée par **Mozilla**, et entièrement **open-source**.

Il a été annoncé en 2011 et est toujours en cours de développement.

L’objectif est de proposer un OS mobile reposant sur des **standarts ouverts du Web** :
_ un noyau Gonk, basé sur un simple **Linux**, partageant quelques composants en commun avec le noyau Android (pilotes d’accès au matériel).
_ un **runtime Javascript nommé Gecko**
_ et une interface utilisateur entièrement écrite en **HTML5/CSS3 nommée Gaïa**

A noter que le runtime Gecko peut s’appuyer sur d’autres systèmes que Gonk, notamment Android (avec des restrictions sur les fonctionnalités).

Le développement d’application se fera vous l’aurez compris en **Javascript / HTML5.**

----------

{{< figure src="/img/panorama-plateformes-mobiles/Logo_Tizen.jpg" alt="Tizen" >}}

[Tizen](https://www.tizen.org/) est un projet de la **Fondation Linux**, dont le développement est assuré par Intel et Samsung.
Il résulte d’un long processus de mise en place d’un OS mobile basé sur Linux, via les projets LiMo, Moblin, Maemo (par Nokia), MeeGo (par Nokia et Intel).

Tout comme Firefox OS et WebOS, il est open-sources et **repose sur le couple Linux / HTML5**, les applications crées devant mêmes être compatibles entres ces différentes plateformes ouvertes.

Les autres composant logiciels de l’OS sont la **librairie EFL** (Enlightenment Foundation Libraries) pour la gestiongraphique, et le **runtime Webkit** pour la partie web.

Le projet est majoritairement porté par Nokia, Intel et Samsung, après le quasi-abandon de Bada OS par ce dernier. Il va d’ailleurs remplacer Bada sur la gamme Wave du constructeur Coréen.

Ce système a pour ambition de **créer un écosystème ouvert**, les pilotes développés étant libres eux aussi (FireFox OS utilise ceux d’Android).

----------