---
layout: page
title: Counterfactual World Models
description: Digital twin-conditioned video diffusion for surgical counterfactual scene synthesis
img: assets/img/projects/counterfactual_thumb.svg
importance: 2
category: research
related_publications: true
---

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/projects/counterfactual_thumb.svg" title="Counterfactual World Models overview" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Given a real surgical video and a modified digital twin configuration, our framework synthesizes
  plausible counterfactual outcomes — enabling reasoning about hypothetical interventions.
  <em>(Placeholder — replace with actual figures from the paper.)</em>
</div>

## Overview

**Counterfactual World Models** tackles the question: *"What would have happened if the surgeon had acted differently?"*
By conditioning a video diffusion model on a **digital twin** representation of the surgical scene, we enable
synthesis of plausible counterfactual videos that reflect modified scene states — different instrument positions,
tissue configurations, or procedural choices.

This capability is valuable for:
- **Surgical simulation and training** — generating diverse "what-if" scenarios from a single real procedure
- **AI safety and robustness testing** — evaluating perception and planning systems under rare or adverse conditions
- **Surgical planning** — providing surgeons with a preview of possible outcomes before committing to an action

## Method

The framework consists of two key components:

1. **Digital Twin Conditioning** — A structured 3D scene representation is derived from the real video (via reconstruction
   and semantic parsing) and serves as the controllable conditioning signal. Modifications to the digital twin
   (e.g., changing instrument trajectory, tissue state) drive counterfactual generation.

2. **Video Diffusion Model** — A latent diffusion model takes the modified digital twin as input and synthesizes
   temporally coherent video that reflects the specified scene changes, while preserving photorealistic appearance
   consistent with the original endoscopic footage.

## Significance

Counterfactual reasoning is foundational to causal understanding — a capability that current surgical AI systems
largely lack. This work provides a concrete step toward models that can plan, reason, and adapt rather than
simply pattern-match to training distributions.

## Citation

{% cite shen2025counterfactual %}

## Links

- [arXiv Preprint](https://arxiv.org/abs/2511.17481){:target="_blank"}

## Team

Yiqing Shen, **Aiza Maksutova**, Chenjia Li, Mathias Unberath

*Unberath Lab, Johns Hopkins University*
