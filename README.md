# Ginner Zapata Portfolio

An Astro portfolio deployed as a static GitHub Pages site. It uses semantic CSS tokens, reusable Astro components, and Markdown Notes.

## Development

```sh
pnpm install
pnpm dev
pnpm build
```

## Writing Notes

Create a Markdown file in `src/content/notes/` with this frontmatter:

```md
---
title: "Your note title"
description: "A short description for readers and search engines."
publishedAt: 2026-09-08
tags: [Go, Learning]
draft: false
---

Your article content goes here.
```

Set `draft: true` to keep a Note out of production. A published file is available at `/portfolio/notes/<filename>/`.

## Deployment

Pushes to `main` deploy through `.github/workflows/deploy.yml`. In the repository settings, set **Pages > Source** to **GitHub Actions**.
