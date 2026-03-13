# CLAUDE.md

This file provides guidance for AI assistants (like Claude) working with this repository.

## Repository Overview

**iuhh.github.io** is a GitHub Pages static site repository. It is currently a minimal placeholder with no build system, framework, or significant content — just a bare HTML entry point served directly by GitHub Pages.

- **Owner:** Hui Li (hui@ybex.io)
- **Hosting:** GitHub Pages (served directly from the `master` branch root)
- **Created:** October 2020

## Repository Structure

```
iuhh.github.io/
├── index.html      # Site entry point ("Hello World" placeholder)
├── README.md       # Minimal project title
└── CLAUDE.md       # This file
```

## Technology Stack

- **No build system** — no npm, yarn, webpack, Vite, or any package manager
- **No frameworks** — no React, Vue, Angular, Jekyll, Hugo, or similar
- **No preprocessors** — no TypeScript, SASS, or Less
- **Pure static files** — content is served as-is by GitHub Pages

## Development Workflow

Since there is no build process, development is straightforward:

1. Edit files directly
2. Commit changes to `master`
3. Push to `origin/master` — GitHub Pages automatically serves the updated site

### Local Preview

Without a build system, you can preview locally by opening `index.html` directly in a browser, or using any simple HTTP server:

```bash
# Python 3
python3 -m http.server 8080

# Node.js (npx)
npx serve .
```

## Conventions

- **Entry point:** `index.html` must remain in the root directory (GitHub Pages requirement)
- **Branch:** The live site is served from `master`
- **No CI/CD:** There are no GitHub Actions or automated pipelines — pushes to `master` deploy immediately via GitHub Pages

## Expanding This Repository

If adding complexity, consider these common patterns for GitHub Pages:

- **Jekyll** (GitHub Pages native): Add `_config.yml` and use Liquid templating
- **Static site generators**: Hugo, Eleventy, Astro — typically require a GitHub Actions workflow to build and deploy
- **Vanilla HTML/CSS/JS**: Add assets in organized subdirectories (e.g., `css/`, `js/`, `assets/`)

If a build step is introduced, document it here and add a `package.json` or equivalent with a `build` script, and configure a GitHub Actions workflow at `.github/workflows/deploy.yml`.

## Key Notes for AI Assistants

- The repository is intentionally minimal — do not assume missing files are errors
- There is no linter, formatter, or test suite configured
- Changes to `index.html` directly affect the live site
- When adding new pages, use relative paths for links and assets
- If asked to "build" or "run" the project, note there is no build step — serve the static files directly
