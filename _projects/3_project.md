---
layout: page
title: Bias in scRNA-seq Annotation Benchmarks
description: Donor-held-out evaluation reveals leakage from random cell-level splits
img: assets/img/scrna_benchmark_cover.jpg
importance: 4
category: featured
related_publications: false
github: https://github.com/danielchen05/scRNA-cross-donor-generalization
---

This project evaluates how common train/test splitting strategies can bias single-cell RNA-seq cell type annotation benchmarks. Using healthy PBMC data with donor metadata, I compared random cell-level splits against donor-held-out evaluation to test whether models generalize to unseen biological donors.

The main finding is that **random cell-level splits can systematically inflate annotation performance** because cells from the same donor can appear in both training and test sets. Donor-held-out evaluation provides a more realistic estimate of cross-donor generalization.

---

## Overview

Cell type annotation models are often evaluated using random splits of individual cells. However, in single-cell datasets, cells are not independent observations: many cells come from the same biological donor, tissue sample, or sequencing batch. If cells from the same donor appear in both training and test sets, benchmark performance may partly reflect donor-level leakage rather than true generalization.

This project compares two evaluation schemes:

1. **Random cell-level split**  
   Cells are randomly divided into training and test sets.

2. **Donor-held-out evaluation**  
   Entire donors are held out during testing, forcing the model to generalize to unseen individuals.

I evaluated these schemes across multiple data representations and classification metrics to determine how much evaluation design affects reported performance.

---

## Key Findings

- Random cell-level splits produced systematically higher performance than donor-held-out evaluation.
- The evaluation scheme often mattered more than the choice of representation.
- Donor-held-out testing exposed harder generalization problems, especially for biologically similar cell types.
- Cross-site transfer further reduced performance, highlighting distribution shift between collection sites.
- T-cell subtype classification remained challenging across representations, suggesting that biological structure influences model errors.

---

## My Contributions

- Designed and implemented the benchmark comparing random cell-level and donor-held-out evaluation schemes.
- Trained multinomial logistic regression classifiers across HVG, PCA, Harmony, and scVI representations.
- Evaluated performance using macro F1, accuracy, per-class F1, confusion matrices, and cross-site transfer analyses.
- Performed donor ablation and cell-type-specific error analyses.
- Built a reproducible research package with ordered notebooks, modular Python code, manuscript, presentation, GitHub repository, and archived Zenodo snapshot.

---

## Methods

The project used healthy PBMC single-cell RNA-seq data with donor and site metadata.

Key steps included:

1. **Data preprocessing**  
   Filtered and organized the dataset by donor, site, and cell type.

2. **Representation construction**  
   Compared multiple input representations, including HVG expression, PCA, Harmony, and scVI.

3. **Model training**  
   Trained multinomial logistic regression classifiers under each evaluation scheme.

4. **Benchmark evaluation**  
   Compared random cell-level splits against donor-held-out testing using macro F1, accuracy, and per-class performance.

5. **Error analysis**  
   Used confusion matrices, donor ablation, and cell-type-specific analyses to identify where models struggled.

---

## Selected Figures

<div class="row justify-content-sm-center">
  <div class="col-sm-12 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/scrna_figure2_three_panel.png" title="Dataset construction, evaluation strategy, and site transfer affect apparent model performance" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

<div class="caption">
  Random cell-level splitting inflates apparent cell type annotation performance compared with donor-held-out evaluation, while cross-site transfer reveals additional distribution shift between collection sites.
</div>

---

## Tools

`Python` · `Scanpy` · `AnnData` · `scikit-learn` · `scVI` · `Harmony` · `single-cell RNA-seq` · `benchmarking`

---

## Status

This project was completed as a final project for Computational Genomics: Data Analysis under mentorship of Dr. Alexis Battle. It is currently being considered for further extension into a formal benchmark.
