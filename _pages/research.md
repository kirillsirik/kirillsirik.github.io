---
layout: page
title: research
permalink: /research/
description: Research group work and course projects from my undergraduate studies, with code and reports where available.
nav: true
nav_order: 1
---

{% assign sorted = site.projects | sort: "importance" %}
{% assign research_items = sorted | where: "category", "research" %}
{% assign course_items = sorted | where: "category", "course" %}

<div class="research-list">

{% if research_items.size > 0 %}

<h2 class="research-section">Research group work</h2>

{% for entry in research_items %}{% include research_entry.liquid entry=entry %}{% endfor %}

{% endif %}

{% if course_items.size > 0 %}

<h2 class="research-section">Course projects</h2>

<p class="research-section-note">Completed for undergraduate coursework at Princeton University. These are not peer reviewed research.</p>

{% for entry in course_items %}{% include research_entry.liquid entry=entry %}{% endfor %}

{% endif %}

</div>
