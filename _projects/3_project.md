---
layout: page
title: Controllable Surgical Video Synthesis
description: Video diffusion model for generating photorealistic routine and rare OR events at scale
img: assets/img/projects/endosynth_thumb.svg
importance: 3
category: research
related_publications: true
---

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/projects/endosynth_thumb.svg" title="Controllable OR video synthesis overview" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Our controllable video diffusion model synthesizes photorealistic surgical scenes conditioned on
  structured OR event descriptions, enabling scalable data generation for surgical AI training.
  <em>(Placeholder — replace with actual figures from the paper.)</em>
</div>

## Overview

Annotated surgical video is scarce, expensive to collect, and subject to strict privacy regulations.
**Controllable Surgical Video Synthesis** addresses this bottleneck by building a generative model
capable of producing photorealistic operating room video — including both **routine events** (standard
procedural steps) and **rare events** (unexpected complications, uncommon anatomical variations) —
at scale, conditioned on structured scene and event descriptions.

This work enables:
- **Scalable data augmentation** for training surgical perception models without requiring real patient data
- **Long-tail scenario coverage** — synthesizing rare events that are underrepresented in real datasets
- **Downstream model improvement** — perception models trained with synthetic data showing improved performance on real video

## Method

The framework is built on a **latent video diffusion model** that accepts structured conditioning signals encoding:

- Procedural phase (e.g., dissection, clipping, retrieval)
- Instrument type and position
- Tissue state and anatomical context
- Event rarity label (routine vs. rare complication)

The model is trained on curated surgical video collections and evaluated on multiple benchmarks of
surgical phase recognition and instrument detection, using synthetic data as a training supplement.

## Clinical Relevance

Rare surgical events — such as accidental organ perforations or unexpected bleeding — are critical
failure modes for AI-assisted systems yet are vastly underrepresented in training data. This work
provides a systematic path to closing that gap through controlled, on-demand generation.

## Citation

{% cite schneider2026towards %}

## Links

- [arXiv Preprint](https://arxiv.org/abs/2602.21365){:target="_blank"}

## Team

Dominik Schneider, Lalithkumar Seenivasan, Sampath Rapuri, Vishalroshan Anil, **Aiza Maksutova**,
Yiqing Shen, Jan Emily Mangulabnan, Hao Ding, Jose L. Porras, Masaru Ishii, et al.

*Unberath Lab, Johns Hopkins University*
