---
layout: page
title: photos
permalink: /photos/
description:
nav: true
nav_order: 2
horizontal: false
---

<!-- pages/photos.md -->
<div class="projects photos">

<!-- Display photos without categories -->
  {%- assign sorted_photos = site.photos | sort: photo.date -%}
  <!-- Generate cards for each photo -->
  <div class="container">
  <div class="row row-cols-3">
    {%- for photo in sorted_photos reversed -%}
      {% include photos.html %}
    {%- endfor %}
  </div>

</div>
