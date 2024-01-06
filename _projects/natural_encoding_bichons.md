---
layout: page
title: Bichons
description: Synthèse d'images en Python
img: assets/img/projects/natural_encoding_bichons/main.jpg
importance: 5
category: 2022
---

Durant mon semestre 4 au sein de l'ENIB, dans le cadre de la matière dédiée au espace euclidien, à la suite du projet "Reconnaissance sonore" que vous pouvez retrouver sur ce site, mes collègues et moi avons eu l'occasion de travailler sur un projet faisant usage d'une base de "bichons" (ensemble de photo de chien et de chat). Avec cette base, il a été question de réaliser une image "synthétique" à partir d'une image d'origine choisis.

Pour cela, nous avons exprimé notre image dans un espace euclidien ayant pour
base la base de "bichons" (ensemble de photo de chien et de chat) qui a été rendu au préalable orthonormale. Cela a été possible en utilisant le produit scalaire associé à l'espace en question pour projeter la photo à synthétiser sur la base.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/natural_encoding_bichons/main.jpg" class="img-fluid rounded z-depth-1" caption="Image d'origine" %}
    </div>
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.html path="assets/img/projects/natural_encoding_bichons/1.jpg" class="img-fluid rounded z-depth-1" caption="Synthétisation de l'image à l'aide de 200 bichons" %}
    </div>
</div>
