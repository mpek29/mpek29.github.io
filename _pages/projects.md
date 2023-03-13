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
    
  </ul>

  <nav id="navbar" class="navbar navbar-light navbar-expand-sm fixed-top">
    <div class="container">
      <a class="navbar-brand title font-weight-lighter" href="/"><span class="font-weight-bold">PASCO&nbsp;</span>Florian</a>
      <!-- Navbar Toggle -->
      <button class="navbar-toggler collapsed ml-auto" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="sr-only">Toggle navigation</span>
        <span class="icon-bar top-bar"></span>
        <span class="icon-bar middle-bar"></span>
        <span class="icon-bar bottom-bar"></span>
      </button>
      <div class="collapse navbar-collapse text-right" id="navbarNav">
            <ul class="navbar-nav ml-auto flex-nowrap">
              <!-- Categories -->
              {%- for category in page.display_categories %}
              <li class="nav-item ">
                <a class="nav-link">{{ category }}</a>
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
