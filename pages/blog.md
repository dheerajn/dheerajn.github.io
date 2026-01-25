---
layout: archive
title: Blog
permalink: /blog/
author_profile: true
---

# Blog Posts

Long-form technical articles, tutorials, and thoughts on software engineering.

{% for post in site.posts %}
<article class="archive__item">
  <h2 class="archive__item-title">
    <a href="{{ post.url }}">{{ post.title }}</a>
  </h2>
  <p class="archive__item-excerpt">
    {{ post.excerpt | strip_html | truncate: 200 }}
  </p>
  <p class="page__meta">
    <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
    {% if post.tags %}
      • Tags: {{ post.tags | join: ", " }}
    {% endif %}
  </p>
</article>
{% endfor %}

{% if site.posts.size == 0 %}
<p>No blog posts yet. Check back soon!</p>
<p>In the meantime, explore:</p>
<ul>
  <li><a href="/til/">TIL (Today I Learned)</a> - Quick learnings and discoveries</li>
  <li><a href="/projects/">Projects</a> - Portfolio of work</li>
  <li><a href="/about/">About</a> - Learn more about me</li>
</ul>
{% endif %}
