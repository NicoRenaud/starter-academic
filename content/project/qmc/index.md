---
title: Deep Learning approach of Quantum Monte Carlo Simulations
summary: Quantum Aware Neural Network form QMC
tags:
- Quantum Chemistry
- Deep Learning
- QMCTorch
date: "2019-10-12T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: A Quantum Aware Neural Network
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

Quantum Monte Carlo (QMC) simulations hold great promises for exascale electronic structure calculations as the MCMC sampling can easily be distriubted on large scale compute infrastructure with minimal communication cost. QMC simulations consists of interleaed sampling and optimization of a wave function ususally expressed as :


$$\Psi(R) = J(R) \sum_n c_n D_n^\uparrow(Q) D_n^\downarrow(Q)$$

where $J(R)$ is a Jastrow factor capturing electronic correlation and $D_n^\uparrow(Q)$ and $D_n^\downarrow(Q)$ Slater determinants constructed over the basis of molecular orbitals and computed at the backflow-transformed coordinates, $Q$, of the spin up and down electrons.

The code we developped, QMCTorch, implement these wave function ansatz in a quantum aware neural network. Well known ingredients of the wave function, e.g. the atomic and molecular orbitals have been directly implemented in the architecture of the network. Other ingredients such a the Jastrow factor and the backflow transformation kernels can be defined as sub-network allowing for a very flexible functional form.

This semi-analytical wave function ansatz allows for fast calculations of the key observables, e.g. the kinetic energy and atomic forces, via the Jacobi Formula. For example in absence of backflow and Jastrow the kinetic energy can be evaluated with the help of  :

$$\frac{\partial^2 \det{A}}{\partial x_i^2} = Tr(A^{-1} \frac{\partial^2 A}{\partial x_i^2})$$

Hence avoiding a costly computation of the diagonal Hessian via automatic differentiation.

{{< icon name="github" pack="fab" >}} [QMCTorch](https://www.github.com/NLESC-JCER/QMCTorch/)