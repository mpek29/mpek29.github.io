---
layout: page
title: Bichons
description: Synthèse d'images en Python
img: assets/img/projects/natural_encoding_bichons/main.jpg
importance: 6
category: Programmation informatique(Python - Rust - Unity C# - Kotlin - SQLite3)
---

Le but de projet a été de travailler avec une base de "bichons" (ensemble de photo de chien et de chat) et de réaliser à l'aide de celle-ci une image "synthétique" de la première.

Pour cela, il a été question de représenter dans un espace euclidien notre photo d'origine. Cela a été possible en utilisant le produit scalaire associé à l'espace en question pour projeter la photo à synthétiser sur la une base de "bichons". Cette base de "bichons" aura servi ici de base vectorielle (il a été question de la rendre orthonormale notamment.).

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/natural_encoding_bichons/main.jpg" class="img-fluid rounded z-depth-1" caption="Image d'origine" %}
    </div>
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.html path="assets/img/projects/natural_encoding_bichons/1.jpg" class="img-fluid rounded z-depth-1" caption="Synthétisation de l'image à l'aide de 200 bichons" %}
    </div>
</div>
