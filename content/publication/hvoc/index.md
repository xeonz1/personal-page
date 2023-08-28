---
title: "Constrained Iterative Nonlinear Optimization for Robot Control Applications"
authors:
- admin
- Yuqing Chen
date: "2022-09-01T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2022-09-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "*International Conference on Automation and Computing* (ICAC 2022)"
publication_short: ""

abstract: Numerical optimization provides a computational tool widely used to control robotic systems subject to constraints during their motion. However, many of the methods used to solve these problems lack treatment of physical constraints i.e., limitations on the control inputs and constraints on the temporal aspect of the motion, common in practical application. Here we present a computational method to nonlinear dynamic optimization which enables us to take inequality constraints on the control commands and the simultaneously optimized task duration rigorously into account. The presented approach uses state augmentation to reduce the original free time horizon optimization to a fixed time horizon problem. Following this transformation we derive a minimalistic constraint linear-quadratic sub-problem which is iteratively solved to find the solution of the original constrained nonlinear dynamic optimization problem. The proposed approach is used to solve high-dimensional test problems in simulation, a low-dimensional, non-convex robot control problem tested in an feedback control experiment and a high-dimensional, unstable robot planning problem in simulation. These examples indicate high accuracy, demonstrate scalability, and suggest wide range applicability of the proposed approach.
# Summary. An optional shortened abstract.
summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

featured: false

# links:
# - name: ""
#   url: ""
url_pdf: https://ieeexplore.ieee.org/document/9911086

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: [horizon_variable_oc]

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
---
