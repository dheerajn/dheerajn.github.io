---
layout: single
title: TIL (Today I Learned)
permalink: /til/
author_profile: false
classes: wide
---

# Today I Learned

Quick learnings, discoveries, and "aha!" moments. Short, focused posts with code snippets, tips, and tricks I pick up along the way.

{% assign sorted_til = site.til | sort: 'date' | reverse %}
{% for til in sorted_til %}
<article class="archive__item">
  <h2 class="archive__item-title">
    <a href="{{ til.url }}">{{ til.title }}</a>
  </h2>
  <p class="archive__item-excerpt">
    {{ til.excerpt | strip_html | truncate: 300 }}
  </p>
  <p class="page__meta">
    <time datetime="{{ til.date | date_to_xmlschema }}">{{ til.date | date: "%B %d, %Y" }}</time>
    {% if til.tags %}
      • Tags: {{ til.tags | join: ", " }}
    {% endif %}
  </p>
</article>
{% endfor %}

{% if site.til.size == 0 %}
<p>No TIL posts yet. I'll start documenting my daily learnings soon!</p>
<p>TIL posts are short, focused entries about things I learn each day - code snippets, quick tips, problem solutions, and interesting discoveries.</p>
{% endif %}
