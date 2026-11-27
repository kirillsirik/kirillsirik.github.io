---
layout: page
title: research
permalink: /research/
description: Working papers, works in progress, research group work, and course projects from my undergraduate studies, with code and reports where available.
nav: true
nav_order: 1
---

{% assign sorted = site.projects | sort: "importance" %}
{% assign working_papers = sorted | where: "category", "working_paper" %}
{% assign in_progress = sorted | where: "category", "in_progress" %}
{% assign research_items = sorted | where: "category", "research" %}
{% assign course_items = sorted | where: "category", "course" %}

<div class="research-list">

{% if working_papers.size > 0 %}

<h2 class="section-heading">Working papers</h2>

{% for entry in working_papers %}{% include research_entry.liquid entry=entry %}{% endfor %}

<div class="research-entry">
  <h3 class="research-title">Hotel Concentration and Local News Coverage of Short-Term Rentals</h3>
  <p class="research-meta">
    <span class="research-authors"><strong>Kirill Sirik</strong>.</span>
    <span class="research-venue"><em>Working paper, Princeton University</em>, 2026.</span>
  </p>
  <details class="research-abstract" open>
    <summary>Abstract</summary>
    <p>Consolidation can strengthen incumbents' incentives to seek restrictions on entrants. I study whether the 2016 hotel acquisitions, chiefly Marriott's purchase of Starwood, changed local newspaper coverage of short-term rentals. Among 326,251 news articles from 613 U.S. cities, a language model identifies 283 about short-term rentals, and this coverage rises sharply when a city first regulates them. Coverage did not grow more where the acquisitions raised hotel concentration more, which gives no indication that consolidation led hotels to make their case against short-term rentals through local newspapers. With controls for pre-merger concentration, size, news volume, and Airbnb presence, the 95 percent confidence intervals rule out increases in coverage of short-term rentals, and in coverage opposing them, larger than about a tenth of their post-merger means for each 100 points that the acquisitions added to a city's HHI. The bound is looser where the acquisitions added 100 points or more. Across cities, coverage appears to rise with exposure once pre-merger concentration is held fixed, but when the larger pre-merger Airbnb presence of exposed cities is also held fixed, the rise disappears.</p>
  </details>
  <p class="research-links">
    <a href="/papers/sirik-hotel-concentration-news-coverage-full.pdf" target="_blank" rel="noopener noreferrer">Full paper (PDF)</a
    ><span class="research-sep">&middot;</span
    ><a href="/papers/sirik-hotel-concentration-news-coverage-main-text.pdf" target="_blank" rel="noopener noreferrer">Paper without appendix (PDF)</a
    ><span class="research-sep">&middot;</span
    ><a href="/papers/sirik-hotel-concentration-news-coverage-appendix.pdf" target="_blank" rel="noopener noreferrer">Appendix (PDF)</a
    ><span class="research-sep">&middot;</span
    ><a href="https://github.com/kirillsirik/hotel-concentration-news-coverage" target="_blank" rel="noopener noreferrer">Repository</a>
  </p>
</div>

{% endif %}

{% if in_progress.size > 0 %}

<h2 class="section-heading">Works in progress</h2>

{% for entry in in_progress %}{% include research_entry.liquid entry=entry %}{% endfor %}

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
