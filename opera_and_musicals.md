---
title: Opera and Musicals
layout: index
---

<div id = "gallery">

  {% assign operas = site.exhibits | where: "category", "Opera and Musicals" %}

  {% for one in operas %}
  <div class = "grid_cell">
    <a href = "{{ one.url | relative_url }}"><img src="{{ one.image-url }}" class="gallery_thumb"></a>
    <p class = "caption"><a href ="{{ one.url | relative_url }}">{{ one.title }}</a></p>
  <br>
  <br>
  </div>
{% endfor %}
</div>