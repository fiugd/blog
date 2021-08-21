---
title: Releases
layout: default
permalink: /released/
---
{% for post in site.categories.released %}
 <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
