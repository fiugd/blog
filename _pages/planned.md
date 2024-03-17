---
title: Planned
layout: default
permalink: /planned/
---
{{ page.title }}
{% for post in site.categories.planned %}
 <li><span>{{ post.date | date: "%Y-%m-%d" }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}