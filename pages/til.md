---
layout: archive
title: TIL (Today I Learned)
permalink: /til/
author_profile: false
classes: wide
---

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
    <span style="background-color: #e8e8e8; color: #333; padding: 4px 10px; border-radius: 4px; display: inline-block;">
      <time datetime="{{ til.date | date_to_xmlschema }}">{{ til.date | date: "%B %d, %Y" }}</time>
    </span>
    {% if til.tags %}
      <span style="margin-left: 10px;">
        {% for tag in til.tags %}
          <span style="color: #666;">#{{ tag }}</span>{% unless forloop.last %} {% endunless %}
        {% endfor %}
      </span>
    {% endif %}
  </p>
</article>
{% unless forloop.last %}
<hr style="margin: 2rem 0; border: none; border-top: 2px solid #888;">
{% endunless %}
{% endfor %}

{% if site.til.size == 0 %}
<p>No TIL posts yet. I'll start documenting my daily learnings soon!</p>
<p>TIL posts are short, focused entries about things I learn each day - code snippets, quick tips, problem solutions, and interesting discoveries.</p>
{% endif %}
