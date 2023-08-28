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

(**The page is permitted by Prof. Guyue Zhou, PI of AIR DISCOVER Lab.**)
# HZD + WBIC
The following video is a simulation of HZD + WBIC in RaiSim. The three models are respectively: the gait lib reference (back), the controller robot (left front), the kinematic reference (right front) from WBIC. The limbs are heavy and the WBIC cannot make the robot fully track the gait library.
{{< video src="hzd_sim.mp4" controls="yes">}}
The following video shows a instable walking of the robot. 
{{< video src="hzd_hw.mp4" controls="yes">}}

The HZD+WBIC method was later deprecated and a new NMPC controller inspired by https://ieeexplore.ieee.org/document/10000244 is used.
# NMPC
We use OCS2 as our MPC backend. The formulation is basically the same as the one in https://ieeexplore.ieee.org/document/10000244. Due the lack of dof and the heavy limbs, the angular velocity feedback to the mpc is always set zero, and the footstep adaption is implemented as continuous dynamics (i.e., the swing foot xy linear velocity is an input) instead of a discrete input at switching. We also incorporated the foot orientation for the ground torque input. The NMPC adjust foot placments online rather than using the heuristic adaption commonly used in HZD + WBIC (PD feedback of average velocity). See the simulation video:

Due to some reasons, the hardware experiment of the NMPC was canceled by AIR as well as the bipedal project.