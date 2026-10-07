---
layout: page
title: "IsoVita: Isoform Trajectories"
description: "An interpretable statistical framework for finding gradual and abrupt changes in transcript isoform usage across the human lifespan."
img: assets/img/project_isovita_placeholder.svg
importance: 1
category: featured
related_publications: false
status: "Manuscript in preparation"
---

Genes can change which transcript isoforms they use as people age, but comparisons between predefined age groups can miss the shape and timing of those changes. Developed with Stephanie Hicks, IsoVita summarizes each gene’s multi-isoform composition as an interpretable log-ratio balance between two groups of transcripts. Complementary statistical branches then test that feature for discrete changepoints and continuous nonlinear trajectories.

The method uses selection-aware permutations that re-learn the balance under shuffled age labels, accounting for feature construction during inference; multiple-testing control is applied separately within each branch. Simulation studies evaluate false discoveries, detection power, and sensitivity to sampling design, noise, and isoform complexity. Applications to human hippocampus and dorsolateral prefrontal cortex data examine transcript usage across the lifespan.

**Manuscript in preparation:** _IsoVita: Interpretable detection of temporal variation in isoform composition_ — Xingyi Chen and Stephanie Hicks.

[Manuscript details]({{ '/publications/' | relative_url }}#chenisovita)

{% include figure.liquid path="assets/img/project_isovita_placeholder.svg" alt="IsoVita research figure placeholder" class="img-fluid rounded" %}
