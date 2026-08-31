# Common Ground — starter site

A simple Jekyll site for GitHub Pages. Two topics out of the box: **Sharia Law** and **Formal State Law**.

## Structure

- `_config.yml` — site title, description, and settings
- `_posts/` — every article lives here as a `.md` file named `YYYY-MM-DD-title.md`
- `_layouts/` — HTML templates (`default`, `page`, `post`)
- `index.md`, `about.md`, `topics.md`, `guidelines.md` — the site's pages
- `assets/css/style.css` — all the styling, in one file

## Add an article

Create a new file in `_posts/`, e.g. `_posts/2026-09-01-my-article.md`:

```
---
layout: post
title: "Your title"
date: 2026-09-01
categories: [sharia-law]   # or [state-law]
---

Your article, written in Markdown.
```

It appears automatically on the homepage and on the Topics page — nothing else to update.

## Add a third topic

1. Pick a slug, e.g. `custom-law`.
2. In `topics.md`, copy one of the two topic blocks and change the category and heading.
3. In `_layouts/post.html`, add an `{% elsif %}` branch for the new category.
4. In `index.md`, add the matching `{% if %}` line and a new topic card.

## Customize

- Site name & description: `_config.yml`
- Colors, fonts, spacing: the `:root` variables at the top of `assets/css/style.css`
- Nav links: `_layouts/default.html`

## Deploy

This should live in its **own repository**, separate from any other GitHub Pages site you run — one repo can only serve one site from its root. In `_config.yml`, set `baseurl` to `/your-repo-name` unless this is your `username.github.io` root repo, in which case leave it blank.
