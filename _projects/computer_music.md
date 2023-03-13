---
layout: page
title: Mini logiciel de MAO
description: Synthétisation d'une musique en Rust
img: assets/img/projects/computer_music/main.jpg
importance: 2
category: Programmation informatique(Python - Rust - Unity C# - Kotlin - SQLite3)
---

Dans le cadre de notre cours de programmation, nous avons réalisé un projet de mini-logiciel de mao répondant à 2 objectifs :

- Insister sur la démarche de mise en œuvre afin de tendre vers des pratiques (consulter la documentation, utiliser un analyseur de code, tester le code, produire de la documentation...) qui sont courantes dans le milieu professionnel.

- Comprendre le cycle de vie des données manipulées dans un programme : la création, la destruction, la consommation, la recopient, l'accès en consultation, l'accès en modification...

Le principal objectif de ce projet était de réaliser une musique à partir d'une partition au format JSON chose que j'ai réussi ! Néanmoins, durant la phase final consistant à faire usage d'un fichier MIDI (bien plus courant dans le milieu de la MAO), je n'ai pu finaliser totalement le projet.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/computer_music/1.jpg" class="img-fluid rounded z-depth-1" caption="Génération d'une sinusoïde simple" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/computer_music/2.jpg" class="img-fluid rounded z-depth-1" caption="Production d'une note pour un instrument donné" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/computer_music/3.jpg" class="img-fluid rounded z-depth-1" caption="La musique Child_In_Time générée par le projet" %}
    </div>
</div>
