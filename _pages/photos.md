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

{% for photo in sorted_photos %}
    {% cycle 'add row' : '<div class="row">', '', '' %}

      {% include photos.html %}

{% cycle 'end row' : '', '', '</div>' %}
{% endfor %}


</div>
