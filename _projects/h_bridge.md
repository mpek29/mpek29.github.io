---
layout: page
title: Pont en H
description: Contrôleur moteur pour voiture télécommandée
img: assets/img/projects/h_bridge/main.jpg
importance: 2
category: Elec. Analogique
---

## Introduction
Comme vous le savez probablement, pour contrôler un moteur à courant continue par microcontrôleur, il est possible d'utiliser un circuit intégré spécialement conçu à cette fin, comme le populaire L293D. Mais la construction d'un pont en H par ses propres moyens est très aisée et peux permettre d'utiliser des composants de récupération.

Dans ce projet, nous allons réaliser un pont en H afin de permmettre à un micontrôleur de provoquer la rotation d'un moteur et d'en choisir le sens.
La solution proposée au long de cette page consistera à :
- Découvrir ce qu'est un pont en H et son fonctionnement
- Réaliser le dimensionnement du pont en H
- Faire un test sur LTspice XVII
- Faire un test en réel sur breadboard à La Forge de l'[ENIB](https://www.enib.fr/fr/)

## Qu'est ce qu'un pont en H et comment ça fonctionne

### Le pont en H
Vous vous êtes probablement réveillé une jour en vous disant mais oui, je peux simplement brancher mon moteur à courant continue sur les broches du microcontrôleur de mon contrôlleur, c'est si simple! Et bien nan !
Plusieurs raisons nous amènent à penser que c'est un mauvais choix :
- Protéger l'Arduino (puisque la résistance de l'Arduino est faible, on peut faire l'hypothèse que le courant demandé en cas d'utilisation du 5V par une Arduino serait bien trop élevé pour celle-ci.).
- Le moteur en ralentissant pourrait créer du courant(effet de génératrice). 
- Une tension supérieure aux 5V proposés par un microcontrôleur est souvent nécessaire pour obtenir une vitesse de rotation convenable.
- Avec un pont en H notre moteur peut tourner dans une direction, et parfois dans l'autre (Par exemple : une voiture télécommandée qui avance puis recule ).

### Fonctionnement
Voici un schéma de pont en H constitué de 4 transistors (2 PNP et 2 NPN) :

{% include figure.html path="assets/img/projects/h_bridge/1.jpg" class="img-fluid rounded z-depth-1" %}

Lorsque la tension de la pin 6 de l'Arduino est de 5 V et que la tension de la pin 5 est nulle, les transistors Q1 et Q3 forment un trajet conducteur et le courant circule vers la droite dans le moteur.

{% include figure.html path="assets/img/projects/h_bridge/1.jpg" class="img-fluid rounded z-depth-1" %}

Si on inverse la polarité, ce sont les deux autres transistors qui deviennent conducteurs, et le courant circule maintenant vers la gauche dans le moteur.

{% include figure.html path="assets/img/projects/h_bridge/1.jpg" class="img-fluid rounded z-depth-1" %}

On ajoute des diodes afin de protéger le microcontrôleur contre les courants générés par la rotation du moteur.

{% include figure.html path="assets/img/projects/h_bridge/1.jpg" class="img-fluid rounded z-depth-1" %}


## Tester un pont en H
On peut aisément tester ce montage à l'aide de 2 interrupteurs actionnant du 5V.
Ces 2 interrupteurs viennent symbolisant la sortie d'un microcontrôleur placée au 0v ou à 5V.


## Conclusion

Bien qu'aujourd'hui un module à base de L298N puisse remplir la même fonction avec un coût proche de 3€, réaliser un pont en H peut être une bonne façon d'économiser de l'argent, mais aussi des ressources dont notre planète commence à manquer si jamais vous posséder une carte composant déjà des composants. Ici, j'ai utilisé ceux que j'avais à l'origine sur une carte de commande d'une voiture télécommandée.

## Source
- <http://electroniqueamateur.blogspot.com/2016/04/fabriquons-notre-propre-pont-en-h.html>
