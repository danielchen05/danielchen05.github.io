---
layout: page
title: "SpotSweeper-py"
description: "Open-source Python tools for detecting local quality-control outliers in spatial omics data."
img: assets/img/spotsweeper_cover.jpg
importance: 4
category: featured
related_publications: true
status: "Published \u00b7 F1000Research (2026)"
software: https://github.com/danielchen05/spotsweeper_py
analysis_code: https://github.com/danielchen05/SpotSweeper_py_paper
paper: https://f1000research.com/articles/15-33
pypi: https://pypi.org/project/spotsweeper/
---

Spatial omics artifacts can be missed by quality-control thresholds applied across an entire dataset. Under mentorship of Dr. Stephanie Hicks, I developed SpotSweeper-py to bring spatially aware QC from the R/Bioconductor ecosystem into Python workflows. Local neighborhoods provide context for identifying observations with unusual QC metrics relative to nearby spots or cells, supporting review of spatially structured artifacts.

The work combined Python implementation, integration with AnnData/scverse-based analysis, and benchmarking and validation against the original R functionality. Reproducible examples help users examine flagged observations in their tissue context rather than treating every local outlier as a confirmed technical failure. The software and its evaluation are described in our accompanying publication {% cite chen2026spotsweeperpy %}.

{% include figure.liquid path="assets/img/spotsweeper_qc_map.png" alt="Spatial quality-control maps comparing SpotSweeper-py with global QC" class="img-fluid rounded z-depth-1" %}

<div class="caption">Spatial QC summaries help identify local outliers that warrant review in their tissue context. <a href="{{ '/assets/img/spotsweeper_qc_map.png' | relative_url }}">View full-size figure</a>.</div>
