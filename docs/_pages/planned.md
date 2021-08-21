---
title: Planned
layout: default
permalink: /planned/
---
{% for post in site.categories.planned %}
 <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
