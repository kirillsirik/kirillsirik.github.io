---
layout: page
title: Replication and Extension of Missing Financial Data
description: Replication and frequency split extension of Bryzgalova, Lerner, Lettau and Pelger (2024, Review of Financial Studies). Undergraduate course project.
img: assets/img/proj_mfd.png
importance: 2
badge: Course project
related_publications: false
---

<span class="project-badge">Course project</span>

This project replicates the core empirical findings of Bryzgalova, Lerner, Lettau and Pelger (2024), [*Missing Financial Data*](https://doi.org/10.1093/rfs/hhae036) (*Review of Financial Studies*), and extends their imputation methodology with a frequency split design that assigns a separate latent dimension *K* and regularization *γ* to monthly and quarterly firm characteristics. The motivation is that the two groups differ in signal dimensionality, persistence, and missingness structure. This work was completed as an undergraduate course project at Princeton University.

Main findings:

- The replication reproduces the paper's full ranking of imputation methods on a truncated panel covering 2016 to 2020 (60 months, 22,351 permnos, 45 characteristics), with aggregate RMSEs within 0.01 to 0.02 of the published values.
- The frequency split specification improves monthly RMSE out of sample by 2.8% in aggregate and by 10.7% to 13.8% in interior volatility quintiles, and it improves out of sample IPCA Sharpe ratios, while leaving quarterly characteristics essentially unchanged.
- Setting both frequency groups to the baseline hyperparameters reproduces the baseline results exactly, which serves as a correctness check on the implementation.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/proj_mfd.png" title="Out of sample IPCA Sharpe ratios" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Out of sample IPCA Sharpe ratios by number of factors K. Portfolios built on frequency split imputations (green) recover more of the fully observed benchmark (orange) than portfolios built on the baseline imputation (blue).
</div>

**Links:** [code and report on GitHub](https://github.com/kirillsirik/missing-financial-data-replication) · [full report (PDF)](https://github.com/kirillsirik/missing-financial-data-replication/blob/main/report/ECO480_Final_Report_KS.pdf)
