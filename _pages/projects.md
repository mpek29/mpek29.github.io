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
  <nav id="navbar" class="navbar navbar-light navbar-expand-sm">
    <div class="container">
      <div class="collapse navbar-collapse text-right" id="navbarNav">
        <ul class="navbar-nav ml-auto flex-nowrap">
          <!-- Categories -->
          {%- for category in page.display_categories %}
          <li class="nav-item ">
            <nobr><a class="nav-link">{{ category }}</a></nobr>
          </li>
          {%- endfor %}
        </ul>
      </div>
    </div>
  </nav>

  <!-- Generate cards for each project -->
  {%- assign categorized_projects = site.projects | where: "category", category -%}
  <div class="grid">
    {%- for project in categorized_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
</div>
