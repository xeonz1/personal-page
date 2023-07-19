---
title: ARX-6M Bipedal Robot (ARX Robotics)
summary: Miniature bipedal robot project. Controlled by NMPC (old) / DCM (new) + WBC.
tags:
  - RO
date: '2023-07-10T00:00:00Z'

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
The ARX-6M (M means "mini") bipedal robot project was started from June 2023 as a core project of ARX INFINITY Robotics. The NMPC approach was adapated to our new robot along with a new weighted QP WBC since we found that the task priority does not always yield better performance. The simulation is shown in the following video:
{{< video src="nmpc_sim.mp4" controls="yes">}}


However, the NMPC approach is difficult to regularized and we failed to transfer the NMPC to our hardware. Therefore, we quickly switched to DCM (or CP) based walking control and adapted the algorithm in *Walking Control Based on Step Timing Adaptation* to our robot with some modifications. For commerical reason, I cannot share the details of the controller, but one can easily implement his/her own according to previous research. See the hardware video:

{{< video src="dcm_hw.mp4" controls="yes">}}

The robot can stably walking for more than 1 minute. However, due to the relatively heavy limbs (effects on centroidal inertia) and modeling error, the robot cannot recover the same performance as in the simulation. 

(The state estimation is a simple kalman filter adapted from MIT Cheetah Software.)