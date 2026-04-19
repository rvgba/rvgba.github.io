# rvgba.github.io — Personal Website

Personal website of **Ravi Garibaldi Akbar**, built with [Jekyll](https://jekyllrb.com/) and hosted on [GitHub Pages](https://pages.github.com/).

## 🚀 Deploying to GitHub Pages

### First-time setup

1. Make sure your repository is named `rvgba.github.io`
2. Push this entire folder as the repo's `main` branch
3. Go to **Settings → Pages** in your GitHub repo
4. Set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`
5. GitHub will automatically build and deploy — your site will be live at `https://rvgba.github.io` within ~2 minutes

### Subsequent updates

Just commit and push changes to `main` — GitHub Pages rebuilds automatically.

```bash
git add .
git commit -m "Update: describe what you changed"
git push origin main
```

---

## ✍️ Writing a New Blog Post

### Step 1 — Create a new file

Blog posts live in `_posts/`. Filename format is **required**:

```
_posts/YYYY-MM-DD-slug-of-post-title.md
```

Example: `_posts/2025-05-12-redesigning-merchant-onboarding.md`

### Step 2 — Add front matter

Copy the template from `_posts/NEW_POST_TEMPLATE.md` and fill it in:

```yaml
---
layout: post
title: "Your Post Title"
date: 2025-05-12 08:00:00 +0700
category: "PMO"
reading_time: 4
excerpt: "One or two sentences summarizing the post."
---
```

Available categories: `PMO`, `Design`, `Personal`, `Tech`, `Indonesia` — or make your own.

### Step 3 — Write in Markdown

Write the body of the post in standard Markdown below the `---` front matter block.

### Step 4 — Commit and push

```bash
git add _posts/2025-05-12-your-post.md
git commit -m "Post: Your Post Title"
git push origin main
```

Your post will be live in ~1-2 minutes.

---

## 🎨 Adding Design Works

Design works are managed via a data file — no code needed.

### Step 1 — Add your image (optional)

Place your image in `assets/images/design/`. Recommended size: **800×600px** or wider, JPG or PNG.

### Step 2 — Edit `_data/design_works.yml`

Add an entry at the bottom (or reorder as you like):

```yaml
- title: "Your Project Name"
  type: "Illustration"           # Editorial Design / Illustration / Branding / UI/UX / etc.
  year: "2025"
  description: "A brief description of the project."
  image: "/assets/images/design/your-image.jpg"   # Leave "" for placeholder
  link: "https://example.com"    # Leave "" if no external link
  tags: ["Illustration", "Print"]
```

### Step 3 — Commit and push

```bash
git add _data/design_works.yml assets/images/design/
git commit -m "Design: Add [project name]"
git push origin main
```

---

## 📁 File Structure

```
rvgba.github.io/
├── _config.yml          ← Site settings (title, email, resume URL, etc.)
├── _layouts/
│   ├── default.html     ← Main site layout (nav + footer)
│   └── post.html        ← Blog post layout
├── _posts/
│   ├── NEW_POST_TEMPLATE.md   ← Copy this to write new posts
│   └── YYYY-MM-DD-*.md        ← Your blog posts
├── _data/
│   └── design_works.yml ← Manage your design portfolio here
├── assets/
│   ├── css/style.css    ← All styles
│   ├── profile.jpg      ← Your profile photo
│   └── images/design/   ← Design work images go here
├── index.html           ← Home page
├── blog/index.html      ← Blog listing
├── about/index.html     ← About Me + Resume
├── design/index.html    ← Design Works gallery
├── Gemfile              ← Ruby dependencies (for local dev)
└── README.md            ← This file
```

---

## 💻 Local Development (Optional)

To preview changes before pushing:

```bash
# Install Ruby and Bundler first (see jekyllrb.com/docs/installation/)
bundle install
bundle exec jekyll serve
# Open http://localhost:4000
```

---

## ⚙️ Customization

### Update personal info
Edit `_config.yml`:
- `title` — your name
- `description` — site meta description
- `author.email` — your email
- `author.linkedin` — your LinkedIn URL
- `resume_url` — link to your resume PDF

### Update profile photo
Replace `assets/profile.jpg` with your photo. Keep the filename the same, or update the reference in `index.html`.

### Change skills on Home page
Edit the skills section in `index.html`.

### Update About Me content
Edit `about/index.html` — the experience entries are plain HTML, easy to update.

---

Built with ❤️ and Jekyll. Theme designed for Ravi Garibaldi Akbar.
