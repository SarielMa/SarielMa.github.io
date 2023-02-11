---
layout: page
permalink: /publications/
title: publications 
years: [2023, 2022, 2021, 2020, 2019,2018]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
