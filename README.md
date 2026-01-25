# Dheeraj Neelam's Personal Website

Personal website and blog built with Jekyll and hosted on GitHub Pages.

🌐 **Live Site**: [https://dheerajn.github.io](https://dheerajn.github.io)

## About

This is my personal website where I share:
- **Blog Posts**: Long-form technical articles and tutorials
- **TIL (Today I Learned)**: Quick daily learnings and discoveries
- **Projects**: Portfolio of software projects I've built
- **Links**: Curated resources and recommendations

## Features

- ✨ Clean, responsive design using Minimal Mistakes theme
- 📝 Markdown-based content management
- 🤖 LLM discoverability optimization (`/llms.txt`, Schema.org)
- 🚀 Automated deployment with GitHub Actions
- 🆓 Free hosting on GitHub Pages
- 📱 Mobile-friendly and accessible

## Tech Stack

- **Generator**: Jekyll 4.3.4
- **Theme**: Minimal Mistakes (remote theme)
- **Hosting**: GitHub Pages
- **Deployment**: GitHub Actions
- **Content**: Markdown with YAML front matter

## Project Structure

```
dheerajn.github.io/
├── _config.yml                 # Jekyll configuration
├── _posts/                     # Blog posts
├── _til/                       # TIL entries
├── _projects/                  # Portfolio projects
├── _data/                      # Data files (navigation, social links)
├── _includes/                  # Reusable components
├── _layouts/                   # Custom layouts
├── pages/                      # Main pages
├── assets/                     # Images, CSS, etc.
├── llms.txt                    # LLM discoverability
└── .github/workflows/          # GitHub Actions
```

## Local Development

### Prerequisites

- Ruby (3.0 or higher)
- Bundler (`gem install bundler`)

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/dheerajn/dheerajn.github.io.git
   cd dheerajn.github.io
   ```

2. Install dependencies:
   ```bash
   bundle install
   ```

3. Run the local server:
   ```bash
   bundle exec jekyll serve
   ```

4. Visit `http://localhost:4000` in your browser

### Making Changes

1. Create content in the appropriate directory:
   - Blog posts: `_posts/YYYY-MM-DD-title.md`
   - TIL entries: `_til/YYYY-MM-DD-title.md`
   - Projects: `_projects/project-name.md`

2. Use YAML front matter for metadata:
   ```yaml
   ---
   layout: single
   title: "Your Title"
   date: YYYY-MM-DD
   tags: [tag1, tag2]
   ---
   ```

3. Write content in Markdown below the front matter

4. Commit and push to deploy:
   ```bash
   git add .
   git commit -m "Add new post"
   git push
   ```

## LLM Discoverability

This site implements several features to make it discoverable and understandable by AI language models:

1. **`/llms.txt`**: Machine-readable site map following the llms.txt specification
2. **`/for-llms`**: Human-readable documentation for AI assistants
3. **Schema.org**: JSON-LD structured data for Person, BlogPosting, and Blog

Learn more: [LLM Discoverability Blog Post](https://cassidoo.co/post/ai-llm-discoverability/)

## Deployment

The site automatically deploys when you push to the `main` branch. GitHub Actions builds the site and publishes it to GitHub Pages.

**Workflow**: `.github/workflows/jekyll.yml`

## Configuration

Main configuration is in `_config.yml`. Update:
- Site title, description, and URL
- Author information and social links
- Navigation menu items
- Theme settings

Social links are managed in `_data/social.yml`

## Adding Content

### Blog Post

Create `_posts/YYYY-MM-DD-my-post-title.md`:

```markdown
---
layout: single
title: "My Post Title"
date: YYYY-MM-DD
categories: [category]
tags: [tag1, tag2]
excerpt: "Brief description"
---

Your content here...
```

### TIL Entry

Create `_til/YYYY-MM-DD-what-i-learned.md`:

```markdown
---
title: "What I Learned Today"
date: YYYY-MM-DD
tags: [tag1, tag2]
---

Quick learning or discovery...
```

### Project

Create `_projects/project-name.md`:

```markdown
---
title: "Project Name"
date: YYYY-MM-DD
tech_stack: "Tech, Stack, List"
demo_url: "https://demo.com"
github_url: "https://github.com/user/repo"
excerpt: "Brief description"
---

Project details...
```

## License

Content is © Dheeraj Neelam. Code is available under the MIT License.

## Contact

- **GitHub**: [dheerajn](https://github.com/dheerajn)
- **LinkedIn**: [Update in _data/social.yml]
- **Twitter**: [Update in _data/social.yml]

---

Built with ❤️ using Jekyll and GitHub Pages
