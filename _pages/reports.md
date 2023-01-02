---
title: "Tech Reports"
permalink: /reports/
author_profile: true
redirect_from:
  - "/reports.html"
  - "/thesis/"
  - "/thesis.html"
  - "/theses/"
  - "/theses.html"
  - "/libra/"
  - "/libra.html"
  - "/diem/"
  - "/diem.html"
  - "/sui/"
  - "/sui.html"
---

This page references non peer-reviewed technical reports and whitepapers I co-authored.

{% assign sorted_papers = site.data.papers | sort: "date" %}

### Sui

{% assign libra = sorted_papers | where: "category", "sui" %}
{% for report in libra reversed %}
{% include paper.html paper=report %}
{% endfor %}

### Libra / Diem

{% assign libra = sorted_papers | where: "category", "libra" %}
{% for report in libra reversed %}
{% include paper.html paper=report %}
{% endfor %}

### Theses

{% assign theses = sorted_papers | where: "category", "thesis" %}
{% for report in theses reversed %}
{% include paper.html paper=report %}
{% endfor %}

### Others

{% assign others = sorted_papers | where: "category", "report" %}
{% for report in others reversed %}
{% include paper.html paper=report %}
{% endfor %}
