---
title: Miscellaneous
layout: default
permalink: /misc/
---

<ul>
{% for post in site.misc %}
  <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a> - {{ post.category }}</li>
{% endfor %}
</ul>
