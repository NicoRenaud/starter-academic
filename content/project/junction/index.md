---
title: Molecular Junctions & Machine Learning
summary: Improving conformational sampling using ML
tags:
- Deep Learning
- Molecular Dynamics
- Quantum Transport
date: "2016-02-07T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: Molecular Dynamics in Tunelling Junctions
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

Grasping the molecular dynamics of small molecule in tunelling junction can provide a much deeper understanding of mechanically controlled break-junction experiments. However accurately computing the quantum transport properties along a full MD trajectory is a very costly task.

Using a finite number of training points, machine learning models can be trained to map the conformational space of the molecule to its low-bias conductance values. Linking machine learning and quantum transport would allow for a much more resolved characterization of molecular junctions and would be the first step toward generative modelling of molecular systems with desired quantum transport properties.


{{< figure src="nnjunction.png" caption="" >}}