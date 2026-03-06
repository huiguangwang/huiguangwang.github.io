---
layout: single
permalink: /pub/
title: Publications
classes: wide
author_profile: true
last_modified_at: 2025-09-21
comments: True
---



{% assign papers_sorted = site.papers | sort: "year" | reverse %}

{% for paper in papers_sorted %}
  {% include paper-card.html paper=paper %}
{% endfor %}