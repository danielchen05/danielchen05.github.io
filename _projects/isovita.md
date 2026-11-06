---
layout: page
title: "IsoVita: Isoform Trajectories"
description: "Learning interpretable compositional features and testing their association with continuous covariates, with applications to transcript isoform usage."
img: assets/img/isovita_method_workflow.png
img_alt: "IsoVita workflow: effective isoform filtering, interpretable balance construction, and discrete and continuous association tests."
importance: 1
category: featured
related_publications: false
status: "bioRxiv (2026)"
preprint: https://www.biorxiv.org/content/10.64898/2026.11.04.764349
software: https://github.com/danielchen05/isovita
analysis_code: https://github.com/danielchen05/IsoVita-paper
pypi: https://pypi.org/project/isovita/
---

Compositional measurements can change along continuous covariates in ways that are difficult to summarize. Developed with Stephanie Hicks, IsoVita learns an interpretable log-ratio balance between two groups of components, then tests its association with a continuous covariate using complementary changepoint and spline tests. In transcriptomics, this balance summarizes a gene’s multi-isoform composition while retaining the connection to the contributing transcripts.

The method uses selection-aware permutations that re-learn the balance under shuffled covariate labels, accounting for feature construction during inference; multiple-testing control is applied separately within each branch. Simulation studies evaluate false discoveries, detection power, and sensitivity to sampling design, noise, and isoform complexity. Applications to human hippocampus and dorsolateral prefrontal cortex data examine transcript usage across the lifespan. The maintained package also supports other continuous covariates and appropriately prefiltered compositional inputs.

**bioRxiv (2026):** _Learning interpretable compositional features associated with continuous covariates_ — Xingyi Chen and Stephanie Hicks.

[bioRxiv](https://www.biorxiv.org/content/10.64898/2026.11.04.764349) · [Software](https://github.com/danielchen05/isovita) · [Analysis Code](https://github.com/danielchen05/IsoVita-paper) · [PyPI](https://pypi.org/project/isovita/) · [Publication details]({{ '/publications/' | relative_url }}#chenisovita)

The **Software** repository contains the maintained Python package. **Analysis Code** preserves the implementation, notebooks, and workflows used to reproduce the manuscript analyses independently of future package updates.

{% include figure.liquid path="assets/img/isovita_method_workflow.png" alt="IsoVita workflow: effective isoform filtering, log-ratio trajectory summarization and interpretable balance selection, followed by discrete changepoint and continuous spline tests." class="img-fluid rounded" zoomable=true %}

<div class="caption">IsoVita method overview: effective isoforms are summarized by an interpretable balance, which is evaluated with complementary discrete and continuous tests. <a href="{{ '/assets/img/isovita_method_workflow.png' | relative_url }}">View full-size figure</a>.</div>
