---
layout: page
title: photos
permalink: /photos/
description: A growing collection of your cool photos.
nav: true
nav_order: 2
display_categories: [work, fun]
horizontal: false
---

<!-- pages/photos.md -->
<div class="projects">

<!-- Display photos without categories -->
  {%- assign sorted_photos = site.photos | sort: "importance" -%}
  <!-- Generate cards for each photo -->
  <div class="container">
  <div class="row">
    {%- for photo in sorted_photos -%}
      {% include photos.html %}
    {%- endfor %}
  </div>

</div>
