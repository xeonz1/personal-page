---
title: ARX-6 Bipedal Robot (Tsinghua AIR DISCOVER Lab)
summary: Bipedal robot project. Controlled by HZD gait library (old) / NMPC (new) + WBC.
tags:
  - RO
date: '2022-12-09T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

url_code: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
---
Starting from 2022 summer, I worked in Tsinghua AIR as a research intern on bipedal control with Yufei Jia (Tsinghua undergraduate, now a PhD student), and responsible for the controller design, simulation and sim2real. The ARX6 (AIR) robot is a bipedal robot with 8 DoF (no hip yaw joint) and line foot contact. The robot is controlled initially by the HZD gait library (planned using FROST by Yufei) and WBIC (an C++ implementation of https://arxiv.org/abs/1807.01222).
# HZD + WBIC
The demonstration of the HZD+WBIC controller is shown in the following video:
<video width="320" height="240" controls>
  <source
    src="/content/project/air_bipedal/hzd_sim.mp4"
    type="video/mp4">
</video>