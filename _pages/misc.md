---
title: Miscellaneous
layout: default
permalink: /misc/
---

Can anyone tell me what the difference is between 'random' and 'miscellaneous'?

And what is a 'post' versus a 'page'?

Random:   
<ul>
{% for post in site.categories.random %}
 <li><span>{{ post.date | date: "%Y-%m-%d" }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
   
Miscellaneous:   
<ul>
{% assign sorted_misc = site.misc | sort: 'date' | reverse %}
{% for post in sorted_misc %}
  <li><span>{{ post.date | date: "%Y-%m-%d" }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a> - {{ post.description }}</li>
{% endfor %}
</ul>


