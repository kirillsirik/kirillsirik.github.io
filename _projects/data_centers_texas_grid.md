---
layout: page
title: Data Centers Will Strain the Texas Grid (Even with Demand Response)
description: First-authored ORFEUS study simulating 22 GW of projected data-center load on a 7,000-bus Texas grid — with Alex Crosier and Ronnie Sircar
img: assets/img/proj_datacenters.png
importance: 1
related_publications: false
---

ERCOT forecasts that Texas data centers will demand **22 GW by 2030**, up from around 1 GW today. In this study — published by Princeton's [ORFEUS group](https://orfeus.princeton.edu/) with Alex Crosier and Ronnie Sircar — we ask what that load does to the grid, and whether demand response can soften the blow.

We geolocated **350 Texas data centers** and allocated ERCOT's April 2025 adjusted load forecast across them, then simulated a full year (8,760 hours) of grid operation on a 7,000-bus synthetic Texas grid with 50% renewable generation, solving two-day-ahead unit-commitment and economic-dispatch problems in [Vatic](https://github.com/PrincetonUniversity/Vatic) (built on LLNL's Prescient) with a 15% reserve requirement.

Key findings:

- Adding 22 GW of data-center load raises average wholesale prices from **$21.18/MWh to $31.47/MWh — a 49% increase** — and average total system costs from **$1.4M to $74.5M per hour**, driven largely by load shedding, which jumps from 4 MW to an average of **724 MW per hour**. Without additional supply, the system simply cannot absorb the projected load.
- A **0.5%-curtailment demand-response scheme** (each data center offline at most 44 hours per year, shedding up to half its load) deploys in the 72 tightest hours of the year and **cuts total system costs by about 57% during those hours**, while reducing peak demand by about 7%.
- But because those hours are less than 1% of the year, annual average system costs remain high at **$71.0M per hour** — demand response helps at the peaks, yet is no substitute for new supply.

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/proj_datacenters.png" title="Nodal electricity prices with and without 22 GW of data-center load" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Nodal price map of the simulated 2030 Texas grid at one hour on July 18, 2030: baseline (left) vs. 22 GW of added data-center load (right). Figure from the ORFEUS study.
</div>

**Links:** [full study on ORFEUS](https://orfeus.princeton.edu/data-centers-will-strain-grid-even-demand-response.html)
