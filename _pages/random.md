---
title: Random
layout: default
permalink: /random/
---
{% for post in site.categories.random %}
 <li><span>{{ post.date | date: "%Y-%m-%d" }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
