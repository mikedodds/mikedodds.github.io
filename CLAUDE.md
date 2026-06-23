# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Mike Dodds' personal academic website (publications, talks, blog posts), built on the [Academic Pages](https://github.com/academicpages/academicpages.github.io) Jekyll template and hosted on GitHub Pages.

## Toolchain & Local Development

### Ruby version (important)

The site is pinned to **Jekyll 3.10.x** through the `github-pages` gem (see `Gemfile`). This gem deliberately locks Jekyll and all plugins (currently `github-pages` 232 → jekyll 3.10.0, liquid 4.0.4) to the exact versions GitHub Pages' classic build runs, so a local build matches production.

The catch: this frozen stack does **not** run on modern Ruby. Two failure modes seen with recent Rubies:
- **Ruby 3.4+** removed `csv`, `base64`, `logger`, etc. from the standard library → `LoadError: cannot load such file -- csv`.
- **Ruby 3.2+** removed `Object#tainted?`, which older `liquid` calls → `NoMethodError: undefined method 'tainted?'`. (Current liquid 4.0.4 is fine, but a stale `Gemfile.lock` can pin an older liquid that isn't.)

**Use Ruby 3.3.x**, which is what GitHub Pages runs (3.3.4). Do not use Homebrew's default `ruby` (4.x) directly. The idiomatic setup on macOS:

```bash
brew install rbenv
rbenv init          # then follow its instruction to update ~/.zshrc and restart the shell
rbenv install 3.3.5
rbenv local 3.3.5   # writes .ruby-version, pinning just this project (gitignored)
ruby -v             # confirm 3.3.x
```

Notes:
- `.ruby-version` is gitignored (local-only pin), as is `Gemfile.lock` — so `bundle install` resolves fresh. If you ever hit the `tainted?` error, delete a stale `Gemfile.lock` and re-run `bundle install` to pull current gems.
- `bundle install` needs network + a writable Ruby env; it can fail under a restrictive sandbox.

### Build and serve

```bash
# Install Ruby dependencies (needs network + writable Ruby env)
bundle install

# Install Node.js dependencies (only needed when rebuilding JS assets)
npm install

# Serve the site locally with live-reload; available at http://localhost:4000
bundle exec jekyll serve -l -H localhost
```

Always run Jekyll via `bundle exec` so the pinned (production-matching) version is used, not a stray global install.

### Using Docker

Docker is an alternative that avoids the local Ruby setup. There's a `Dockerfile`, a `docker-compose.yaml`, and a VS Code `.devcontainer/`. Compose is simplest:

```bash
docker compose up        # builds and serves at http://localhost:4000
```

Compose uses `_config_docker.yml` as an overlay on `_config.yml`.

### Rebuilding JavaScript assets

JS is pre-built and committed as `assets/js/main.min.js`. Only rebuild if you change source JS:

```bash
npm run build:js     # uglify + minify into assets/js/main.min.js
npm run watch:js     # rebuild on change
```

## Site Architecture

### Jekyll Collections
- `_posts/` - Blog posts (dated)
- `_publications/` - Academic publications (hand-maintained markdown)
- `_talks/` - Talks and presentations (hand-maintained markdown)
- `_teaching/` - Teaching materials
- `_pages/` - Static pages (About, CV, publications/talks index pages)

Note: the `portfolio` collection exists in `_config.yml` but is unused — it has no entries and is commented out of `_data/navigation.yml`.

### Theme Structure
`_layouts/`, `_includes/`, `_sass/`, and `assets/` are stock Academic Pages template code with no local edits — refer to the upstream repo for their structure. `_data/` holds YAML config; `_data/navigation.yml` controls the nav bar.

The template has a **theme/skin system**: `_config.yml`'s `site_theme` key selects a skin (`default`, `air`, `sunrise`, `mint`, `dirt`, `contrast`), each with light/dark variants under `_sass/theme/`. This site uses `default`.

The **favicon** is Mike's custom headshot icon at the repo root (`/favicon.ico`), referenced from `_includes/head/custom.html`. It lives at root (not `images/`) so the browser's implicit `/favicon.ico` probe resolves.

### Configuration
- `_config.yml` - Main Jekyll config (site settings, author info, collections, `site_theme`). **Restart the Jekyll server after editing — it is not live-reloaded.**
- `Gemfile` - Ruby gem dependencies (pins Jekyll via `github-pages`; plugins include `jekyll-redirect-from`, which powers `redirect_from:` front matter).
- `package.json` - Node dependencies for the JS asset build.

## Content Management

**Publications and talks are maintained by hand** as individual markdown files in `_publications/` and `_talks/`. Add or edit those files directly — do **not** use the `markdown_generator/` scripts (see note below). The simplest way to add an entry is to copy an existing recent file and edit its front matter and body.

### Adding a publication
1. Create `_publications/YYYY-MM-DD-slug.md` (date prefix = publication/submission date).
2. Front matter fields (match existing entries):
   - `title:` (double-quoted)
   - `collection: publications`
   - `category:` — one of `conferences`, `preprints`, `manuscripts`, `misc`
   - `permalink: /publications/YYYY-MM-DD-slug` (must match the filename, **with** date prefix and **with** a leading slash)
   - `date: YYYY-MM-DD`
   - `venue:` (spelled-out venue name with acronym, e.g. `"Programming Language Design and Implementation (PLDI)"`)
   - `paperurl:` (the canonical DOI/arXiv URL)
3. Body: an `**Abstract:**` paragraph, then a final footer line linking the DOI and any hosted PDF, e.g.:
   `DOI: <https://doi.org/...>, Paper: [PDF](https://mikedodds.github.io/files/publications/YYYY-MM-DD-slug.pdf)`
4. If hosting the PDF, place it at `files/publications/YYYY-MM-DD-slug.pdf` (filename matching the markdown slug).

### Adding a talk
Create `_talks/YYYY-MM-DD-slug.md` mirroring an existing talk's front matter. Use zero-padded dates (`YYYY-MM-DD`) and a permalink of `/talks/YYYY-MM-DD-slug` with a leading slash.

### Adding a blog post
Create `_posts/YYYY-MM-DD-title.md`:
```yaml
---
title: 'Post Title'
date: YYYY-MM-DD
permalink: /posts/YYYY/MM/title/
tags:
  - tag1
  - tag2
---
```

### File organization
- Hosted papers/PDFs go in `files/` (e.g. `files/publications/`, `files/talks/`).
- Images go in `images/`.

### About `markdown_generator/` (stale — do not use)
This directory contains the template's original Python/Jupyter scripts for generating publication and talk pages from CSV/TSV/BibTeX data. **It is abandoned and not part of the build.** The `*.tsv`/`*.csv` files contain only the template's example rows and are wildly out of sync with the real, hand-maintained publications (~37 entries in `_publications/`). Nothing invokes these scripts at build time. Do not regenerate content from them — you would overwrite the real entries with placeholder data.

## Deployment

The site deploys automatically to GitHub Pages on push to `master` (classic Pages build — there is no GitHub Actions deploy workflow). No manual deployment step.

**Important — never break existing URLs.** Changes to permalinks, filenames, or site structure must preserve existing page URLs (publications, talks, posts) to maintain link integrity and search rankings. Treat permalink/filename changes on already-published pages as needing explicit confirmation, even when they look like simple consistency fixes.
