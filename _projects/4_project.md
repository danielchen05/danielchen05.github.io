---
layout: page
title: Visium HD Spatial Transcriptomics Pipelines
description: Reusable preprocessing, QC, destriping, and visualization workflows for Visium HD data
img: assets/img/visiumhd_cover.jpg
importance: 5
category: featured
related_publications: false
github: https://github.com/danielchen05/visiumhd_utils
---

This project developed reusable computational workflows for analyzing **Visium HD spatial transcriptomics** data. The goal was to support preprocessing, quality control, destriping, visualization, and publication-ready figure generation for high-resolution spatial omics datasets.

The work was conducted in the Hicks Lab at Johns Hopkins University, Department of Biostatistics, as part of ongoing spatial transcriptomics research and NIH R01 proposal development.

---

## Overview

Visium HD enables high-resolution spatial transcriptomic profiling, but the resulting datasets require careful preprocessing and visualization before downstream biological interpretation. Standard workflows often need to handle multiple spatial resolutions, quality-control summaries, image-aligned spatial plots, and technical artifacts that can vary across tissue sections.

To make these analyses more reproducible, I developed a set of reusable Jupyter pipelines and utility functions for Visium HD data analysis. These workflows helped standardize common steps such as loading spatial data, extracting resolution-specific objects, calculating QC metrics, visualizing spatial patterns, and generating publication-ready figures.

---

## Key Features

- Reusable workflows for Visium HD preprocessing and quality-control analysis.
- Support for spatial visualization of QC metrics such as total counts, detected genes, and mitochondrial percentage.
- Destriping and artifact-aware preprocessing workflows for high-resolution spatial data.
- Utility functions organized into a pip-installable Python package.
- Publication-ready figure generation for spatial transcriptomics research.

---

## My Contributions

- Developed 10+ reusable Jupyter pipelines for Visium HD preprocessing, QC, destriping, visualization, and figure generation.
- Built components of a pip-installable `visiumhd-utils` package to support repeated spatial transcriptomics analyses.
- Implemented workflows for visualizing QC metrics across spatial coordinates and tissue regions.
- Adapted analysis steps to work with modern Python spatial omics data structures.
- Generated figures and analysis outputs supporting an NIH R01 grant proposal.

---

## Workflow Scope

This project focused on building reusable analysis infrastructure rather than producing a single final biological figure. The workflows support repeated Visium HD analyses across datasets, including data loading, quality-control calculation, spatial visualization, destriping, and figure export.

The goal was to make common Visium HD analysis steps easier to reproduce, adapt, and reuse in future spatial transcriptomics projects.

---

## Methods

The project focused on creating modular workflows for high-resolution spatial transcriptomics analysis.

Key steps included:

1. **Data loading and organization**  
   Visium HD outputs were loaded into Python-compatible spatial data structures for downstream analysis.

2. **Resolution-specific extraction**  
   Spatial transcriptomics data were organized across multiple bin sizes or spatial resolutions to support flexible analysis.

3. **Quality-control calculation**  
   QC metrics such as total counts, number of detected genes, and mitochondrial percentage were computed and visualized spatially.

4. **Destriping and artifact handling**  
   Workflows were developed to reduce spatial technical artifacts and improve interpretability of downstream plots.

5. **Visualization and figure generation**  
   Reusable plotting functions were created to generate clear, publication-ready spatial transcriptomics figures.

---

## Example Visualization

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/visiumhd_16um_histology_overlay.png" title="Visium HD histology overlay" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

<div class="caption">
  Example Visium HD spatial visualization showing gene expression overlaid on histology at 16µm resolution, illustrating how the workflow supports image-aligned expression mapping across tissue regions.
</div>

---

## Tools

`Python` · `Jupyter` · `spatialdata` · `spatialdata-plot` · `AnnData` · `Scanpy` · `Visium HD` · `spatial transcriptomics` · `quality control` · `data visualization`

---

## Status

This project is a research infrastructure project in the Hicks Lab and supports reproducible spatial transcriptomics analysis workflows. Finished as of September 2025.  
Github links: https://github.com/danielchen05/hicks-lab-personal, https://github.com/danielchen05/visiumhd_utils. 
