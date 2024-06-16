---
layout: page
title: Résistance chauffante asservie
description: Réalisation et comparaison de l'asservissement numérique de la température d'une résistance chauffante
img: assets/img/projects/temperature_control_system/main.jpg
importance: 2
category: 2024
---

Durant le module "Interface puissance système" inclus dans mon semestre 7 au sein de l'ENIB, j'ai eu l'occasion de travailler sur un projet visant à réaliser l'asservissement en température d'une résistance chauffante ainsi que la comparaison de ses caractéristiques avec un modèle théorique que nous avons réalisé. Il a donc été ici question de traiter : la modélisation théorique du système thermodynamique, sa simulation (en boucle ouverte et boucle fermée par un correcteur), identification expérimentale des paramètres thermiques du système. Et enfin une comparaison entre les résultats théoriques et expérimentaux.

Ma tâche durant ce projet de groupe aura essentiellement consisté à réaliser le circuit électronique puis les plans du circuit imprimé au format shield arduino permettant de faire l'interface entre la partie de puissance du système (résistance chauffante et thermistance) et la partie numérique (STM32). Mais j'ai également fourni une grande aide dans la partie de modélisation de l'équation différentielle du système puis la simulation du système en boucle ouverte et fermée ainsi que dans le code afin d'interpréter le résultat des capteurs.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/temperature_control_system/0.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/temperature_control_system/1.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>