---
layout: page
title: Longeek Tech Notes
tagline: pythonic, stacker
---
{% include JB/setup %}

##My Posts list:

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

