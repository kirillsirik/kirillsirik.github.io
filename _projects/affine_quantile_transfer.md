---
layout: page
title: "Affine Transfer for Conditional Quantiles with Heavy-Tailed Responses"
description: An affine correction that transfers a fitted nonlinear quantile regression to a target population with few labeled observations.
importance: 0
related_publications: false

category: working_paper
hide_details: true # no detail page
sitemap: false
authors: Kirill Sirik
venue: Senior thesis, Princeton University
year: 2026
abstract_open: true
abstract: >-
  A small target sample may not support a rich quantile regression even when a larger sample from a related source
  population does. We fit the target quantile as an affine function of a fitted source quantile, principal-component
  scores, and selected covariates. We prove a finite-sample bound on squared prediction error that separates affine
  approximation, input estimation, and target estimation errors. Under boundedness and density conditions, its target
  term has order $k \log n / n$ for $k$ coefficients and $n$ target responses, and no response moments are required.
  Sharing one slope across several quantile levels is a second restriction that, like transfer, saves variance at the
  risk of bias. Under standard Cauchy errors, for which the least-squares slope has no finite variance, a slope shared
  by the three quartiles has 58% less asymptotic variance than the slope of a separate fit at an outer quartile. For
  local scale departures, in which the spread of the response changes with the inputs by an amount that shrinks like
  $n^{-1/2}$, we identify the boundary where the squared bias of sharing offsets the variance it saves. For three
  quartiles, in the cases we tabulate, the 5% joint test of equal slopes that one would run before sharing has limiting
  power 0.14–0.53 at the outer-quartile boundary, so nonrejection does not establish a prediction advantage for sharing.
  In 2024 American Community Survey data, we transfer the 0.90 quantile of income from California to the eight least
  populous states. With $n = 100$ labeled records per state, transfer lowers mean held-out check loss by 16.8–21.6%
  relative to target-only regression. Against target-only regression on the same scores and covariates, without the
  source prediction, the reduction is 1.9–10.2% and persists at larger $n$.
links:
  - name: Full paper (PDF)
    url: /papers/sirik-affine-quantile-transfer-full.pdf
  - name: Paper without appendix (PDF)
    url: /papers/sirik-affine-quantile-transfer-main-text.pdf
  - name: Appendix (PDF)
    url: /papers/sirik-affine-quantile-transfer-appendix.pdf
  - name: Repository
    url: https://github.com/kirillsirik/affine-quantile-transfer
---

<script>window.location.replace("{{ '/research/' | relative_url }}#{{ page.slug }}");</script>

See this entry on the [research page]({{ '/research/' | relative_url }}#{{ page.slug }}).
