---
layout: page
title: "Surgical Scheduling"
description: "Large Language Models · Operations Research"
img: assets/img/surgical-scheduling.gif
importance: 5
category: work
---

**Research project · University of Nottingham**

[View the code and project abstract on GitHub](https://github.com/Linyan0115/LLM-Based-Surgical-Scheduling-Optimization)

## Research Question

How can we turn written scheduling requirements into an operating-room schedule that accounts for case order, room availability, and equipment needs?

## Methodology

**Constraint extraction.** We used GLM-4 to extract scheduling requirements from surgical case descriptions and operating rules.

**Model formulation.** A chain-of-experts workflow organized the extracted requirements and translated them into a mixed-integer linear programming model.

**Schedule optimization.** We used CPLEX to solve the model, sequence cases, and allocate operating rooms and equipment.

<img src="{{ '/assets/img/surgical-scheduling.gif' | relative_url }}"
     class="img-fluid rounded"
     alt="Animated demonstration of the surgical scheduling workflow"
     loading="lazy">

*Visualization of the surgical scheduling workflow.*

## Results

In an evaluation with more than 1,000 surgical cases across 20 operating rooms, the system improved scheduling efficiency by 18% and decision speed by 20%.

In an evaluation with more than 1,000 surgical cases across 20 operating rooms, the system improved scheduling efficiency by 18% and increased decision speed by 20%.
