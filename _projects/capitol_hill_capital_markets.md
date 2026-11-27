---
layout: page
title: "On Persistence in Congressional Stock Selection"
description: Whether the same congressional households repeatedly select stocks that outperform, and how the return benchmark changes the answer.
importance: 1
related_publications: false

category: working_paper
hide_details: true # no detail page; the links below go to the paper and the code
sitemap: false
authors: Kirill Sirik
venue: Working paper (junior independent work), Princeton University
year: 2026
abstract_open: true
abstract: >-
  Do the same congressional households repeatedly pick stocks that outperform? For 7,964 purchases by 38 households,
  persistence from 2015–2020 to 2021–2025 is negative under a factor-only benchmark and positive under an event-study
  benchmark; neither estimate is statistically significant. The event-study benchmark carries forward recent alpha, the
  intercept of the stock's factor regression before the purchase. The positive estimate can reflect repeated
  underperformance: recent alpha barely predicts later returns (forecast coefficient 0.057, where the benchmark assumes
  one), yet the same households keep buying stocks with high recent alpha. Benchmarks carrying recent alpha forward
  should first be checked against later returns. A second question is what tests of average returns can say about one
  household. A clustered test of whether the pooled mean return is zero can miss an arbitrarily large gain to that
  household; for a household specified in advance making 50 purchases a year, detecting a 5 percent annual advantage
  would take about 74 years.
links:
  - name: Full paper (PDF)
    url: /papers/sirik-congressional-stock-selection-complete.pdf
  - name: Paper without appendix (PDF)
    url: /papers/sirik-congressional-stock-selection-main-text.pdf
  - name: Appendix (PDF)
    url: /papers/sirik-congressional-stock-selection-appendix.pdf
  - name: Repository
    url: https://github.com/kirillsirik/congressional-trading-persistence
---

<script>window.location.replace("{{ '/research/' | relative_url }}#{{ page.slug }}");</script>

See this entry on the [research page]({{ '/research/' | relative_url }}#{{ page.slug }}).
