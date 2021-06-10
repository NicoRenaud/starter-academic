---
title: Real-Time Time Dependent Density Functional
summary: Dynamics of quantum systems
tags:
- Electronic Structure
- Quantum Chemistry
date: "2016-04-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: A very excited pyrole
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

Simulating the time-dependent dynamics of the electronic density of optically excited molecules represent a fantastic challenge for the development of quatum chemistry. Real-Time Time-Dependent Density Functional Theory holds thr promise to give an accurate evaluation of this dynamics at a reasonable computational cost. In contrast to the linear response time-dependent DFT, RT-TD-DFT directly computes the dynamics of the density in repsonse of its excitation by a transient electromagnetic perturbation. The equation of motion :

$$\dot{\rho(t)} = -i\hbar[\mathcal{F}(\rho(t)); \rho(t)]$$

where $\mathcal{F}$ is the Fock matrix and $\rho(t)$ the density matrix. Solving this equation for example using ADF to compute the Fock matrix on a localized orbital Slater basis set, allows to follow the population of the different molecular orbital during and after the excitation process. The Fourier transform of the dipole moment can then gives the excitation spectrum of the system.

Making no assumption of the type of excitation, RT-TD-DFT can access excitations that linear response cannot grasp. This is for example the case of excitations of core electrons that requires very high-intensity X-Ray pulses.

{{< figure src="rttddft.jpeg" caption="" >}}