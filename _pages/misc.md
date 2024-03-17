---
title: Miscellaneous
layout: default
permalink: /misc/
---

Can anyone tell me what the difference is between 'random' and 'miscellaneous'?

And what is a 'post' versus a 'page'?

Random Posts:   
{% for post in site.categories.random %}
 <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
   
Other Miscellaneous:   
<ul>
{% for post in site.misc %}
  <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a> - {{ post.description }}</li>
{% endfor %}
</ul>
   
Drafts:
<ul>
{% for post in site.misc %}
  <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a> - {{ post.description }}</li>
{% endfor %}
</ul>

