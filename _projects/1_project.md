---
layout: page
title: "InterVLM"
description: "Multimodal Learning · Model Interpretability"
img: assets/img/intervlm-pipeline.png
importance: 1
category: work
---

**March–May 2026 · Team project**

[View the code on GitHub](https://github.com/JayDuan123/InterVLM)

## Overview

Memes often convey meaning through the combination of an image and its caption. In InterVLM, we studied which features a vision–language model uses when predicting hate, humor, and stance.

## Approach

We extracted MemeCLIP embeddings from 20,827 memes and trained a Top-K sparse autoencoder. We measured how the learned features aligned with human-annotated concepts, then used ablation and activation steering to test how individual features influenced model predictions.

{% include figure.liquid path="assets/img/intervlm-pipeline.png" class="img-fluid rounded" alt="InterVLM pipeline from meme inputs to sparse feature analysis" %}

*The InterVLM pipeline, from meme inputs to sparse feature analysis.*

## Results

We identified 2,493 feature–concept alignments. In one steering experiment, increasing a feature’s activation lowered the model’s predicted hate score and raised its predicted support score.

{% include figure.liquid path="assets/img/intervlm-results.png" class="img-fluid rounded" alt="Concept alignment comparison between sparse autoencoder features and MemeCLIP neurons" %}

*Concept alignment of sparse autoencoder features and MemeCLIP neurons.*
