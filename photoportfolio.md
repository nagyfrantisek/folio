---
layout: page
title: photoportfolio
permalink: /photoportfolio/
---


{% for image in site.static_files %}

{% if image.path contains '.webp' %}
{% else %}
    {% if image.path contains 'photoportfolio' %}


<div class="grid-sizer"></div>
<div class="grid-item">
  <a href="{{ site.baseurl }}{{ image.path }}">
      <div class="card hoverable">
          {%- if photoportfolio.img %}
        {%- include figure.html
          path=photoportfolio.img
          alt="project thumbnail" -%}
        {%- endif %}

      </div>
    </a>
</div>





    {% endif %}
{% endif %}
{% endfor %}




<!-- this is for the lightbox --> 
<script type="text/javascript" src="/js/lightbox.js"></script>
<link rel="stylesheet" href="/css/lightbox.css">
