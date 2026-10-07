---
layout: page
title: "Visium HD Analysis Workflows"
description: "Reusable Python workflows for quality control, artifact correction, and tissue-aligned visualization of high-resolution spatial transcriptomics."
img: assets/img/visiumhd_cover.jpg
importance: 6
category: featured
related_publications: false
status: "Research software"
github: https://github.com/danielchen05/visiumhd_utils
---

High-resolution spatial transcriptomics requires careful handling of tissue images, spatial scales, and technical artifacts before biological interpretation. In the Hicks Lab, I developed reusable Jupyter workflows and Python utilities for Visium HD preprocessing, quality control, destriping, and tissue-aligned visualization. These workflows support repeated analyses across spatial resolutions rather than a single dataset-specific result.

The implementation organizes data loading, resolution-specific extraction, spatial QC summaries, and figure generation into reusable steps. Image-aligned plots make it easier to compare expression and QC patterns with tissue structure, while the utilities reduce repeated code across analyses. Completed in September 2025, this research infrastructure also supported figure generation for an NIH R01 proposal.

[Python utilities](https://github.com/danielchen05/visiumhd_utils) · [Analysis workflows](https://github.com/danielchen05/hicks-lab-personal)

{% include figure.liquid path="assets/img/visiumhd_16um_histology_overlay.png" alt="Visium HD gene expression overlaid on histology at 16 micrometer resolution" class="img-fluid rounded z-depth-1" %}

<div class="caption">Image-aligned expression visualization at 16 µm resolution.</div>
