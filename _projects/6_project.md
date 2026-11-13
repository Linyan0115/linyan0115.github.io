---
layout: page
title: "Dynamic Pricing"
description: "Reinforcement Learning · Inventory Optimization"
img: assets/img/dynamic-pricing.png
importance: 6
category: work
---

**Research project · 2024 Tri-Campus Conference**

[View the presentation slides](https://github.com/Linyan0115/Dynamic-Pricing/blob/main/slides-Tricampus2024.pdf) · [View the extended abstract](https://github.com/Linyan0115/Dynamic-Pricing/blob/main/triCampus_Extended%20Abstract.pdf)

## Research Question

How should a supermarket adjust prices for fresh vegetables throughout the day as demand changes and unsold inventory approaches the end of its shelf life? We studied this question using historical sales data for five perishable vegetable products.

## Methodology

**Sales forecasting with Random Forest.** We trained a Random Forest model on historical data to estimate sales under different prices and time slots.

**Pricing decisions with Q-learning.** We divided the selling day into time slots and treated price selection as a sequential decision. We used the sales forecasts to evaluate candidate prices and built a Q-table to guide which pricing action to choose in each state.

{% include figure.liquid path="assets/img/dynamic-pricing.png" class="img-fluid rounded" alt="Framework combining Random Forest sales forecasts with Q-learning pricing decisions" %}

*Random Forest forecasts sales under different prices, and Q-learning guides pricing decisions.*

## Revenue Evaluation

For each candidate pricing strategy, we estimated revenue by multiplying prices by predicted sales. We selected the strategy with the highest estimated revenue and used recorded historical revenue as the benchmark.

{% include figure.liquid path="assets/img/dynamic-pricing-revenue.png" class="img-fluid rounded" alt="Workflow for estimating revenue under candidate pricing strategies and benchmarking against historical revenue" %}

*Workflow for estimating revenue and benchmarking it against historical revenue.*
