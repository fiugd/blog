---
layout: default
title: Welcome
---

# {{ page.title }}

_work in progress: more to come_

## posts
<ul class="posts">
  {% for post in site.posts %}
    <li class="post">
      <a href="{{ post.url }}">{{ post.title }}</a>
      <span>{{ post.description }}</span>
      <span>{{ post.category }}</span>
      <time class="publish-date" datetime="{{ post.date | date: '%F' }}">
        {{ post.date | date: "%B %-d, %Y" }}
      </time>
    </li>
  {% endfor %}
</ul>
