---
layout: page
title: "Visium HD Analysis Workflows"
description: "Reusable Python workflows for quality control, artifact correction, and tissue-aligned visualization of high-resolution spatial transcriptomics data."
img: assets/img/visiumhd_cover.jpg
importance: 6
category: featured
related_publications: false
status: "Research software"
github: https://github.com/danielchen05/visiumhd_utils
---

High-resolution spatial transcriptomics data requires careful handling of tissue images, spatial scales, and technical artifacts before biological interpretation. I developed reusable Jupyter notebook workflows and Python utilities for Visium HD preprocessing, quality control, destriping, and tissue-aligned visualization. These workflows support repeated analyses across spatial resolutions.

The implementation organizes data loading, resolution-specific extraction, spatial QC summaries, and figure generation into reusable functions. Image-aligned plots make it easier to compare expression and QC patterns with tissue structure, while the utilities reduce repeated code across analyses. This research infrastructure also supported figure generation for an NIH R01 proposal.

[Python utilities](https://github.com/danielchen05/visiumhd_utils) · [Analysis workflows](https://github.com/danielchen05/hicks-lab-personal/blob/main/VisiumHDPlotting.ipynb)

{% include figure.liquid path="assets/img/visiumhd_16um_histology_overlay.png" alt="Visium HD gene expression overlaid on histology at 16 micrometer resolution" class="img-fluid rounded z-depth-1" %}

<div class="caption">Expression of <i>AA986860</i> in the 10x Genomics Visium HD mouse small intestine dataset, overlaid on histology at 16 µm resolution. Colors show transcript counts per bin (0-4); bins with zero counts are transparent.</div>
