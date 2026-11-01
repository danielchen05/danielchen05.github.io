---
layout: page
title: "Cross-Donor Generalization"
description: "Testing how evaluation design changes estimates of cell-type classifier performance on unseen donors."
img: assets/img/scrna_benchmark_cover.jpg
importance: 2
category: featured
related_publications: false
status: "bioRxiv preprint (2026)"
github: https://github.com/danielchen05/scRNA-cross-donor-generalization
preprint: https://www.biorxiv.org/content/10.64898/2026.10.26.761949v1
---

Cell-type classifiers can appear more accurate when training and test sets contain cells from the same donors. With Jiabei Li and Alexis Battle, this project compares repeated random cell-level splits with donor-held-out cross-validation across PBMC, lung, kidney, pancreas, and Blood Atlas single-cell RNA-seq datasets. The central question is when cell-level testing overstates performance on unseen donors, and how that gap depends on donor and cell-type structure.

I developed reproducible benchmarking workflows using logistic regression with highly variable genes, PCA, Harmony, and scVI representations where available, with macro F1 as the primary metric. Random cell-level splits yielded higher performance estimates in PBMC and lung, while gaps were smaller near perfect or chance-level classification. Technical-covariate adjustment, donor-level modeling, donor ablation, and cross-site analyses help examine the sources and limits of these differences. Representations are constructed before classifier splitting, so the study evaluates classifier generalization conditional on shared cohort-level representations. The findings support holding out donors when performance claims concern new individuals.

**bioRxiv preprint (2026):** _Evaluation design shapes estimates of cross-donor generalization in single-cell classification of cell-type_ — Xingyi Chen, Jiabei Li, and Alexis Battle.

[Preprint](https://www.biorxiv.org/content/10.64898/2026.10.26.761949v1) · [GitHub](https://github.com/danielchen05/scRNA-cross-donor-generalization) · [Publication details]({{ '/publications/' | relative_url }}#chencrossdonor)

{% include figure.liquid path="assets/img/scrna_figure2_three_panel.png" alt="Existing PBMC benchmark comparing dataset construction, random cell-level and donor-held-out evaluation, and cross-site transfer" class="img-fluid rounded z-depth-1" %}

<div class="caption">Illustrative PBMC analysis from the existing benchmark: evaluation design changes the apparent performance of cell-type classifiers.</div>
