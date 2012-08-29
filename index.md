---
layout  : page
title   : Welcome to blog.vietcoop.com
tagline : Viet Coop Blog
---
{% include JB/setup %}


### Recent posts
<ul class="posts">
  {% for post in site.posts %}
    {% if post.hide != true %}
        <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
