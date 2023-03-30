---
layout: page
title: EN COURS Pont en H
description: Contrôleur moteur pour voiture télécommandée
img: assets/img/projects/h_bridge/main.jpg
importance: 2
category: Elec. Analogique
---

Comme vous le savez probablement, afin de contrôler un moteur DC par microcontrôleur, il est possible d'utiliser un circuit intégré spécialement conçu à cette fin, comme le populaire L293D. Mais la construction d'un pont en H par ses propres moyens est très aisée et me permettait ici de réutiliser des composants de la carte électronique d'origine de la voiture télécommandée dont je souhaite refaire l'électronique embarquée.


## Pourquoi utiliser un contrôleur de moteur (pont en H)
Mais oui, on pourrait simplement brancher le moteur sur les broches du microcontrôleur, nan ?? Et non !
Plusieurs raisons nous amène à penser que c'est un mauvais choix:
- Protéger l'Arduino (puisque la résistance de l'Arduino est faible, on peut faire l'hypothèse que le courant demandé en cas d'utilisation du 5V par une Arduino serait bien trop élévé pour celle-ci).
- Le moteur en ralentissant pourrait créer du courant (effet de génératrice)
- Une tension supérieure au 5V proposé par un microcontrôleur est souvent nécessaire

## Pourquoi faire le choix d'un pont en H
L'utilisation d'un seul transistor peut suffire si vous désirez que votre moteur tourne toujours dans la même direction.

Mais ce n'est pas toujours le cas ! On veut bien souvent que notre moteur tourne dans une direction, et parfois dans l'autre (par exemple:  une voiture télécommandée qui avance puis recule).  Et c'est à partir de ce moment qu'un pont en H devient incontournable.

Voici un schéma de pont en H constitué de 4 transistors (2 PNP et 2 NPN) :

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/h_bridge/1.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

## Source
- <http://electroniqueamateur.blogspot.com/2016/04/fabriquons-notre-propre-pont-en-h.html>
