---
layout  : page
title   : Welcome to blog.vietcoop.com
tagline : Viet Coop Blog
---
{% include JB/setup %}

<ul class="tag_box inline">
  {% assign categories_list = site.categories %}
  {% include JB/categories_list %}
</ul>

{% for category in site.categories %} 
  <h2 id="{{ category[0] }}-ref">{{ category[0] | join: "/" }}</h2>
  <ul>
    {% assign pages_list = category[1] %}  
    {% include JB/posts_list %}
  </ul>
{% endfor %}
