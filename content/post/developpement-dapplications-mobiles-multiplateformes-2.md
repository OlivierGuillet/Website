+++
title = "Développement d’applications mobiles multiplateformes (2/2)"
tags = [
    "mobile",
    "multiplatform",
    "development"
]
date = "2012-11-16"
description = "Ce billet fait suite au précédent décrivant les principales techniques de développement mobile multiplateformes."
+++

----------

Ce billet fait suite au précédent décrivant les principales techniques de développement mobile multiplateformes.

Voyons ici les **principales solutions existantes** et leurs éditeurs:

 - [PhoneGap](http://phonegap.com/) (Adobe)
 - [Titanium](http://www.appcelerator.com/)  (Appcelerator)
 - [Rhodes](http://www.motorola.com/Business/US-EN/RhoMobile+Suite/Rhodes) (Rhomobile) 
 - [jQuery Mobile](http://jquerymobile.com/) (jQuery Foundation, association à but non lucratif) 
 - [Sencha Touch](http://www.sencha.com/products/touch) (Sencha) 
 - [Flex mobile](http://www.adobe.com/devnet/devices.html) (Adobe)
 - [MonoTouch](http://xamarin.com/monotouch) / [Mono for Android](http://xamarin.com/monoforandroid) (Xamarin)
 - [Wope](http://www.backelite.com/software/) (Backelite)
 - Développement hybride « maison »

Bien évidemment il existe de nombreux autres solutions / frameworks / librairies pour le développement multiplateformes, non décrites ici.

---------- 

{{< figure src="/img/developpement-dapplications-mobiles-multiplateformes/multi_phonegap.jpg" alt="PhoneGap" >}}

 - Pour la mise en place d’application hybride comportant des vues web(troisième approche).
 - **Gratuit, open source, supporte TOUTES les plateformes mobiles**, support payant en option.
 - Permet d’appeler les API natives des SDKs mobiles depuis le JavaScript (accès au contacts, caméra, gyroscope, GPS, base de données locale).
 - **Ne propose aucun composants visuels**! Phonegap est en fait une "boite" ou une "coque native" pour encapsuler des composants HTML5 et JavaScript.
 - PhoneGap N’EST PAS un framework JavaScript, il s’utilise AVEC un framework JavaScript complémentaire (au choix).
 - Alternatives : Trigger.io, Sencha Touch native packaging, coque native "fait maison"

---------- 

{{< figure src="/img/developpement-dapplications-mobiles-multiplateformes/multi_titanium.png" alt="Titanium" >}}

 - Propose une API **100% JavaScript** (pas de HTML), le code est ensuite transformé en application native.
 - **Gratuit, API open source** (mais pas le compilateur), supporte uniquement iOS et Android, support payant en option.
 - Inclut un outil de cross-compilation **ONLINE** qui demande un accès internet **PERMANENT**. Les fichiers sources sont envoyés à un serveur propriétaire qui renvoie alors les binaires (JavaScript précompilé). Une machine virtuelle JavaScript exécute alors le code.
 - Inconvénients : syndrome de la boîte noire, difficultés pour débugger, problèmes éventuels de performances et de gestion mémoire.

---------- 

{{< figure src="/img/developpement-dapplications-mobiles-multiplateformes/multi_rhomobile.png" alt="Rhodes" >}}

 - Développement d’applications hybrides en **Ruby et JavaScript-HTML**, fortement inspiré de Ruby On Rails.
 - **Gratuit, open source**, supporte iOS, Android, Windows Phone 7 et BlackBerry.
 - Peu de composants d’IHM fournis, nécessite un framework mobile JavaScript complémentaire (au choix).
 - Plutôt à destination des développeurs Ruby On Rails.

---------- 

{{< figure src="/img/developpement-dapplications-mobiles-multiplateformes/multi_jquery.png" alt="jQuery Mobile" >}}

 - Version mobile du framework **JavaScript jQuery UI** (il contient donc la librairie jQuery). 
 - **Gratuit, open source**, supporte **TOUTES** les plateformes mobiles.
 - Développement en HTML (et JavaScript), plus simple de prise en main que Sencha Touch.
 - Performances moins bonnes que Sencha Touch, et interface reconnaissable qui ne ressemble guère aux widgets natifs.

---------- 

{{< figure src="/img/developpement-dapplications-mobiles-multiplateformes/multi_sencha.png" alt="Sencha Touch" >}}

 - Version mobile du framework **JavaScript ExtJS**.
 - Compatible **iOS, Android, BlackBerry**. Compatibilité Windows Phone 8 annoncée (mais pas WP7).
 - SDK **open source et gratuit** pour le développement d’applications commerciales, payant pour une utilisation OEM. Environnement de développement payant (Sencha Architect).
 - Sencha Touch est **Full JavaScript** (pas de HTML), le DOM est généré par la librairie JavaScript. La prise en main peut donc être plus déroutante que jQuery Mobile.
 - Framework **MVC** et fortement orienté objet.
 - Bonnes performances pour un framework JavaScript
 - De nombreux composants d’IHM (widgets JavaScript assez proches du natif, en tout cas plus que jQuery Mobile).

---------- 

{{< figure src="/img/developpement-dapplications-mobiles-multiplateformes/multi_adobeAIR.jpg" alt="Flash (Adobe AIR)" >}}

 - Fait tourner des applications Flash sur une **machine virtuelle embarquée** (Adobe AIR).
 - Compatible **Android, iOS, et BlackBerry**.
 - SDK gratuit mais environnement de développement payant (Adobe Flash Builder).
 - Pas d’accès aux widgets natifs des plateformes, problèmes éventuels de performances et mémoire (comme toutes les solutions utilisant une machine virtuelle).
 - Le plugin Flash pour Safari Mobile étant abandonnée, la pérennité de cette technologie est incertaine.

---------- 

{{< figure src="/img/developpement-dapplications-mobiles-multiplateformes/multi_Mono.png" alt="Mono" >}}

 - Permet de développer en **C#.NET** sur Android et iOS en générant des applications natives.
 - La partie mobile de Mono est composé en fait de deux SDKs : **Monotouch** (pour iOS, nécessite un Mac avec XCode), et **Mono for Android**.
 - Produit **commercial payant** (399$ par plateforme).
 - **Ne masque pas les SDKs natifs sous-jacents**. On manipule des StoryBoards et Controllers sous iOS, ou des Activity sous Android, le tout en C#.
 - Seul le code métier peut être mutualisé entre iOS, Android et Windows Phone, toute la partie IHM reste spécifique à chaque plateforme.

---------- 

{{< figure src="/img/developpement-dapplications-mobiles-multiplateformes/multi_wope.jpg" alt="Wope" >}}

**Edit du 28/11/2012** : la solution a évolué depuis mes tests datant de 2011 (cf. le commentaire du product owner wope ci-dessous).

 - anciennement BKRender
 - Framework mobile HTML5 et JavaScript, plus un moteur de rendu.
 - Solution commerciale et payante.
 - **Un serveur de rendu** génère un fichier html adapté et optimisé au terminal qui l’appelle.
 - ~~Les applications ont un rendu de site web, pas d’animations entre écrans mais un chargement de la page.~~
 - ~~Grande compatibilité au détriment de l’expérience utilisateur.~~
 - Permet de packager des applications pour déploiement sur les stores (applications hybrides donc)

---------- 

{{< figure src="/img/developpement-dapplications-mobiles-multiplateformes/multi_zepto.jpg" alt="Zepto.js" >}}

 - Pour **optimiser les performances au besoin**, il peut être intéressant de mettre une place une solution **hybride personnalisée**.
 - Phonegap peut être utilisé pour **prototyper**, on écrira ensuite le code natif dont on a besoin (et pas plus).
 - Les ponts JavaScript <-> SDK natif ne sont pas très compliqués à développer (chaque plateforme mobile le permet).
 - Considérer l’utilisation de **[Zepto.js](http://zeptojs.com/)** à la place de jQuery (la syntaxe est la même). Zepto ne fonctionne que sur les navigateurs basés sur WebKit mais il est beaucoup plus léger. Les framework [XUI](http://xuijs.com/) et [QuoJS](http://quojs.tapquo.com/)
   sont d’autres alternatives crédibles.
 - On utilisera un **framework JavaScript MVC** tel que [BackBone.js](http://backbonejs.org/) ou [Angular](http://angularjs.org/) pour structurer le code, faciliter les tests et la maintenance.
 - De même on pourra utiliser une librairie de **templating JavaScript** telle que [ICanHaz.js](http://icanhazjs.com/) ou [Mustache](http://mustache.github.com/) .
 - De nombreuses micro-librairies Javascript permettent de gérer le scrolling et les gestures tactiles (QuoJS, iSCroll4, Mobile Boilerplate, Hammer.js, …).
 - Pour toutes ces librairies Javascript, on pourra trouver son bonheur sur le site [Microjs.com](http://microjs.com/)

---------- 

## Conclusion

 - Il n’y a pas de solution miracle, chaque technologie/solution a ses avantages et inconvénients.
 - Aucune technologie multiplateforme ne permet d’être aussi performante que le développement natif tout en ayant un look-and-feel natif.
 - Le choix d’une technologie doit être un compromis entre différents facteurs :
    - Budget disponible
    - Nombre de plateformes cibles
    - Performances désirées
    - Type d’application
    - Connaissances des équipes de développement
    - Présence souhaitée ou non sur les magasins d’applications / fréquence des mises à jour
    
----------    