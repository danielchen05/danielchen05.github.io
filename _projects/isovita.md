---
layout: page
title: "IsoVita"
description: "Learning interpretable compositional features and testing their association with continuous covariates, with applications to transcript isoform usage."
img: assets/img/isovita_method_workflow.png
img_alt: "IsoVita workflow: effective isoform filtering, interpretable balance construction, and discrete and continuous association tests."
importance: 1
category: featured
related_publications: true
status: "bioRxiv (2026)"
preprint: https://www.biorxiv.org/content/10.64898/2026.11.04.764349
software: https://github.com/danielchen05/isovita
analysis_code: https://github.com/danielchen05/IsoVita-paper
pypi: https://pypi.org/project/isovita/
---

Compositional measurements can change along continuous covariates in ways that are difficult to summarize. I developed IsoVita with Dr. Stephanie Hicks to learn interpretable compositional features and test their association with continuous covariates. The method learns a log-ratio balance between two groups of components and evaluates it using complementary changepoint and spline tests. In transcriptomics, this balance summarizes a gene’s multi-isoform composition while retaining the connection to the contributing transcripts.

I implemented the Python package and evaluated the method through simulations and analyses of human hippocampus and dorsolateral prefrontal cortex data. Selection-aware permutations re-learn the balance under shuffled covariate labels, accounting for feature construction during inference; multiple-testing control is applied separately within each branch. Simulations showed low empirical false discovery proportions and increasing detection power as signals strengthened, with performance depending on trajectory shape and study design. The brain analyses identified widespread age-associated isoform variation while retaining transcript-level interpretability. The maintained package also supports other continuous covariates and appropriately prefiltered compositional inputs.

The method and its evaluation are described in our accompanying preprint {% cite chenisovita %}.

{% include figure.liquid path="assets/img/isovita_method_workflow.png" alt="IsoVita workflow: effective isoform filtering, log-ratio trajectory summarization and interpretable balance selection, followed by discrete changepoint and continuous spline tests." class="img-fluid rounded" zoomable=true %}

<div class="caption">IsoVita method overview: effective isoforms are summarized by an interpretable balance, which is evaluated with complementary discrete and continuous tests. <a href="{{ '/assets/img/isovita_method_workflow.png' | relative_url }}">View full-size figure</a>.</div>
