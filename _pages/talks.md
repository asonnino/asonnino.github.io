---
title: "Talks"
permalink: /talks/
author_profile: true
redirect_from:
  - "/talks.html"
  - "/seminars/"
  - "/seminars.html"
---

I had the opportunity to speak at the following events.

## Invited Talks

{% assign invited_talks = site.data.talks | where: "category", "invited" %}
{% assign grouped_by_year = invited_talks | group_by: "date" %}
{% assign sorted_groups = grouped_by_year | sort: "event" %}

{% for group in sorted_groups reversed %}
{% assign sorted_talks = group.items | sort: "title" %}
{% for talk in sorted_talks reversed %}
{% include talk.html talk=talk %}
{% endfor %}
{% endfor %}

## Conferences and Workshops

{% assign conference_talks = site.data.talks | where: "category", "conference" %}
{% assign grouped_by_year = conference_talks | group_by: "date" %}
{% assign sorted_groups = grouped_by_year | sort: "event" %}

{% for group in sorted_groups reversed %}
{% assign sorted_talks = group.items | sort: "title" %}
{% for talk in sorted_talks %}
{% include talk.html talk=talk %}
{% endfor %}
{% endfor %}

## Others

{% assign misc_talks = site.data.talks | where: "category", "misc" %}
{% assign grouped_by_year = misc_talks | group_by: "date" %}
{% assign sorted_groups = grouped_by_year | sort: "event" %}

{% for group in sorted_groups reversed %}
{% assign sorted_talks = group.items | sort: "title" %}
{% for talk in sorted_talks %}
{% include talk.html talk=talk %}
{% endfor %}
{% endfor %}
