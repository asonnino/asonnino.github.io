---
title: "Publications"
permalink: /publications/
author_profile: true
redirect_from:
  - "/publications.html"
  - "/papers/"
  - "/papers.html"
---

{% if site.author.googlescholar %}
You can also find my papers on [my Google Scholar profile]({{site.author.googlescholar}}).
{% endif %}

### Under Submission

{% assign submissions = site.data.papers | where: "category", "submission" %}
{% assign sorted_submissions = submissions | sort: "name" %}
{% for paper in sorted_submissions %}
{% include paper.html paper=paper %}
{% endfor %}

{% assign publications = site.data.papers | where: "category", "publication" %}
{% assign grouped_by_year = publications | group_by: "date" %}
{% assign sorted_groups = grouped_by_year | sort: "name" %}

{% for group in sorted_groups reversed %}

### {{ group.name }}

{% assign sorted_publications = group.items | sort: "title" %}
{% for paper in sorted_publications %}
{% include paper.html paper=paper %}
{% endfor %}

{% endfor %}
