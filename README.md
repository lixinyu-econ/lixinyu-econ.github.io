# Academic website

A simple Jekyll site that GitHub Pages builds for you automatically. It has a home page with your photo and bio, plus Research, Supervision, Teaching, Blog and Chinese (中文) pages. No coding is needed to update it.

## Put it online (about 10 minutes)

1. Create a **public** GitHub repository named `yourusername.github.io`.
2. On the repo page, click **Add file → Upload files**, drag in *everything inside this folder* (including the `_layouts`, `_data`, `_posts`, `assets`, `blog` and `zh` folders), and click **Commit changes**.
3. Go to **Settings → Pages** and check that the source is **Deploy from a branch**, branch `main`, folder `/ (root)`.
4. Wait a minute or two, then visit `https://yourusername.github.io`.

## What to edit

| To change… | Edit this file |
|---|---|
| Name, title, email, photo, profile links, site URL | `_config.yml` |
| Bio, research interests, editorial roles, appointments, education, contact/addresses | `_data/cv.yml` (Home page section) |
| Working papers, publications, grants, projects | `_data/cv.yml` (Research page section) |
| Students and supervision note | `_data/cv.yml` (Supervision page section) |
| Courses | `_data/cv.yml` (Teaching page section) |
| Chinese page | `zh/index.md` |
| Menu items and their order | `_data/navigation.yml` |
| Colors and fonts | `assets/css/style.css` |

You can edit any file directly on GitHub: open it, click the pencil icon, then **Commit changes**. The site updates within a minute or two.

**Photo:** upload your headshot, e.g. `assets/photo.jpg`, then set `photo: /assets/photo.jpg` in `_config.yml`. A square image of at least 320×320 pixels looks best.

**CV PDF:** upload your CV as `assets/cv.pdf`, or clear `cv_pdf` in `_config.yml` to hide the link.

**Paper PDFs:** upload them to `assets/papers/` and link them in `_data/cv.yml`, e.g. `links: [{ label: PDF, url: /assets/papers/my-paper.pdf }]`.

**Removing a page:** delete its line from `_data/navigation.yml` and delete its file (e.g. `zh/index.md` for the Chinese page).

**Adding a page:** create a file like `talks.md` in the main folder that starts with

```markdown
---
layout: default
title: Talks
permalink: /talks/
---
# Talks

Written in Markdown.
```

then add `- title: Talks` / `url: /talks/` to `_data/navigation.yml`.

## Writing a blog post

Create a file in `_posts/` named `YYYY-MM-DD-short-title.md`, for example `_posts/2026-10-15-notes-from-the-archive.md`:

```markdown
---
layout: post
title: "Notes from the archive"
tags: [research]
---

Your post, written in Markdown.
```

Posts appear on `/blog/` grouped by year, newest first, and the three most recent show on the home page. An RSS feed is at `/feed.xml`. Delete `_posts/2026-09-28-welcome.md` once you've written your own.

## Custom domain (optional)

In **Settings → Pages → Custom domain**, enter your domain, then add a `CNAME` DNS record pointing to `yourusername.github.io` with your domain registrar. Update `url` in `_config.yml` to match.

## Preview on your own computer (optional)

With Ruby installed: `bundle install`, then `bundle exec jekyll serve`, then open http://localhost:4000.
