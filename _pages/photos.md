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
<div class="projects photos">

<!-- Display photos without categories -->

  <!-- Generate cards for each photo -->
  <div class="container">

{% for photo in site.photos %}
    {% cycle 'add row' : '<div class="row">', '', '' %}

      {% include photos.html %}

{% cycle 'end row' : '', '', '</div>' %}
{% endfor %}


</div>