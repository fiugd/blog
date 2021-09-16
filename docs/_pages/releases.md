---
title: Releases
layout: default
permalink: /released/
---

{% for post in site.categories.released %}
 <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}



{% for release in site.releases %}
  <h2>
    <a href="{{ release.url }}">
      {{ release.name }}
    </a>
  </h2>
  <p>{{ release.content | markdownify }}</p>
{% endfor %}
