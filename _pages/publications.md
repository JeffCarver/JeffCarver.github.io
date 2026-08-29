---
layout: page
permalink: /publications/
title: publications
nav: true
nav_order: 1
---

<p style="font-size: 1.5rem; font-weight: bold; margin-bottom: 1rem;">Jeffrey Carver has published {% bibliography_count -q @*[type=journal] %} journal papers and {% bibliography_count -q @*[type=conference] %} conference papers.</p>

<div class="social">
  <div class="contact-icons">{% include social.liquid %}</div>
</div>

{% include bib_search.liquid %}

<div class="publications">

{% bibliography %}

</div>
