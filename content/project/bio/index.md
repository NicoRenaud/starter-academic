---
title: Machine Learning for Protein-Protein Interactions
summary: Recognizing natural vs artifical protein interface
tags:
- Deep Learning
- Bioinformatics
- DeepRank
- iScore
- pdb2sql
date: "2019-01-12T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: Protein-Protein Interface Featurization
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

The indentification of biological protein-protein interface is a crucial task of computational biology with applications ranging from drug design to evolutionary studies. The experimental characterization of these interface usually relies on expensive and time consuming methods such X-Ray crystallography. To alleviate this cost a multitude of computational approaches have been developped.

We have recently developped several machine learning based approaches for the classification and scoring of protein-protein interface. Our first attempt, iScore is based on a support vector machine approach using randow walk graph kernels using only about 100 known interfaces in the training set.

{{< figure src="iscore.png" caption="" >}}

{{< icon name="github" pack="fab" >}} [iScore](https://www.github.com/DeepRank/iScore/)


We also explored deep-learning based methods using convolutional neural networks. Featurization of the interface is obtained via gaussian expansion of atomic and residue features on a 3D grid. These models require a large number of training sample that we obtained via molecular dynamics docking simulations on the BM5 dataset.

{{< figure src="deeprank.png" caption="" >}}

{{< icon name="github" pack="fab" >}} [DeepRank](https://www.github.com/DeepRank/DeepRank/)

More recently we have explored the possiblity to use graph neural network to encode the strucrture of the interface. This promising approch would remove the need to artificially augment the training data set to account for rotational invariance of the scoring function.

{{< figure src="deeprank_gnn.png" caption="" >}}

{{< icon name="github" pack="fab" >}} [DeepRank-GNN](https://www.github.com/DeepRank/DeepRank-GNN/)
