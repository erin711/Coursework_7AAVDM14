---
title: Dance Drama
layout: index
---

<div id = "gallery">  
  {% assign dances = site.exhibits | where: "category", "Dance" %}
  {% assign title_alphabetical = dances | sort: "title" %}
  {% for one in title_alphabetical %}
  <div class = "grid_cell">
    <a href="{{ one.url | relative_url }}"><img src="{{ one.image-url }}" class="gallery_thumb"></a>
    <p class = "caption"><a href ="{{ one.url | relative_url }}">{{ one.title }}</a></p>
  </div>
  {% endfor %}
</div>