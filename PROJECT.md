# Portfolio Project Context

## Purpose

This is Ginner Zapata's personal frontend portfolio for potential clients and hiring managers. It is an Astro static site deployed to GitHub Pages at `https://ginnerzapata.github.io/portfolio/`.

## Product Structure

- The homepage currently contains Home, Experience, About, and Contact sections.
- Experience lists three chronological roles: Vizzn Senior Web Developer, Elys Network Frontend Developer, and Vizzn Frontend Developer.
- Work will become an editorial index for case studies, experiments, and React apps. Keep it out of public navigation until it has real content.
- Notes are Git-managed Markdown files. Keep Notes out of public navigation until at least one non-draft Note exists.
- Contact uses `ginnerzapata@gmail.com` and `https://github.com/ginnerzapata`. Do not publish a phone number or a guessed LinkedIn URL.

## Design System

- Visual direction: a typography-led editorial portfolio, not a UI-library-driven marketing page.
- Font: self-hosted Epilogue through `@fontsource-variable/epilogue`.
- Source the palette from the Penpot local library:
  - `Color / Ink`: `#0D0F12`
  - `Surface / Canvas`: `#F2F0EA`
  - `Surface / Elevated`: `#406280`
  - `Text / Muted`: `#92979F`
  - `Border / Subtle`: `#406280`
  - `Status / Available`: `#8BA4FF`
- Define raw primitives and semantic tokens in `src/styles/global.css`. Components should consume semantic tokens, not raw hex values.
- Use custom CSS and scoped Astro component styles. Tailwind remains installed for possible future React apps, but it is not the portfolio's styling system.
- Maintain WCAG 2.2 AA behavior: semantic markup, keyboard access, visible focus, and reduced-motion support.
- Keep the mobile hero heading at a more generous line height than desktop to avoid Epilogue glyph overlap.

## Technical Decisions

- React is configured for future interactive demos. Do not add a React island unless the interaction needs it.
- Use CSS transitions for simple portfolio motion. Motion is reserved for future React apps or genuinely stateful interactions.
- Notes live in `src/content/notes/`; `draft: true` entries must not be published.
- The `NN` placeholder has been replaced by `public/ginner.svg`. Keep the logo inside an accessible home link with empty image alt text.
- Keep internal asset and route URLs compatible with Astro's `/portfolio` GitHub Pages base path.

## Deployment

- `.github/workflows/deploy.yml` deploys pushes to `main` through GitHub Actions.
- GitHub repository Pages settings must use **GitHub Actions** as the source.
- Before finishing a change, run `node_modules/.bin/astro build`.
