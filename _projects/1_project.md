---
layout: page
title: Isoform Markers of Brain Aging
description: Isoform-level machine learning analysis of human brain aging using bulk RNA-seq
img: assets/img/isoform_aging_cover.jpg
importance: 1
category: featured
related_publications: false
---

This project investigates whether **isoform usage patterns** can serve as molecular markers of human brain aging. Using bulk RNA-seq datasets from human brain regions, I developed isoform-level machine learning workflows to identify both **tissue-agnostic** and **hippocampus-specific** transcript usage markers associated with age.

The project was conducted in the Hicks Lab at Johns Hopkins University, Department of Biostatistics, and was presented as a poster at **Biology of Genomes, Cold Spring Harbor Laboratory, 2026**.

---

## Overview

Most transcriptomic aging studies focus on gene-level expression. However, genes can produce multiple transcript isoforms, and the relative usage of these isoforms may change across development and aging. This project asks whether **isoform fractions** provide useful and interpretable features for age prediction and aging marker discovery.

For each gene, I represented transcript usage using isoform fraction features, focusing on the relative abundance of major isoforms. I then trained and evaluated machine learning models to identify age-associated isoform usage patterns and compare their transferability across brain regions.

---

## Key Findings

- Isoform fraction features captured age-associated transcript usage patterns beyond gene-level expression.
- Some isoform aging signals appeared transferable across brain regions, suggesting tissue-agnostic markers.
- Hippocampus-specific feature selection identified additional transcript usage markers that were not prioritized by models trained in other brain regions.
- Cross-region validation showed that aging-associated isoform usage can be partially shared but also region-specific.

---

## My Contributions

- Built isoform-level machine learning models for human brain aging using bulk RNA-seq data.
- Designed feature engineering workflows based on isoform fraction features.
- Compared tissue-agnostic versus hippocampus-specific transcript usage markers.
- Performed feature selection, model evaluation, and cross-dataset validation.
- Generated publication-style figures and presented the project at Biology of Genomes 2026.

---

## Methods

The analysis combined transcript quantification, isoform fraction construction, feature selection, and predictive modeling.

Key steps included:

1. **Transcript-level quantification**  
   RNA-seq reads were quantified at the isoform level and summarized into transcript usage features.

2. **Isoform fraction feature construction**  
   For selected genes, I calculated the relative usage of major isoforms to capture transcript switching behavior.

3. **Feature selection**  
   I identified candidate aging-associated isoform markers using statistical and machine learning-based screening strategies.

4. **Age prediction modeling**  
   I trained regularized regression models to evaluate whether isoform usage features could predict chronological age.

5. **Cross-region validation**  
   I compared markers across brain regions to distinguish tissue-agnostic signals from hippocampus-specific aging patterns.

---

## Poster

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/isoform_aging_poster.png" title="Isoform aging poster" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

<div class="caption">
  Poster presented at Biology of Genomes, Cold Spring Harbor Laboratory, 2026.
</div>

---

## Selected Figures

<div class="row justify-content-sm-center">
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/isoform_aging_model.png" title="Model performance" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/isoform_aging_features.png" title="Isoform aging markers" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

<div class="caption">
  Example outputs from the project, including model evaluation and selected isoform aging markers.
</div>

---

## Tools

`Python` · `Jupyter` · `bulk RNA-seq` · `machine learning` · `elastic net regression` · `feature selection` · `transcriptomics`

---

## Status

This project is ongoing as part of my research in the Hicks Lab. Preprint coming soon in Fall 2026.
