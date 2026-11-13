---
layout: page
title: "Charging Optimization"
description: "Network Optimization · Facility Location"
img: assets/img/charging-placement.png
importance: 2
category: work
---

**Spring 2026 · CS 524 Final Project · UW–Madison**

[View the code on GitHub](https://github.com/Linyan0115/uw-madison-charging-optimization)

## The problem

Where should UW–Madison place portable charging kiosks so students can recharge along their daily walking routes? We studied how kiosk placement changes when we account for battery limits, installation costs, and coverage across different trip types.

## How we modeled it

We represented the campus as a pedestrian network with 20 buildings, 32 walking links, and 36 origin–destination pairs. We developed five optimization formulations, starting with shortest-path routing and extending to battery-aware, budget-constrained, and equity-aware placement. We implemented the models in Julia with JuMP and solved them with HiGHS.

{% include figure.liquid path="assets/img/charging-placement.png" class="img-fluid rounded" alt="Campus maps comparing optimal charging kiosk locations under four models" %}

*Optimal kiosk locations under four placement models.*

## What we found

Our recommended three-phase rollout uses five kiosks to cover all 36 modeled routes. The budget sensitivity analysis showed diminishing returns as coverage approached 100%.

{% include figure.liquid path="assets/img/charging-coverage.png" class="img-fluid rounded" alt="Route coverage as a function of the installation budget" %}

*Modeled route coverage as the installation budget increases.*
