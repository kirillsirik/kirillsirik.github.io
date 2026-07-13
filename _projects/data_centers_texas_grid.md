---
layout: page
title: Data Centers Will Strain the Texas Grid (Even with Demand Response)
description: A study of how 22 GW of projected data center load would affect prices, costs, and reliability on the Texas grid. Project done in collaboration with Alex Crosier and Ronnie Sircar. Published on the ORFEUS research group at Princeton University.
img: assets/img/proj_datacenters.png
importance: 1
badge: Research group study
related_publications: false
---

<span class="project-badge">Research group study</span>

Electric Reliability Council of Texas (ERCOT) forecasts that data centers in Texas will demand 22 GW of electricity by 2030, up from roughly 1 GW today. This study, written with Alex Crosier and Ronnie Sircar and published by the [ORFEUS group](https://orfeus.princeton.edu/), examines how that projected load increase would affect prices, costs, and reliability on the Texas grid, and to what extent demand response can mitigate the effects inflicted by said load increase.

We geolocated 350 Texas data centers and allocated the projected load from ERCOT's April 2025 adjusted load forecast across them. We then simulated a full year (8,760 hours) of grid operation on a synthetic Texas grid with 7,000 buses and 50% renewable generation, solving unit commitment and economic dispatch problems in [Vatic](https://github.com/PrincetonUniversity/Vatic) with a two day ahead forecast horizon and a 15% reserve requirement.

Main findings:

- Adding 22 GW of data center load raises average wholesale prices from $21.18/MWh to $31.47/MWh, an increase of 49%. Average total system costs rise from $1.4 million to $74.5 million per hour, driven largely by load shedding, which increases from 4 MW to an average of 724 MW per hour.
- A demand response scheme with 0.5% curtailment, under which each data center is offline at most 44 hours per year and sheds at most half of its load, deploys in the 72 tightest hours of the year. It reduces total system costs by about 57% during those hours and lowers peak demand by about 7%.
- Because those hours account for less than 1% of the year, annual average system costs remain at $71.0 million per hour. Although demand response helps mitigate the most severe hours, it does fully replace the need for additional supply.

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/proj_datacenters.png" title="Nodal electricity prices with and without 22 GW of data center load" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Nodal price map of the simulated 2030 Texas grid at one hour on July 18, 2030: the baseline case (left) and the case with 22 GW of added data center load (right). Figure from the study.
</div>

**Links:** [full study on ORFEUS](https://orfeus.princeton.edu/data-centers-will-strain-grid-even-demand-response.html)
