---
layout: page
title: 3D Affordance Learning
description: Spatial affordance prediction for deformable tissue from 3D geometric representations
img: assets/img/projects/affordance3d_thumb.svg
importance: 4
category: research
---

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/projects/affordance3d_thumb.svg" title="3D Affordance Learning" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  3D geometric representations enable richer affordance reasoning over deformable surgical tissue.
  <em>(Placeholder — replace with actual project figures.)</em>
</div>

## Overview

This project investigates **affordance learning in 3D**, extending the dense 2D prediction formulation
to operate directly on 3D point clouds and mesh representations of tissue. Working with 3D geometry
unlocks richer spatial reasoning — such as surface curvature, depth continuity, and multi-view consistency
— that 2D projections fundamentally cannot capture.

The project includes:
- Construction of 3D tissue affordance datasets from stereo endoscopy and phantom setups
- Adaptation of 3D deep learning architectures (PointNet++, sparse convolution networks) to the affordance estimation task
- Integration of monocular depth estimation to enable 3D affordance prediction from single-view endoscopic video at test time

## Relevance

3D affordance reasoning is a prerequisite for high-dexterity autonomous surgical subtasks, where the robot
must account for the full volumetric extent of tissue — not merely its projection onto a camera plane.
This work feeds directly into the AffordTissue framework and lays groundwork for future real-time intraoperative deployment.

## Status

Ongoing work — builds on results from the AffordTissue project.
