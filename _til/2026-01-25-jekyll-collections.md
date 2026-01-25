---
title: "Jekyll Collections for Content Organization"
date: 2026-01-25
tags: [jekyll, static-sites, web-development]
---

Today I learned that Jekyll collections are a powerful way to organize different types of content beyond just blog posts!

## The Problem

I wanted to separate my blog posts from my TIL (Today I Learned) entries and portfolio projects, but I wasn't sure how to do that in Jekyll.

## The Solution

Jekyll collections let you define custom content types. Here's how to set them up:

### 1. Define Collections in `_config.yml`

```yaml
collections:
  til:
    output: true
    permalink: /til/:title/
  projects:
    output: true
    permalink: /projects/:title/
```

### 2. Create Directory Structure

```
_posts/      # Regular blog posts
_til/        # TIL entries
_projects/   # Portfolio projects
```

### 3. Set Default Layouts

```yaml
defaults:
  - scope:
      path: ""
      type: til
    values:
      layout: single
      author_profile: true
```

## Why This Is Useful

- **Clean separation**: Each content type has its own directory
- **Custom permalinks**: Different URL structures for different content
- **Flexible layouts**: Apply different templates to each collection
- **Easy querying**: Access collections with `site.til` or `site.projects`

## Example Usage

To loop through TIL posts:

```liquid
{% raw %}{% for til in site.til %}
  <a href="{{ til.url }}">{{ til.title }}</a>
{% endfor %}{% endraw %}
```

## Resources

- [Jekyll Collections Documentation](https://jekyllrb.com/docs/collections/)
- [Working with Collections](https://jekyllrb.com/docs/step-by-step/09-collections/)

---

*That's it! Collections make Jekyll way more powerful for multi-content-type sites.*
