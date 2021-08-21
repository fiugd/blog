---
title: Releases
layout: default
permalink: /random/
---
{% for post in site.categories.random %}
 <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
