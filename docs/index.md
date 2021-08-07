---
layout: default
title: Welcome
---

# {{ page.title }}


_Add your text here_

:::Testing:::

What's Markdown (`.md`)?

Markdown is markup that lets you write hypertext (HTML) documents
in easy-to-read and easy-to-write plain text.
No angle brackets `<></>` required for
paragraphs, lists, blockquotes, tables, etc.


This is a paragraph (in Markdown). Some more
text here.

This is another paragraph.

This is a list:

- Orange
- Apple
- Blueberry



Just getting started with Markdown?
See the [HTML <-> Markdown Quick Reference (Cheat Sheet)][quickref].


[quickref]: https://github.com/mundimark/quickrefs/blob/master/HTML.md

{% for post in site.posts %}
  <h1>[{{ post.title | escape }}]({{ post.url | relative_url }})</h1>
  > {{ post.description }}
  {{ post.date }}
{% endfor %}

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
