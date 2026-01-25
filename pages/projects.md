---
layout: archive
title: Projects
permalink: /projects/
author_profile: true
---

# Projects

A collection of software projects I've built. Each project showcases different technologies, problem-solving approaches, and learning experiences.

{% assign sorted_projects = site.projects | sort: 'date' | reverse %}
{% for project in sorted_projects %}
<article class="archive__item">
  <h2 class="archive__item-title">
    <a href="{{ project.url }}">{{ project.title }}</a>
  </h2>

  {% if project.tech_stack %}
  <p class="page__meta">
    <strong>Tech Stack:</strong> {{ project.tech_stack }}
  </p>
  {% endif %}

  <p class="archive__item-excerpt">
    {{ project.excerpt | strip_html | truncate: 200 }}
  </p>

  <p class="archive__item-links">
    {% if project.demo_url %}
      <a href="{{ project.demo_url }}" target="_blank" rel="noopener">Live Demo</a>
    {% endif %}
    {% if project.demo_url and project.github_url %} • {% endif %}
    {% if project.github_url %}
      <a href="{{ project.github_url }}" target="_blank" rel="noopener">Source Code</a>
    {% endif %}
  </p>
</article>
<hr>
{% endfor %}

{% if site.projects.size == 0 %}
<p>Project portfolio coming soon! I'll be adding details about the software projects I've built.</p>
<p>Check back later or explore:</p>
<ul>
  <li><a href="/blog/">Blog</a> - Technical articles and tutorials</li>
  <li><a href="/til/">TIL</a> - Daily learnings and quick tips</li>
  <li><a href="https://github.com/dheerajn">GitHub</a> - View my repositories</li>
</ul>
{% endif %}
