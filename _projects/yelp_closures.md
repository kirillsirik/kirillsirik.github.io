---
layout: page
title: Predicting Business Closures with the Yelp Open Dataset
description: Leakage-aware machine learning on 150k businesses and ~7M reviews — classical models vs. neural networks
img: assets/img/proj_yelp.png
importance: 3
related_publications: false
---

Using the Yelp Open Dataset (150,346 businesses, ~7M reviews across 11 metropolitan areas), this project asks two questions: can we predict whether a business closes after a cutoff date *T*, and — for businesses that survive — can we predict their average post-*T* star rating?

The design is strictly **leakage-aware**: every feature is computed only from information dated on or before *T* = 2020-12-31, and Yelp's own pre-aggregated fields are discarded and recomputed from pre-*T* data.

Highlights:

- MLP-2 achieves the best closure-classification ROC-AUC (0.879) and PR-AUC (0.716); random forest is the strongest classical model and wins the star-rating regression (R² ≈ 0.53).
- Customer-engagement features dominate: REVIEW-derived features alone reach ROC-AUC 0.862, vs. 0.607 for geography and 0.704 for business attributes.
- Businesses whose last pre-*T* review is over a year old close at a 44% rate, vs. 3% for businesses reviewed within 30 days — a ~15× difference.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/proj_yelp.png" title="Closure rate by recency of last review" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Closure rate rises roughly 15-fold as the last pre-cutoff review ages from under 30 days to over a year.
</div>

**Links:** [code & report on GitHub](https://github.com/kirillsirik/Yelp-Open-Dataset-Project) · [full report (PDF)](https://github.com/kirillsirik/Yelp-Open-Dataset-Project/blob/main/report/SML301_Final_Project.pdf)
