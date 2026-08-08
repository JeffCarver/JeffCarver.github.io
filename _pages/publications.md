---
layout: page
permalink: /publications/
title: publications
description: Grouped by category, most recent first. Click "Bib" on any entry to copy its BibTeX citation, or use the search box below.
nav: true
nav_order: 1
---

<div class="social">
  <div class="contact-icons">{% include social.liquid %}</div>
</div>

{% include bib_search.liquid %}

<div class="publications">

<h1 class="bibliography-category">Peer-reviewed Journals</h1>
{% bibliography -q @*[type=journal] %}

<h1 class="bibliography-category">Peer-reviewed Conferences</h1>
{% bibliography -q @*[type=conference] %}

<h1 class="bibliography-category">Editorially Reviewed Journals and Magazines</h1>
{% bibliography -q @*[type=editorial] %}

<h1 class="bibliography-category">Workshops and Other Publications</h1>
{% bibliography -q @*[type=workshop] %}

</div>
