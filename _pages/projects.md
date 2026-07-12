---
layout: page
title: projects
permalink: /projects/
description: A selection of course projects and research group work from my undergraduate studies. Each card links to a full description, with code and reports where available.
nav: true
nav_order: 2
horizontal: true
---

<!-- pages/projects.md -->
<div class="projects">

{% assign sorted_projects = site.projects | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
</div>
