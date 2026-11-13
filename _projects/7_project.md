---
layout: page
title: "Multimodal EEG Modeling"
description: "Multimodal Learning · Time Series"
img: assets/img/multimodal-eeg.png
importance: 7
category: work
---

**Summer 2026 · Data Science Research Internship · YG Technology**

## Research Question

Can combining EEG with heart rate, eye tracking, and behavioral signals help predict user states for people the model has never seen?

## Methodology

**Data integration.** I built an AWS S3 pipeline to integrate data from 900 sessions across 39 participants. The pipeline produced 4,366 analysis windows for feature extraction and modeling.

**Multimodal fusion.** I used Random Forest models to compare individual data sources, early fusion, and late fusion. Early fusion combined features before training, while late fusion combined predictions from models trained on separate data sources.

**Cross-participant validation.** I used participant-level GroupKFold to keep all windows from the same person in the same fold. This let me evaluate how well the models generalized to held-out participants.

{% include figure.liquid path="assets/img/multimodal-eeg.png" class="img-fluid rounded" alt="Pipeline combining EEG, heart rate, eye tracking, and behavioral signals for cross-participant modeling" %}

*Multimodal data integration, fusion, and cross-participant evaluation.*

## Results

The modeling pipeline achieved an F1 score of 0.93 under participant-level GroupKFold validation.
