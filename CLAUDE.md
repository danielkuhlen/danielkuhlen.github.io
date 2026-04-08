# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Academic personal website for Daniel Kuhlen, built with Jekyll using the [al-folio](https://github.com/alshedivat/al-folio) theme. Deployed to GitHub Pages at `danielkuhlen.github.io`.

## Build & Development Commands

```bash
# Local development with Docker (recommended)
docker compose up
# Serves at http://localhost:8080 with live reload

# Local Ruby development
bundle install
bundle exec jekyll serve --port=8080 --livereload

# Production build
JEKYLL_ENV=production bundle exec jekyll build

# Purge unused CSS (runs post-build in CI)
npx purgecss --config purgecss.config.js

# Format code with Prettier
npx prettier --check .
npx prettier --write .
```

## Code Formatting

Prettier with the Shopify Liquid plugin. Config in `.prettierrc`:
- Print width: 150
- Trailing comma: ES5
- Plugin: `@shopify/prettier-plugin-liquid`

## Architecture

**Static site generator**: Jekyll builds from source into `_site/`. Templates use Liquid syntax (`.liquid` and `.md` files with YAML front matter).

**Key directories:**
- `_pages/` — Top-level site pages (about, cv, publications, software, workingpapers)
- `_posts/` — Blog posts (named `YYYY-MM-DD-title.md`)
- `_projects/` — Project pages (named `N_project.md` for ordering)
- `_news/` — News items shown on home page
- `_bibliography/papers.bib` — BibTeX file for publications (rendered by jekyll-scholar)
- `_data/` — YAML data files (socials, cv, repositories, coauthors, software, venues)
- `_layouts/` — Page templates (Liquid)
- `_includes/` — Reusable template partials (Liquid)
- `_sass/` — SCSS stylesheets (`_themes.scss` for colors, `_variables.scss` for sizing)
- `_plugins/` — Custom Ruby Jekyll plugins
- `assets/` — Static files (images, JS, CSS, PDFs, fonts, JSON)

**Configuration**: `_config.yml` controls site metadata, theme settings, navbar, collections, and plugin options.

## Content Conventions

**Front matter** for posts:
```yaml
---
layout: post
title: Title Here
date: YYYY-MM-DD HH:MM:SS
description: Short description
tags: tag1 tag2
categories: category-name
---
```

**Publications** are managed via `_bibliography/papers.bib` (BibTeX format) and auto-rendered by jekyll-scholar.

**CV data** lives in `assets/json/resume.json` (JSON Resume format) with `_data/cv.yml` as fallback.

## Deployment

Automatic via GitHub Actions (`.github/workflows/deploy.yml`) on push to `main`. The workflow builds with Jekyll, runs PurgeCSS, and deploys to the `gh-pages` branch.
