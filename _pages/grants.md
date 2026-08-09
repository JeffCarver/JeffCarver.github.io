---
layout: page
permalink: /grants/
title: grants
nav: true
nav_order: 2
---

{% assign today = site.time | date: '%s' %}

## Active Grants

{% assign n = 0 %}
{% for grant in site.data.grants %}{% assign is_active = false %}{% if grant.end_date %}{% assign end_ts = grant.end_date | date: '%s' %}{% if end_ts >= today %}{% assign is_active = true %}{% endif %}{% endif %}{% if is_active %}{% assign n = n | plus: 1 %}
{{ n }}. {{ grant.role }}. "{{ grant.title }}." [{{ grant.agency }}]({{ grant.agency_url }}){% if grant.note %} ({{ grant.note }}){% endif %}. {{ grant.amount }}{% if grant.dates %}. {{ grant.dates }}{% endif %}.
{% endif %}{% endfor %}

## Completed Grants

{% assign n = 0 %}
{% for grant in site.data.grants %}{% assign is_active = false %}{% if grant.end_date %}{% assign end_ts = grant.end_date | date: '%s' %}{% if end_ts >= today %}{% assign is_active = true %}{% endif %}{% endif %}{% unless is_active %}{% assign n = n | plus: 1 %}
{{ n }}. {{ grant.role }}. "{{ grant.title }}." [{{ grant.agency }}]({{ grant.agency_url }}){% if grant.note %} ({{ grant.note }}){% endif %}. {{ grant.amount }}{% if grant.dates %}. {{ grant.dates }}{% endif %}.
{% endunless %}{% endfor %}
