---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: false
---

Here are a few projects that highlight my work in predictive modeling, analytics, and visualization.

{% assign sorted = site.projects | sort: 'order' %}
{% for p in sorted %}
- [{{ p.title }}]({{ p.url }}) — {{ p.excerpt }}
{% endfor %}
