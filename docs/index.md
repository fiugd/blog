---
layout: default
title: Welcome
---

# {{ page.title }}

_work in progress: more to come_

TODO: move all of the following from fiug-beta to here

![image](https://user-images.githubusercontent.com/1816471/128581713-cddc90d7-0ebf-43f5-82ae-d16376b18006.png)


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
- [Markdown Cheat Sheet](https://github.com/mundimark/quickrefs/blob/master/HTML.md)

## references
- [waltershub](https://github.com/waltershub/waltershub.github.io)
- [dzhavat](https://github.com/dzhavat/dzhavat.github.io)

