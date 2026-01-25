# Setup Guide - Getting Your Site Live

Your personal website is ready! Follow these steps to deploy it to GitHub Pages.

## ✅ What's Already Done

All the files are created and ready in: `~/Desktop/dheerajn.github.io/`

- ✅ Jekyll configuration
- ✅ All pages (home, blog, TIL, projects, links, about)
- ✅ Example content (1 blog post, 1 TIL, 1 project)
- ✅ LLM discoverability features (llms.txt, /for-llms, Schema.org)
- ✅ GitHub Actions workflow
- ✅ Git repository initialized with initial commit

## 🚀 Next Steps to Deploy

**IMPORTANT**: You already have a `dheerajn.github.io` repository! We'll replace it with your new personal website.

**Good News**: Your Plainly privacy page at `/Plainly/privacy/` will keep working - it's in a separate repository and won't be affected!

### Quick Migration (4 Commands)

Run these commands to replace your existing site:

```bash
cd ~/Desktop/dheerajn.github.io

# Connect to your existing GitHub repository
git remote add origin https://github.com/dheerajn/dheerajn.github.io.git

# Fetch existing repo
git fetch origin

# Replace with new site (force push)
git push -u origin main --force
```

### What Happens After Push

1. GitHub Actions automatically starts building your site
2. Wait 2-3 minutes for deployment
3. Your site goes live at: **https://dheerajn.github.io**

### Verify Everything Works

After deployment, check:
- ✅ https://dheerajn.github.io → Your new personal site
- ✅ https://dheerajn.github.io/Plainly/privacy/ → Still works!
- ✅ https://dheerajn.github.io/besafe.json → Still accessible

### Configure GitHub Pages (If Needed)

If the site doesn't deploy automatically:
1. Go to repository **Settings** → **Pages**
2. Under **Source**, select **GitHub Actions**
3. Save and wait for deployment

### Backup Available

Your old site is backed up at: `~/Desktop/dheerajn.github.io-backup/`

If you need to rollback, see **MIGRATION_GUIDE.md** for instructions.

## 📝 Things to Customize

Before or after deploying, update these with your info:

### 1. Update Social Links

Edit `_data/social.yml`:
```yaml
links:
  - name: LinkedIn
    url: https://linkedin.com/in/YOUR-PROFILE  # ← Update this
  - name: Twitter
    url: https://twitter.com/YOUR-HANDLE        # ← Update this
```

### 2. Update About Page

Edit `pages/about.md` to add:
- Your bio
- What you do
- Your interests
- Professional background

### 3. Update Config

Edit `_config.yml`:
- Line 6: Update your location
- Line 10-12: Update your LinkedIn and Twitter URLs
- Line 141: Update timezone if needed

### 4. Add Profile Picture

1. Add your photo to `assets/images/profile.jpg`
2. Or update the path in `_config.yml` (line 5)

## 📱 Local Development (Optional)

To preview your site locally before pushing:

### Install Ruby and Jekyll

**Mac** (using Homebrew):
```bash
brew install ruby
gem install bundler jekyll
```

**Follow the prompts to add Ruby to your PATH**

### Run Locally

```bash
cd ~/Desktop/dheerajn.github.io
bundle install
bundle exec jekyll serve
```

Visit: `http://localhost:4000`

## ✍️ Creating Content

### New Blog Post

Create `_posts/2026-01-26-my-post-title.md`:

```markdown
---
layout: single
title: "My Post Title"
date: 2026-01-26
categories: [category]
tags: [tag1, tag2]
excerpt: "Brief description"
---

Your content here...
```

### New TIL Entry

Create `_til/2026-01-26-learned-something.md`:

```markdown
---
title: "What I Learned"
date: 2026-01-26
tags: [tag1]
---

Quick learning...
```

### New Project

Create `_projects/project-name.md`:

```markdown
---
title: "Project Name"
date: 2026-01-26
tech_stack: "React, Node.js"
demo_url: "https://demo.com"
github_url: "https://github.com/dheerajn/project"
excerpt: "Brief description"
---

Project details...
```

## 🔄 Publishing Changes

After making changes:

```bash
git add .
git commit -m "Description of changes"
git push
```

GitHub Actions will automatically rebuild and redeploy your site!

## 🌐 Custom Domain (Future - Optional)

To use your own domain (like `yourname.com`) instead of `dheerajn.github.io`:

1. Buy a domain from a registrar (Namecheap, Google Domains, etc.)
2. Add a `CNAME` file to the root with your domain name
3. Configure DNS at your registrar to point to GitHub Pages
4. Enable custom domain in GitHub repository settings

**No migration needed** - just DNS configuration!

## 📊 Adding Analytics (Optional)

To track visitors:

1. **Google Analytics**: Add tracking ID to `_config.yml`
2. **Plausible**: Add script to `_includes/head/custom.html`

## 🎨 Customizing Design

The site uses the Minimal Mistakes theme. To customize:

- **Colors**: Edit `_config.yml` → `minimal_mistakes_skin`
- **Fonts**: Add custom CSS in `assets/css/main.scss`
- **Layout**: Override theme files in `_layouts/` or `_includes/`

See: [Minimal Mistakes Docs](https://mmistakes.github.io/minimal-mistakes/docs/configuration/)

## 🤖 LLM Discoverability

Your site includes:

1. **`/llms.txt`** - Update with your topics and expertise
2. **`/for-llms`** - Already configured, but you can customize
3. **Schema.org** - Automatically generated from your content

These help AI tools like Claude and ChatGPT understand and recommend your content!

## 📚 Resources

- **Jekyll Docs**: https://jekyllrb.com/docs/
- **Minimal Mistakes**: https://mmistakes.github.io/minimal-mistakes/
- **GitHub Pages**: https://docs.github.com/pages
- **Markdown Guide**: https://www.markdownguide.org/

## 🆘 Troubleshooting

### Build fails in GitHub Actions
- Check the Actions tab for error details
- Usually it's a typo in YAML front matter
- Make sure all dates are in YYYY-MM-DD format

### Site shows 404
- Make sure repository name is exactly `dheerajn.github.io`
- Check that GitHub Pages is enabled in Settings
- Wait a few minutes after first push

### Styling looks broken
- Check that `remote_theme` is set in `_config.yml`
- Make sure the GitHub Actions workflow completed successfully

## ✨ You're All Set!

Your personal website is ready to go. Just push it to GitHub and you'll be live!

Questions? Check the README.md or Jekyll documentation.

**Happy blogging!** 🎉
