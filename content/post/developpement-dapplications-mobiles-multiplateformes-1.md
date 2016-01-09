+++
title = "Développement d’applications mobiles multiplateformes (1/2)"
tags = [
    "mobile",
    "multiplatform",
    "development"
]
date = "2012-11-16"
description = "Avec la multiplication des plateformes mobiles, la question du développement multiplateforme s’est rapidement posée, afin de tenter de réduire les coûts de développement."
+++

Avec la **multiplication des plateformes mobiles**, la question du développement multiplateforme s’est rapidement posée, afin de tenter de réduire les coûts de développement.

Dans la première partie de cet article je vais décrire les différentes techniques pour cette mutualisation des développements, ainsi que leurs limitations

Dans le billet suivant je présenterai les principales solutions open sources ou commerciales existantes.

A ce jour on peut rencontrer **4  techniques pour le développement multiplateformes** :

 - Cross-compilation en code natif
 - Développement bas niveau
 - Développement web – hybride
 - Application web sur un serveur de rendu optimisé pour mobile

A noter que beaucoup de solutions multiplateformes mélangent plusieurs de ces différentes approches pour essayer de tirer le meilleur parti de chacune.

## 1 – Approche native

 - Cette première technique consiste à utiliser les composants natifs des plateformes mobiles, via une API et un langage de programmation unique.
 - Un **cross-compiler** permet ensuite de compiler le code en application native. Il est également possible de faire exécuter ce code sur une machine virtuelle embarquée dans une application native.
 - Ces techniques permettent d’avoir des **performances optimales** (si compilation en binaires natifs), et un rendu natif de l’IHM, mais sont souvent limitées par le plus petit dénominateur commun entre les différentes plateformes.

## 2 – Approche bas niveau

 - Cette technique consiste à dessiner des composants graphiques avec des langages et librairies bas niveau comme le couple **C++/OpenGL**, dans le but de bénéficier de performances maximales.
 - Cela est possible sur la majorité des plateformes mobiles (iOS, Android, Windows Phone).
 - L’inconvénient de cette approche est de perdre la facilité d’utilisation des widgets natifs, et surtout leur identité visuelle. En effet chaque plateforme mobile possède son propre look-and-feel et ses mécanismes d’interactions avec l’utilisateur.
 - Cette approche est donc le plus souvent utilisée pour le développement de **jeux vidéos**, plutôt que pour des projets plus classiques type applications d’entreprises.

## 3 – Approche web

 - Cette troisième (et principale) approche se base sur le **navigateur web embarqué** pour les composants visuels en HTML5, et un accès via JavaScript aux fonctionnalités natives.
 - On parle alors d’**applications hybrides**, une « coque » native embarquant alors des vues web.
 - Différents frameworks JavaScript (optimisés pour le mobile ou non) peuvent être utilisés pour mettre en place de telles solutions.
 - Les deux facteurs problématiques sont ici la **compatibilité HTML5** du navigateur embarqué qui peut être plus ou moins bonne, et la **perte de performances** par rapport à une application native qui est souvent importante.

## 4 – Serveur de rendu

 - Cette dernière approche se base sur un serveur hébergeant un **moteur de rendu** afin d’optimiser l’affichage d’une application web sur mobile, à la manière des navigateurs Opera Mobile et Opera Mini.
 - Nécessite de faire tourner l’application sur **un serveur web**, plus le moteur de rendu 
 - Le moteur de rendu doit s’adapter aux différentes plateformes clientes
 - Cette technique s’appuie également sur le navigateur web embarqué et est donc complémentaire de la troisième approche.
 - Chaque page est rendue séparément, il n’y a pas d’animations entre
   écrans