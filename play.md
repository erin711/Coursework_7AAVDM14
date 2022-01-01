---
title: Play
layout: index
---


{% assign plays = site.exhibits | where: "category", "plays" %}
{% assign title_alphabetical = plays | sort: "title" %}
{% for one in title_alphabetical %}
 
  <a href = "{{ one.url | relative_url }}"><img src="{{ one.image-url }}" width = 256></a>
  <p><a href ="{{ one.url | relative_url }}">{{ one.title }}</a></p>
{% endfor %}
