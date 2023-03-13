---
layout: page
title: Projets
permalink: /projects/
description: Voici une liste des projets que j'ai réalisé ou auquel j'ai participé.
nav: true
nav_order: 2
display_categories: [C/C++, Python, Elec. analogique, SQLite3, Qt, Java, Kotlin, Rust, Elec. numérique, Conception méca. (CAO)]
---
<!-- pages/projects.md -->
<div class="projects">
  <h2 class="category">{{ category }}</h2>

  <ul class="navbar-nav ml-auto flex-nowrap">
    <!-- Categories -->
    {%- for category in page.display_categories %}
    <li class="nav-item ">
      <a class="nav-link">{{ category }}</a>
    </li>
    {%- endfor %}
  </ul>

  <!-- Generate cards for each project -->
  {%- assign categorized_projects = site.projects | where: "category", category -%}
  <div class="grid">
    {%- for project in categorized_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
</div>
