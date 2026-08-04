---
layout: page
title: research
permalink: /research/
description: Working papers, research group work, and course projects from my undergraduate studies, with code and reports where available.
nav: true
nav_order: 1
---

{% assign sorted = site.projects | sort: "importance" %}
{% assign working_papers = sorted | where: "category", "working_paper" %}
{% assign research_items = sorted | where: "category", "research" %}
{% assign course_items = sorted | where: "category", "course" %}

<div class="research-list">

{% if working_papers.size > 0 %}

<h2 class="section-heading">Working papers</h2>

{% for entry in working_papers %}{% include research_entry.liquid entry=entry %}{% endfor %}

{% endif %}

{% if research_items.size > 0 %}

<h2 class="section-heading">Research group work</h2>

{% for entry in research_items %}{% include research_entry.liquid entry=entry %}{% endfor %}

{% endif %}

{% if course_items.size > 0 %}

<h2 class="section-heading">Course projects</h2>

<p class="section-note">These projects were completed as part of undergraduate coursework at Princeton University.</p>

{% for entry in course_items %}{% include research_entry.liquid entry=entry %}{% endfor %}

{% endif %}

</div>
