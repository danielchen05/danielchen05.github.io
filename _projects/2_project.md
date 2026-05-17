---
layout: page
title: SpotSweeper-py
description: Python implementation of spatially aware quality-control metrics for spatial omics data
img: assets/img/spotsweeper_cover.jpg
importance: 2
category: work
related_publications: chen2026spotsweeperpy
---

This project contributed to **SpotSweeper-py**, a Python implementation of spatially aware quality-control metrics for spatial omics data. The goal of the project was to bring SpotSweeper functionality from the R/Bioconductor ecosystem into the Python spatial omics ecosystem, making it easier to apply spatially informed quality control in modern Python workflows.

This work was conducted in the Hicks Lab at Johns Hopkins University, Department of Biostatistics, and contributed to a published F1000Research software workflow.

---

## Overview

Spatial omics technologies measure molecular profiles while preserving tissue location. However, quality-control artifacts in these datasets are often spatially structured: low-quality regions, edge effects, tissue damage, or local technical artifacts may affect nearby spots or cells together.

Traditional quality-control metrics often treat observations independently. SpotSweeper-py addresses this by incorporating spatial neighborhood information into quality-control summaries, helping users identify spatially localized technical artifacts in spatial omics datasets.

---

## My Contributions

- Ported SpotSweeper functionality from R/Bioconductor to Python.
- Helped preserve spatially aware quality-control behavior in the Python implementation.
- Worked with spatial omics data structures and Python analysis workflows.
- Contributed to software development supporting a published F1000Research workflow.
- Helped make spatially aware QC more accessible to users working in the Python ecosystem.

---

## Methods

The project focused on implementing and validating spatially aware quality-control metrics for spatial omics datasets.

Key components included:

1. **Spatial neighborhood construction**  
   Spots or cells are represented using spatial coordinates, allowing nearby observations to be grouped into local neighborhoods.

2. **Quality-control metric calculation**  
   Standard QC metrics can be summarized locally to identify spatially structured artifacts.

3. **Python ecosystem integration**  
   The implementation supports Python-based spatial omics workflows and is designed to work naturally with common data structures used in computational biology.

4. **Validation and reproducibility**  
   Outputs were compared against expected behavior to ensure that the Python version preserved the core functionality of the original SpotSweeper workflow.

---

## Selected Figures

<div class="row justify-content-sm-center">
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/spotsweeper_qc_map.png" title="Spatial QC map" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/spotsweeper_workflow.png" title="SpotSweeper-py workflow" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

<div class="caption">
  Example spatial quality-control outputs and workflow summary for SpotSweeper-py.
</div>

---

## Publication

**Spotsweeper-py – spatially-aware quality control metrics for spatial omics data in the Python ecosystem**  
Chen X, Totty M, Hicks SC. *F1000Research*. 2026.

---

## Tools

`Python` · `spatial omics` · `quality control` · `software development` · `AnnData` · `SpatialData` · `open-source tools`

---

## Status

This project contributed to a published software workflow and supports spatially aware quality control in Python-based spatial omics analysis.
