---
layout: page
permalink: /grants/
title: grants
description: Funded grants and contracts, reverse chronological order.
nav: true
nav_order: 2
---

{% for grant in site.data.grants %}{{ forloop.index }}. {{ grant.role }}. "{{ grant.title }}." [{{ grant.agency }}]({{ grant.agency_url }}){% if grant.note %} ({{ grant.note }}){% endif %}. {{ grant.amount }}{% if grant.dates %}. {{ grant.dates }}{% endif %}.
{% endfor %}
