---
layout: page
title: AffordTissue
description: Dense affordance prediction for tool-action specific tissue interaction in surgical robotics
img: assets/img/projects/affordtissue_thumb.svg
importance: 1
category: research
related_publications: true
---

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/projects/affordtissue_thumb.svg" title="AffordTissue framework overview" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  AffordTissue produces spatially dense affordance maps conditioned on surgical tool type and action,
  enabling intraoperative guidance for robotic and AI-assisted surgery.
  <em>(Placeholder — replace with actual figures from the paper.)</em>
</div>

## Overview

**AffordTissue** addresses a fundamental challenge in surgical robotics: given an endoscopic view of a surgical field,
where should a specific tool engage with tissue, and how?
Rather than coarse region proposals, AffordTissue produces **dense, pixel-wise affordance maps** conditioned jointly
on the instrument type (e.g., grasper, scissors, cautery) and the desired action (e.g., grasp, cut, coagulate).

This level of spatial precision is critical for:
- Autonomous robotic subtask execution (e.g., tissue grasping, blunt dissection)
- Surgeon decision support and intraoperative guidance overlays
- Data-efficient imitation learning from demonstration

## Method

AffordTissue frames tissue affordance estimation as a **dense prediction problem** over the endoscopic image.
We condition the network on a structured action-tool specification and leverage:

- **Geometric priors** — depth/surface normal estimates from monocular endoscopic video
- **Texture and appearance cues** — learned from endoscopic imagery of phantom and ex-vivo tissue
- **Action-conditioned cross-attention** — to fuse tool-action context with spatial image features

The output is a per-pixel affordance probability map indicating where the specified tool-action interaction is feasible and safe.

## Results

AffordTissue was validated on phantom tissue setups and ex-vivo datasets, demonstrating:

- State-of-the-art localization accuracy for tool-tissue interaction regions
- Generalisation across instrument types not seen during training
- Potential for real-time deployment in a surgical workstation pipeline

## Citation

{% cite maksutova2026affordtissue %}

## Links

- [arXiv Preprint](https://arxiv.org/abs/2604.01371){:target="_blank"}
- **Code**: _Coming soon_

## Team

**Aiza Maksutova**, Lalithkumar Seenivasan, Hao Ding, Jiru Xu, Chenhao Yu, Chenyan Jing, Yiqing Shen, Mathias Unberath

*Unberath Lab, Johns Hopkins University*
