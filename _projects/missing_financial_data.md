---
layout: page
title: Missing Financial Data — Replication & Extension
description: Replication and frequency-split extension of Bryzgalova, Lerner, Lettau & Pelger (2024, Review of Financial Studies)
img: assets/img/proj_mfd.png
importance: 1
related_publications: false
---

This project replicates the core empirical findings of Bryzgalova, Lerner, Lettau & Pelger (2024), [*Missing Financial Data*](https://doi.org/10.1093/rfs/hhae036) (*Review of Financial Studies*), and extends their imputation methodology with a **frequency-split hyperparameter design**: separate latent dimension *K* and regularization *γ* for monthly versus quarterly firm characteristics, motivated by differences in signal dimensionality, persistence, and missingness structure.

Highlights:

- Replicated the paper's full imputation-method ranking on a truncated 2016–2020 panel (60 months, 22,351 permnos, 45 characteristics), with aggregate RMSEs within 0.01–0.02 of the published values.
- The frequency-split specification improves out-of-sample monthly RMSE by 2.8% in aggregate and 10.7–13.8% in interior volatility quintiles, and substantially improves out-of-sample IPCA Sharpe ratios — while leaving quarterly characteristics unchanged.
- Built-in correctness check: collapsing both frequency groups to the baseline hyperparameters reproduces the baseline results exactly.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/proj_mfd.png" title="Out-of-sample IPCA Sharpe ratios" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Out-of-sample IPCA Sharpe ratios by number of factors K: portfolios built on frequency-split imputations (green) recover much more of the fully-observed benchmark (orange) than the baseline imputation (blue).
</div>

**Links:** [code & report on GitHub](https://github.com/kirillsirik/missing-financial-data-replication) · [full report (PDF)](https://github.com/kirillsirik/missing-financial-data-replication/blob/main/report/ECO480_Final_Report_KS.pdf)
