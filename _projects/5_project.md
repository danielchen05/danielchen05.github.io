---
layout: page
title: "Homozygous Deletion Detection"
description: "Finding small, rare deletions in sparse single-cell DNA data by pooling evidence across cells."
img: assets/img/qsure_cover.jpg
img_alt: "Schematic of pooled single-cell sequencing signals and a deletion scan"
importance: 3
category: featured
related_publications: false
status: "QSURE (2026) \u00b7 Research follow-up"
github: https://github.com/danielchen05/scDNA-homozygous-deletions
---

Sparse single-cell DNA data make small homozygous deletions (both DNA copies lost) difficult to distinguish from low read coverage, especially when few cancer cells carry an event. During my QSURE internship in the Shah/McPherson Lab at Computational Oncology Service at Memorial Sloan Kettering Cancer Center, I developed a deletion-specific one-sided scan statistic that pools evidence across cells, mentored by Andrew McPherson and Matt Myers. The approach targets depleted read counts in short genomic intervals and estimates which cells may carry a candidate deletion.

Simulation studies compared the scanner with changepoint and segmentation approaches across sequencing depths, deletion sizes, cell numbers, and carrier fractions. In controlled simulations, the scanner achieved perfect precision and recall when an event contained at least one fully deleted bin; strictly sub-bin events remained difficult because bin-level averaging diluted the signal. Applications to MSK-SPECTRUM, followed by additional cancer datasets, examined candidate deletions in real data. Technical zero-count regions required further filtering, so these candidates remain exploratory rather than validated biological calls.

[Code](https://github.com/danielchen05/scDNA-homozygous-deletions)

{% include figure.liquid path="assets/img/qsure_cover.jpg" alt="Schematic of pooled single-cell sequencing signals and a deletion scan" class="img-fluid rounded z-depth-1 project-portrait-figure" avoid_scaling=true %}

<div class="caption">Schematic: a shared drop in read counts across a subset of cells (top) contributes to a pooled scan signal that highlights a candidate deletion interval (bottom).</div>
