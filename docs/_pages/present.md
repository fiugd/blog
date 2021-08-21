---
title: Present
layout: default
permalink: /present/
---
{% for post in site.categories.present %}
 <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
