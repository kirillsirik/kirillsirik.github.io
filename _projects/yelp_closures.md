---
layout: page
title: Predicting Business Closures with the Yelp Open Dataset
description: Predicting business closures and future star ratings from 150,346 businesses and about 7 million reviews, comparing classical machine learning models with neural networks.
img: assets/img/proj_yelp.png
importance: 3
related_publications: false
---

This project uses the Yelp Open Dataset (150,346 businesses and about 7 million reviews across 11 metropolitan areas) to study two prediction problems: whether a business is closed after a cutoff date *T*, and, for businesses that remain open, what their average star rating is after *T*.

All features are computed from information dated on or before *T* = December 31, 2020. Yelp's own aggregate fields are discarded and recomputed from reviews dated before the cutoff in order to prevent information leakage. Classical models (logistic regression, a calibrated ridge classifier, decision trees, and random forests) are compared with feedforward neural networks under a shared preprocessing and evaluation pipeline.

Main findings:

- A two layer neural network achieves the best classification performance on the held out test set (ROC AUC of 0.879 and PR AUC of 0.716), while a random forest is the strongest classical model and performs best in the ratings regression (R² of about 0.53).
- Features derived from review activity carry most of the predictive signal. On their own they reach a ROC AUC of 0.862, compared with 0.607 for geographic features and 0.704 for business attributes.
- Businesses whose most recent review before the cutoff is more than a year old close at a rate of 44%, compared with 3% for businesses reviewed within the previous 30 days.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/proj_yelp.png" title="Closure rate by recency of the last review" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Closure rate by recency of the last review before the cutoff date. The closure rate rises from about 3% to about 44% as the most recent review ages from under 30 days to more than a year.
</div>

**Links:** [code and report on GitHub](https://github.com/kirillsirik/Yelp-Open-Dataset-Project) · [full report (PDF)](https://github.com/kirillsirik/Yelp-Open-Dataset-Project/blob/main/report/SML301_Final_Project.pdf)
