---
title: Dance Drama
layout: index
---


{% assign dances = site.exhibits | where: "category", "Dance" %}
{% assign title_alphabetical = dances | sort: "title" %}
{% for one in title_alphabetical %}
  <a href="{{ one.url | relative_url }}"><img src="{{ one.image-url }}" width = 256></a>
  <p><a href ="{{ one.url | relative_url }}">{{ one.title }}</a></p>
{% endfor %}
