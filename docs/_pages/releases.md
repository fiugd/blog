---
title: Releases
layout: default
permalink: /releases/
---
{% for post in site.tags.releases %}
 <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
