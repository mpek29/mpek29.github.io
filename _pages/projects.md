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
  <nav class="nav-proj" role="tablist">
    {%- for category in page.display_categories %}
    <button class="nav-btn" type="button" id="cardHover" aria-label="Open All" aria-current="All">{{ category }}</button>
    {%- endfor %}
  </nav>
  <!-- Generate cards for each project -->
  {%- assign categorized_projects = site.projects | where: "category", category -%}
  <div class="grid">
    {%- for project in categorized_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
</div>
