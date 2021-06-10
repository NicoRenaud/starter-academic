---
title: HPC for GW-BSE Simulations
summary: Many-Body Physics for Excited State Chemistry
tags:
- Quantum Chemistry
- GW-BSE
- VOTCA-XTP
date: "2019-07-01T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: Electronic Structure of a benzen on a graphene Sheet
  focal_point: Smart

# links:
# - icon: twitter
#   icon_pack: fab
#   name: Follow
#   url: https://twitter.com/georgecushen
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

GW-BSE simulations allows to obtain avery detailled and accurate calculation of the excitation spectrum of small molecular systems. However this approach requires to solve large-scale eigenvalue problems that becomes rapidly untracktable using conventional methods.

Using [Votca-XTP](https://github.com/votca/xtp), a recent engine for GW-BSE simulations we have implemented Matrix-Free Jacobi-Davidson eigenvalue solvers to accelerate the simulations of small molecule and solve the memory bottleneck associated with the calculations of large systems. Porting these methods to GPU give an additional computational benefits making Votca-XTP a valuable tool for the future of electronic-structure calculations

{{< figure src="davidson.png" caption="Timing and Memory consumption of the Davidson solver compared to the DSYVEX solver from LAPACK. The Davidson solver can be either much faster than DSYVEX or consume orders of magnitude less of memory depending on the type of applications" >}}

{{< icon name="github" pack="fab" >}} [Votca-xtp](https://github.com/votca/xtp)