---
title: "Personal Website with LLM Discoverability"
date: 2026-01-25
tech_stack: "Jekyll, GitHub Pages, Minimal Mistakes Theme"
github_url: "https://github.com/dheerajn/dheerajn.github.io"
excerpt: "A personal website built with Jekyll and GitHub Pages, featuring LLM discoverability optimization and multiple content types."
---

# Personal Website with LLM Discoverability

A personal website and blog built with Jekyll, hosted on GitHub Pages, and optimized for AI discoverability.

## Overview

This project is my personal website where I share blog posts, daily learnings (TIL), and showcase my portfolio projects. It's designed to be simple, fast, and easy to maintain while being discoverable by AI language models.

## Features

- **Multiple Content Types**: Separate sections for blog posts, TIL entries, and projects
- **LLM Optimized**: Includes `/llms.txt`, `/for-llms` page, and Schema.org structured data
- **Responsive Design**: Works great on all devices using the Minimal Mistakes theme
- **Fast & Secure**: Static site generation means no database or server-side code
- **Free Hosting**: Hosted on GitHub Pages at no cost
- **Markdown-Based**: Write content in Markdown for simplicity

## Technical Details

### Stack

- **Static Site Generator**: Jekyll 4.3.4
- **Theme**: Minimal Mistakes (remote theme)
- **Hosting**: GitHub Pages
- **Deployment**: GitHub Actions
- **Content Format**: Markdown with YAML front matter

### Key Implementation Decisions

**Why Jekyll?**
- Native GitHub Pages support
- Large community and ecosystem
- Simple Markdown-based content management
- Extensive plugin support

**Why Minimal Mistakes?**
- Clean, professional design
- Built-in support for multiple content types
- Excellent documentation
- Actively maintained

**LLM Discoverability Features:**
1. **`llms.txt`**: Machine-readable site map in Markdown format
2. **`/for-llms` page**: Human-readable documentation for AI assistants
3. **Schema.org markup**: JSON-LD structured data for Person, BlogPosting, and Blog schemas

### Directory Structure

```
dheerajn.github.io/
├── _config.yml                 # Jekyll configuration
├── _posts/                     # Blog posts
├── _til/                       # TIL entries
├── _projects/                  # Portfolio projects
├── _data/                      # Data files (navigation, social links)
├── _includes/                  # Reusable components
│   └── head/custom.html        # Schema.org structured data
├── pages/                      # Main pages (about, links, etc.)
├── assets/                     # Images, CSS, etc.
└── llms.txt                    # LLM discoverability file
```

## Challenges & Solutions

### Challenge 1: Organizing Multiple Content Types
**Solution**: Used Jekyll collections to separate blog posts, TIL entries, and projects into distinct content types with their own URLs and layouts.

### Challenge 2: LLM Discoverability
**Solution**: Implemented three complementary approaches:
- Machine-readable `llms.txt` file
- Human-readable `/for-llms` documentation page
- Schema.org structured data in JSON-LD format

### Challenge 3: Simple Deployment
**Solution**: GitHub Actions workflow automatically builds and deploys on every push to main branch.

## What I Learned

- Jekyll collections are powerful for organizing different content types
- Static sites are incredibly fast and secure
- GitHub Pages makes deployment dead simple
- LLM optimization is an emerging best practice for content sites
- Markdown is perfect for technical writing

## Future Improvements

- Add search functionality
- Implement tag-based filtering
- Add comment system (Giscus or Utterances)
- Custom domain setup
- Analytics integration
- Dark mode toggle

## Links

- **Live Site**: [dheerajn.github.io](https://dheerajn.github.io)
- **Source Code**: [GitHub Repository]({{ page.github_url }})
- **Jekyll Docs**: [jekyllrb.com](https://jekyllrb.com)
- **Minimal Mistakes**: [Theme Repository](https://github.com/mmistakes/minimal-mistakes)

---

*Built with Jekyll and deployed with GitHub Pages. Source code available on GitHub.*
