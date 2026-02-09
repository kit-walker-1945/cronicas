---
layout: default
title: Línia temporal
permalink: /timeline/
---

# Línia temporal

Totes les històries ordenades cronològicament.

{% assign totes = site.histories | sort: "data" %}
<ul>
{% for h in totes %}
  <li>
    <strong>{{ h.data | date: "%d/%m/%Y" }}</strong> —
    <a href="{{ h.url | relative_url }}">{{ h.title }}</a>
    <small>(Període: <a href="{{ '/periodes/' | relative_url }}{{ h.periode }}/">{{ h.periode }}</a>)</small>
  </li>
{% endfor %}
</ul>
