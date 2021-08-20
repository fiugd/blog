---
layout: default
title: Welcome
---

# {{ page.title }}

_work in progress: more to come_

{% include fiug-intro.md %}

## posts
<ul class="posts">
  {% for post in site.posts %}
    <li class="post">
      <a href="{{ post.url }}">{{ post.title }}</a>
      <span>{{ post.description }}</span> 
      <time class="publish-date" datetime="{{ post.date | date: '%F' }}">
        {{ post.date | date: "%B %-d, %Y" }}
      </time>
      <span>{{ post.category }}</span>
      <ul>
        {% for tag in post.tags %}
          <li>{{ tag }}</li>
        {% endfor %}
      </ul>
    </li>
  {% endfor %}
</ul>
