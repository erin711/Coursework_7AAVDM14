---
title: Top Picks
layout: index
---

{% for exhibit in site.exhibits %}

{% assign writers = site.data.writers | find: "writer", exhibit.writer %}


<a href="{{ exhibit.url | relative_url }}" target="_blank" title="跳转到individual page"><img src="{{ exhibit.image-url }}" width = 350></a>
<h3><a href="{{ exhibit.url | relative_url }}">{{ exhibit.title }}</a> by <a href="{{ writers.writer-url }}">{{ exhibit.writer }}</a></h3>
<p>{{ exhibit.brief-introduction }}</p>

{% endfor %}
