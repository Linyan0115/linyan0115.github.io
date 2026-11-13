---
layout: page
title: "From Links to Lanes"
description: "Transportation Modeling · Traffic Assignment"
img: assets/img/lane-assignment.png
importance: 3
category: work
---

**Research project · 2025 INFORMS Annual Meeting**

[View the code and presentation slides on GitHub](https://github.com/Linyan0115/From-Links-to-Lanes-A-Lane-Level-Traffic-Assignment-Framework.)

## Research question

Two lanes on the same road can experience very different delays. A queue in a turn lane can spill back, and vehicles changing lanes can slow traffic in the receiving lane. We studied how explicitly modeling these movements changes estimates of congestion and route choice.

## Approach

We developed a lane-level traffic assignment framework that represents through movements, turns, and lane changes separately. Each maneuver has a travel-delay function that accounts for traffic in both the origin and receiving lanes.

{% include figure.liquid path="assets/img/lane-assignment.png" class="img-fluid rounded" alt="Diagram of lane-level traffic movements" %}

## Evaluation

We used microscopic SUMO simulations to evaluate the model and the Sioux Falls network to study its behavior on a benchmark network.
