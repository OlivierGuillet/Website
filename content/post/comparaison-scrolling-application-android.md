+++
title = "Natif, hybride, web app : comparaison des méthodes de scrolling sur application Android"
tags = [
    "mobile",
    "web",
    "development"
]
date = "2012-01-10"
description = "Un pattern récurrent dans les applications mobiles consiste à afficher une liste d’items, avec éventuellement un header et/ou un footer fixe, la liste étant scrollable entre ce header et ce footer."
+++

Un pattern récurrent dans les applications mobiles consiste à afficher une liste d’items, avec éventuellement un header et/ou un footer fixe, la liste étant scrollable entre ce header et ce footer.
En code Android natif cela est très facile à mettre en place avec deux TextView et une simple ListView, mais en HTML pour un site mobile ou une webapp cela peut se compliquer.

En effet, cela devrait se faire facilement en HTML5 en positionnant le header et le footer en **position:fixed**, et en faisant scroller la liste avec une propriété CSS **overflow:scroll**.
**Problème** : bien que les navigateurs Android et iOS soient basés sur le moteur WebKit, ils ne supportaient pas ces propriétés jusque récemment. Leur support est apparu avec **iOS en version 5.0 et Android en version 2.2**

Plusieurs librairies javascript ont donc été développées pour apporter ce positionnement fixe et ce scrolling des listes, en imitant le **scrolling inertiel natif** des systèmes Android et iOS. Nous allons donc tester les plus matures :

 - la plus connue, la librairie iScroll de Matteo Spinelli
 - Scrollability, la librairie développé par Joey Hewitt, ancien employé
   chez Facebook et développeur à la fois de l’application pour Iphone
   et de l’application web mobile
 - la librairie TouchSCroll de David Aurelio

**Pour tester cela j’ai fait une petite appli Android présentant 6 écrans :**

 1. ListView native Android
 2. LinearLayout comprenant un header et un footer natif, et une liste d’items HTML dans une WebView entre les deux ( solution hybride, c’est le système Android qui gère le scroll)
 3. WebView appelant une page HTML5, le scrolling est géré en CSS3
 4. WebView appelant une page HTML5, le scrolling est géré par la librairie Javascript iScroll4
 5. WebView appelant une page HTML5, le scrolling est géré par la librairie Javascript Scrollability
 6. WebView appelant une page HTML5, le scrolling est géré par la librairie Javascript TouchSCroll

La démo est disponible sur [Android Market](http://goo.gl/G3VKl).

Les tests iPhone ont été fait en appelant directement les pages de tests suivantes :

 - [HTML5 / CSS3](http://goo.gl/82L29)
 - [iScroll4](http://goo.gl/J5rLX)
 - [Scrollability](http://goo.gl/CF4ob)
 - [TouchScroll](http://goo.gl/2wbce)

---------- 
 
Voici le résultat des tests sur cette appli :

|               	| Android 2.3.4 (ZTE Blade)                                                                                                                                                                           	| iOS 5.0.1 (iPhone3GS)                                                                                                                                                                                        	| iOS 4.2.1 (iPhone3G)                                                              	|
|---------------	|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|-----------------------------------------------------------------------------------	|
| Natif         	| très rapide<br>     bonne inertie du scrolling<br>     pas de rebond en fin de scroll                                                                                                               	|                                                                                                                                                                                                              	|                                                                                   	|
| ScrollView    	| très rapide<br>     bonne inertie du scrolling<br>     pas de rebond en fin de scroll                                                                                                               	|                                                                                                                                                                                                              	|                                                                                   	|
| HTML5         	| scrolling et inertie   OK<br>     les scrollbars apparaissent sur tout l'écran<br>     la liste ne s'arrête pas en haut du footer mais passe sous   celui-ci<br>     pas de rebond en fin de scroll 	| scrolling OK<br>     les scrollbars apparaissent sur tout l'écran<br>     la liste ne s'arrête pas en haut du footer mais passe sous   celui-ci<br>     peu d'inertie<br>     pas de rebond en fin de scroll 	| footer non fixe !                                                                 	|
| iScroll4      	| scrolling et inertie   OK<br>     rebond en fin de scroll OK                                                                                                                                        	| scrolling et inertie   OK<br>     rebond en fin de scroll OK                                                                                                                                                 	| scrolling et inertie   OK<br>     rebond en fin de scroll OK                      	|
| Scrollability 	| aucune   inertie<br>     scrolling saccadé                                                                                                                                                          	| scrolling et inertie   OK<br>     rebond en fin de scroll OK                                                                                                                                                 	| scrolling et inertie légèrement   saccadés<br>     rebond en fin de scroll OK     	|
| TouchScroll   	| scrolling et   inertie OK<br>     pas de rebond en fin de scroll                                                                                                                                    	| scrolling et inertie   OK<br>     pas de rebond en fin de scroll                                                                                                                                             	| scrolling et inertie légèrement   saccadés<br>     pas de rebond en fin de scroll 	|
La bonne surprise est la librairie **iScroll4** qui est la seule à fonctionner sur toutes les plateformes de test si on souhaite une compatibilité maximale. De plus elle permet d’autres fonctionnalités qu’un simple scrolling, notamment le "[pull to refresh](http://cubiq.org/dropbox/iscroll4/examples/pull-to-refresh/)".    
On pourra éventuellement détecter les versions des navigateurs, et utiliser iScroll uniquement si iOS<=4.0 ou Android<=2.2.  
Enfin à l'avenir on peut espérer que le couple HTML5/CSS3 fonctionnera correctement sur toutes les plateformes, et que l'on pourra se passer de ces librairies javascript.

---------- 

Codes sources disponibles sur GitHub:

 - [client Android](https://github.com/olivierguillet/Scroll-Demo-Android)
 - [pages HTML](https://github.com/olivierguillet/Scroll-Demo-HTML5)
 
--------- 