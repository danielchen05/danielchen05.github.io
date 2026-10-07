---
layout: page
title: "SpotSweeper-py: Spatial QC"
description: "Open-source Python tools for detecting local quality-control outliers in spatial omics data."
img: assets/img/spotsweeper_cover.jpg
importance: 4
category: featured
related_publications: false
status: "Published \u00b7 F1000Research 2026"
github: https://github.com/danielchen05/spotsweeper_py
---

Spatial omics artifacts can be missed by quality-control thresholds applied across an entire dataset. In the Hicks Lab, I developed SpotSweeper-py to bring spatially aware QC from the R ecosystem into Python workflows. Local neighborhoods provide context for identifying observations with unusual QC metrics relative to nearby spots or cells, supporting review of spatially structured artifacts.

The work combined Python implementation, integration with AnnData-based analysis, and benchmarking and validation against the original R functionality. Reproducible examples help users examine flagged observations in their tissue context rather than treating every local outlier as a confirmed technical failure. The open-source package is described in the 2026 F1000Research paper, _SpotSweeper-py: spatially-aware quality control metrics for spatial omics data in the Python ecosystem_.

[Paper](https://f1000research.com/articles/15-33) · [Code](https://github.com/danielchen05/spotsweeper_py) · [Python package](https://pypi.org/project/spotsweeper/)

{% include figure.liquid path="assets/img/spotsweeper_qc_map.png" alt="Spatial quality-control maps comparing SpotSweeper-py with global QC" class="img-fluid rounded z-depth-1" %}

<div class="caption">Spatial QC summaries help identify local outliers that warrant review in their tissue context.</div>
