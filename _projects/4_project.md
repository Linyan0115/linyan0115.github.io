---
layout: page
title: "Parallel Modeling of Steam Review Helpfulness"
description: "A parallel computing pipeline for comparing Steam review helpfulness across languages."
img: assets/img/steam-review-performance.png
importance: 4
category: work
---

**Spring 2026 · STAT405 UW–Madison · Team project**

[View the R scripts and HTCondor job files on GitHub](https://github.com/Linyan0115/large-scale-review-helpfulness-prediction)

## Research Question

How well can review metadata and user activity predict whether a Steam review will be marked as helpful? We compared English, Chinese, and other-language reviews to see how predictive performance varied across groups.

## Parallel Computing Methodology

**Data partitioning.** We grouped reviews by language and split each group into five chunks, creating 15 independent modeling jobs.

**Parallel execution.** We submitted the jobs through HTCondor on UW–Madison’s Center for High Throughput Computing (CHTC). Each job read only its assigned chunk, requested a few gigabytes of memory and disk space, and could run concurrently with the other jobs. Within each chunk, an R script cleaned the data, engineered features, split the data into 80% training and 20% testing, and fit a logistic regression model.

**Aggregation.** Each job saved its fitted coefficients and held-out evaluation metrics. Once all 15 jobs finished, a separate aggregation job combined the outputs, summarized performance across chunks within each language group, and generated comparison plots.

## Results

The English-language models achieved the highest mean AUC (0.706), and the Chinese-language models had the lowest mean AUC (0.609). Performance was stable across chunks within each language group, while the differences between groups showed that the same modeling pipeline had different predictive power across languages.

{% include figure.liquid path="assets/img/steam-review-performance.png" class="img-fluid rounded" alt="Held-out model performance across English, Chinese, and other-language Steam reviews" %}

*Held-out model performance by language group.*
