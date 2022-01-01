---
title: opera and musicals
layout: index
---


{% assign operas = site.exhibits | where: "category", "Opera and Musicals" %}

{% for one in operas %}

  <a href = "{{ one.url | relative_url }}"><img src="{{ one.image-url }}" width = 256></a>
  <p><a href ="{{ one.url | relative_url }}">{{ one.title }}</a></p>
{% endfor %}