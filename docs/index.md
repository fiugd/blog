---
layout: default
title: Welcome
---

# {{ page.title }}

_work in progress: more to come_

## posts (fake)
<ul class="posts">
  {% for post in site.posts %}
    <li class="post">
      <a href="{{ post.url }}">{{ post.title }}</a>
      <span>{{ post.description }}</span>
      <time class="publish-date" datetime="{{ post.date | date: '%F' }}">
        {{ post.date | date: "%B %-d, %Y" }}
      </time>
    </li>
  {% endfor %}
</ul>

## misc
[Markdown Cheat Sheet](https://github.com/mundimark/quickrefs/blob/master/HTML.md)

## references
- https://github.com/waltershub/waltershub.github.io
- https://github.com/dzhavat/dzhavat.github.io

