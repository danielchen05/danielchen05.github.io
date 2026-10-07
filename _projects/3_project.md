---
layout: page
title: "Cross-Donor Generalization"
description: "Testing how evaluation design changes estimates of cell-type classifier performance on unseen donors."
img: assets/img/scrna_benchmark_cover.jpg
importance: 2
category: featured
related_publications: false
status: "Manuscript in preparation"
github: https://github.com/danielchen05/scRNA-cross-donor-generalization
---

Cell-type classifiers can appear more accurate when training and test sets contain cells from the same donors. With Jiabei Li and Alexis Battle, this project compares random cell-level splits with donor-held-out evaluation across multiple single-cell RNA-seq datasets. The central question is when cell-level testing overstates performance on unseen donors, and how that gap depends on donor and cell-type structure.

I developed reproducible benchmarking workflows to compare classifiers using highly variable genes, PCA, Harmony, and scVI representations. Analyses examine overall classification performance alongside donor-level variation and cell-type-specific errors, helping distinguish an evaluation-design effect from a representation or dataset effect. The goal is to clarify what a reported accuracy estimate says about generalization to new individuals.

**Manuscript in preparation:** _Evaluation design shapes estimates of cross-donor generalization in single-cell cell-type classification_ — Xingyi Chen, Jiabei Li, and Alexis Battle.

[Code](https://github.com/danielchen05/scRNA-cross-donor-generalization) · [Manuscript details]({{ '/publications/' | relative_url }}#chencrossdonor)

{% include figure.liquid path="assets/img/scrna_figure2_three_panel.png" alt="Existing PBMC benchmark comparing dataset construction, random cell-level and donor-held-out evaluation, and cross-site transfer" class="img-fluid rounded z-depth-1" %}

<div class="caption">Illustrative PBMC analysis from the existing benchmark: evaluation design changes the apparent performance of cell-type classifiers.</div>
