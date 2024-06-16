---
layout: page
title: Synthétiseur numérique
description: Réalisation d'un oscillateur numérique et de plusieurs filtres numériquess
img: assets/img/projects/digital_synthesizer/main.jpg
importance: 3
category: 2024
---

Durant le module "Traitement des signaux et des images" inclus dans mon semestre 7 au sein de l'ENIB, j'ai eu l'occasion de travailler sur un projet visant à programmer un microcontrôleur STM32 afin de concevoir un synthétiseur numérique à synthèse soustractive.

Voici comment fonctionne la sythèse soustrative :
- On génère un signal riche en harmoniques ( de type triangle / dent de scie / rectangle ). La fréquence fondamentale de ce signal dépend de la note saisie au clavier.
- On applique un filtre passe-bas sur ce signal afin de soustraire des harmoniques, et donc de sculpter le son. La fréquence de coupure de ce filtre doit dépendre de la note saisie au clavier.

L'ensemble des données du clavier sont transmise via USB et grâce au protocole midi à la carte.

Il aura donc été question ici de réaliser un oscillateur numérique puis d'appliquer mes connaissances théoriques sur les filtres FIR et FII à travers le calcul des coefficients propre à ces deux types de filtres et l'application de ces coefficients sur le signal généré par l'oscillateur.