# Migration Guide - Replace Existing GitHub Pages Site

## Current Situation ✅ Understood

- **Existing repo**: `dheerajn.github.io` (contains besafe.json)
- **Separate repo**: `Plainly` (privacy page at `/Plainly/privacy/`)
- **Goal**: Replace main site with new personal website, keep Plainly working

## What Will Happen

**After migration**:
- ✅ `dheerajn.github.io` → Your new personal website
- ✅ `dheerajn.github.io/Plainly/privacy/` → Still works! (separate repo, untouched)
- ✅ `besafe.json` → Preserved in new site

**Your app's privacy page will NOT break** - it's hosted from a different repository.

## Migration Steps

### Option 1: Clean Migration (Recommended)

This replaces the repository completely while preserving the history.

```bash
# 1. Navigate to your new site
cd ~/Desktop/dheerajn.github.io

# 2. Connect to your existing GitHub repository
git remote add origin https://github.com/dheerajn/dheerajn.github.io.git

# 3. Fetch existing repo (to preserve any history)
git fetch origin

# 4. Force push your new content
# This replaces everything but keeps the repository
git push -u origin main --force
```

### Option 2: Manual Migration (If you prefer)

```bash
# 1. Clone your existing repo
cd ~/Desktop
git clone https://github.com/dheerajn/dheerajn.github.io.git dheerajn-existing

# 2. Remove old content (keep .git folder)
cd dheerajn-existing
rm -rf * .*  # Don't worry, .git is hidden and won't be deleted
ls -la      # You should see .git directory

# 3. Copy new site content
cp -r ~/Desktop/dheerajn.github.io/* .
cp ~/Desktop/dheerajn.github.io/.gitignore .
cp ~/Desktop/dheerajn.github.io/.github .

# 4. Commit and push
git add .
git commit -m "Replace with new personal website"
git push
```

## Verify After Migration

After pushing, check:

1. **GitHub Actions**: Go to Actions tab - should see build running
2. **Wait 2-3 minutes** for deployment
3. **Test URLs**:
   - https://dheerajn.github.io → Your new personal site ✅
   - https://dheerajn.github.io/Plainly/privacy/ → Still works ✅
   - https://dheerajn.github.io/besafe.json → Still accessible ✅

## Configure GitHub Pages (If Needed)

If the site doesn't deploy automatically:

1. Go to repository **Settings** → **Pages**
2. Under **Source**, select **GitHub Actions**
3. Save and wait for deployment

## Rollback (If Needed)

If something goes wrong, you have a backup:

```bash
# Your old site is backed up at:
cd ~/Desktop/dheerajn.github.io-backup

# To restore it:
cd ~/Desktop/dheerajn.github.io-backup
git push origin main --force
```

## Next Steps After Migration

1. **Update your info**:
   - Edit `_data/social.yml` with your LinkedIn/Twitter
   - Edit `pages/about.md` with your bio
   - Add profile picture to `assets/images/profile.jpg`

2. **Test the site**:
   - Visit https://dheerajn.github.io
   - Check navigation works
   - Verify Plainly privacy page still works

3. **Start writing**:
   - Add blog posts to `_posts/`
   - Add TIL entries to `_til/`
   - Add projects to `_projects/`

## FAQ

**Q: Will my app's privacy page break?**
A: No! It's in a separate repository (`Plainly`), so it's completely independent.

**Q: What happens to besafe.json?**
A: It's preserved in the new site at `/besafe.json`.

**Q: Can I undo this?**
A: Yes! You have a backup at `~/Desktop/dheerajn.github.io-backup/`

**Q: How long does deployment take?**
A: Usually 2-3 minutes after pushing to GitHub.

**Q: Do I need to update my app?**
A: No! The privacy page URL stays exactly the same.

## Ready to Migrate?

I recommend **Option 1** (Clean Migration) - it's simpler and faster.

Just run those 4 commands and your new site will be live!

---

**Need help?** Let me know if anything doesn't work as expected.
