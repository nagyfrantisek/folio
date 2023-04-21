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
{%- if site.enable_photo_categories and page.display_categories %}
  <!-- Display categorized photos -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_photos = site.photos | where: "category", category -%}
  {%- assign sorted_photos = categorized_photos | sort: "importance" %}
  <!-- Generate cards for each photo -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for photo in sorted_photos -%}
      {% include photos_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for photo in sorted_photos -%}
      {% include photos.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display photos without categories -->
  {%- assign sorted_photos = site.photos | sort: "importance" -%}
  <!-- Generate cards for each photo -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for photo in sorted_photos -%}
      {% include photos_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for photo in sorted_photos -%}
      {% include photos.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>
