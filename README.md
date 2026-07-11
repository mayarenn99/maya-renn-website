# Maya Renn — personal website

A soft, warm, minimal static site for Maya Renn (virtual lifestyle creator). Built with [Eleventy](https://www.11ty.dev/), deploys to Netlify.

## Pages

- `/` — home (hero, latest journal entries, rituals)
- `/about/` — bio, AI-transparency note, press list, contact
- `/blog/` — journal listing
- `/links/` — link-in-bio page for Instagram etc.

## ✍️ Adding a blog post (the part you'll do most)

Create a new `.md` file in `src/posts/`, e.g. `src/posts/2026-07-20-my-new-post.md`:

```markdown
---
title: My new post
description: One sentence that appears in the blog list and on the home page.
date: 2026-07-20
---

Write your post here in plain Markdown. **Bold**, *italic*, lists, and
> quotes all work.
```

That's it. The blog page, home page, and the post's own page all update automatically on the next build. Netlify rebuilds whenever you push to your git repo.

## Running locally

```
npm install
npm start
```

Then open http://localhost:8080. The site live-reloads as you edit.

## Deploying to Netlify

1. Push this folder to a GitHub repo.
2. In Netlify: **Add new site → Import an existing project**, pick the repo.
3. Netlify reads `netlify.toml` automatically (build: `npm run build`, publish: `_site`). Just click Deploy.

After that, every git push publishes the site.

## Photos of Maya

Site photos live in `src/images/` (`maya-hero.jpg` on the home page, `maya-about.jpg` on the about page, `maya-avatar.jpg` on the links page). To change one, just replace the file — keep images under ~200 KB for fast loading (resize to ~1600px max). The `object-position` style on each `<img>` controls which part of the photo stays visible in the crop.

## Editing site-wide details

Social URLs, email, tagline, and site description live in one file: `src/_data/site.json`.

## Colors & fonts

All colors are CSS variables at the top of `src/css/style.css` (`--cream`, `--mauve`, etc.). Fonts are Fraunces (headings) + Karla (body) from Google Fonts.
