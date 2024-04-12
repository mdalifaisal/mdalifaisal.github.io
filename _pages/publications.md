---
layout: page
permalink: /publications/
title: Publications
description: Manuscript of the studies under review could be provided (subject to respective journal's policy).
years: [2024, 2023]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
