# Ginner Zapata Portfolio

Personal portfolio for Ginner Zapata, a frontend engineer building fast, polished product experiences.

**Live site:** [ginnerzapata.github.io/portfolio](https://ginnerzapata.github.io/portfolio/)

## Overview

- Resume-backed professional experience from Vizzn and Elys Network.
- A typography-led editorial design system built with semantic CSS tokens and self-hosted Epilogue.
- Markdown Notes for learning in public, including future writing about Go and frontend engineering.
- Astro React integration ready for future interactive demos and portfolio apps.
- Static deployment to GitHub Pages through GitHub Actions.

## Stack

- [Astro](https://astro.build/)
- [React](https://react.dev/), configured for future interactive islands
- CSS custom properties and scoped Astro component styles
- [Epilogue](https://fonts.google.com/specimen/Epilogue), self-hosted with Fontsource
- GitHub Pages and GitHub Actions

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
