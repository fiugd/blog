---
title: Releases
layout: default
permalink: /releases/
---

<ul>
{% for release in site.releases %}
  <li><span>{{ release.date | date_to_string }}</span> &nbsp; <a href="{{ release.url }}">{{ release.title }}</a></li>
{% endfor %}
</ul>
