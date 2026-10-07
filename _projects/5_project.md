---
layout: page
title: "Homozygous Deletion Detection"
description: "Finding small, rare deletions in sparse single-cell DNA data by pooling evidence across cells."
img: assets/img/qsure_cover.jpg
importance: 3
category: featured
related_publications: false
status: "QSURE 2026 \u00b7 Research follow-up"
github: https://github.com/danielchen05/scDNA-homozygous-deletions
---

Sparse single-cell DNA data make small homozygous deletions difficult to distinguish from low read coverage, especially when few cancer cells carry an event. During QSURE 2026 in the Shah/McPherson Lab at Memorial Sloan Kettering Cancer Center, I developed a deletion-specific one-sided scan statistic that pools evidence across cells, mentored by Andrew McPherson and Matthew Myers. The approach targets depleted read counts in short genomic intervals and estimates which cells may carry a candidate deletion.

Simulation studies compared the scanner with changepoint and segmentation approaches across sequencing depths, deletion sizes, cell numbers, and carrier fractions. These experiments characterized both detection performance and limits for small or rare events. Applications to MSK-SPECTRUM, followed by additional cancer datasets, examined candidate deletions in real data.

[Code](https://github.com/danielchen05/scDNA-homozygous-deletions)

{% include figure.liquid path="assets/img/qsure_cover.jpg" alt="Existing schematic of pooled single-cell sequencing signals and a deletion scan" class="img-fluid rounded z-depth-1" %}
