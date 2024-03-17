---
title: Present
layout: default
permalink: /present/
---
{{ page.title }}
{% for post in site.categories.present %}
 <li><span>{{ post.date | date: "%Y-%m-%d" }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}