---
layout: page
permalink: /publications/
title: publications
description: Published work, manuscripts in preparation, and conference posters.
nav: true
nav_order: 2
---

{% include bib_search.liquid %}

<div class="publications">
  <h2>Publications</h2>
  {% bibliography --group_by none --query @*[output_category=publication]* %}
  <h2>Manuscripts in preparation</h2>
  {% bibliography --group_by none --query @*[output_category=manuscript]* %}
  <h2>Conference poster</h2>
  {% bibliography --group_by none --query @*[output_category=poster]* %}
</div>
