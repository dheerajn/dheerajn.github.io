---
layout: single
title: Links & Resources
permalink: /links/
author_profile: true
---

# Links & Resources

A curated collection of apps I've built and blogs I recommend.

---

## <a name="apps"></a>Apps I've Built

Add your applications here with descriptions and links.

### Example App Name
Brief description of what this app does and why you built it.

**Links**: [Live App](https://example.com) • [Source Code](https://github.com/dheerajn/project)

---

## <a name="blogs"></a>Blogs I Recommend

Great blogs and resources I read regularly and find valuable.

{% for blog in site.data.recommended_blogs.blogs %}
### [{{ blog.title }}]({{ blog.url }})
{{ blog.description }}

{% endfor %}

---

## Other Resources

### Tools & Utilities
Add your favorite tools, libraries, or utilities here.

### Learning Resources
Add courses, tutorials, or documentation you find helpful.

---

*This page is regularly updated with new discoveries and recommendations. Last updated: January 2026*
