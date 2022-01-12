---
title: Dance Drama
layout: index
---

<div class="three_gallery">  
    {% assign dances = site.exhibits | where: "category", "Dance" %}
    {% assign title_alphabetical = dances | sort: "title" %}
    {% for one in title_alphabetical %}
  <div class = "three_grid_cell">
    <a href="{{ one.url | relative_url }}"><img src="{{ one.image-url }}" class="three_gallery_img"></a>
    <div class="three_grid_cell_word">
      <p class = "director1">{{ one.director }}</p>
      <p class = "caption"><a href ="{{ one.url | relative_url }}">{{ one.title }}</a></p>
    </div>
  </div>
  {% endfor %}
</div>