---
layout: archive
title: "Teaching"
permalink: /teaching/
author_profile: true
---

{% include base_path %}

**Work in Progress** — This page is currently being updated. More teaching material will be added soon.
{: .notice--info}

## Concordia University

*Course Instructor*

{% for post in site.teaching reversed %}
  {% assign month = post.date | date: "%-m" | plus: 0 %}
  {% if month >= 1 and month <= 4 %}{% assign sem = "Winter" %}{% elsif month >= 5 and month <= 8 %}{% assign sem = "Summer" %}{% else %}{% assign sem = "Fall" %}{% endif %}
- [{{ post.title }}]({{ base_path }}{{ post.url }}) &mdash; {{ post.type }}, {{ sem }} {{ post.date | date: "%Y" }}
{% endfor %}
