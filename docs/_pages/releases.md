---
title: Releases
layout: default
permalink: /released/
---

old way
{% for post in site.categories.released %}
 <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}


new way
<ul>
{% for release in site.releases %}
  <li><span>{{ release.date | date_to_string }}</span> &nbsp; <a href="{{ release.url }}">{{ release.title }}</a></li>
{% endfor %}
</ul>
