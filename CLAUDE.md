# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Mike Dodds' personal academic website (publications, talks, blog posts), built on the [Academic Pages](https://github.com/academicpages/academicpages.github.io) Jekyll template and hosted on GitHub Pages.

## Toolchain & Local Development

### Ruby version (important)

The site is pinned to **Jekyll 3.9.0** through the `github-pages` gem (see `Gemfile`). This gem deliberately locks Jekyll and all plugins to the exact versions GitHub Pages' classic build runs, so a local build matches production.

The catch: Jekyll 3.9.0 is incompatible with **Ruby 3.4+** (which removed `csv`, `base64`, `logger`, etc. from the standard library — Jekyll 3.9 `require`s them unconditionally and crashes with `LoadError: cannot load such file -- csv`).

**Use Ruby 3.3.x**, which is also what GitHub Pages runs. Do not use Homebrew's default `ruby` (currently 4.x) directly. The idiomatic setup on macOS:

```bash
brew install rbenv
rbenv init          # then follow its instruction to update ~/.zshrc and restart the shell
rbenv install 3.3.5
rbenv local 3.3.5   # writes .ruby-version, pinning just this project
ruby -v             # confirm 3.3.x
```

Note: `Gemfile.lock` is gitignored, so `bundle install` resolves fresh each time.

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

A `Dockerfile` is provided as an alternative that avoids the local Ruby setup:

```bash
docker build -t jekyll-site .
docker run -p 4000:4000 --rm -v $(pwd):/usr/src/app jekyll-site
```

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
`_layouts/`, `_includes/`, `_sass/`, and `assets/` are stock template code with only minor local edits — refer to the upstream repo for their structure. `_data/` holds YAML config; `_data/navigation.yml` controls the nav bar.

### Configuration
- `_config.yml` - Main Jekyll config (site settings, author info, collections). **Restart the Jekyll server after editing — it is not live-reloaded.**
- `Gemfile` - Ruby gem dependencies (pins Jekyll via `github-pages`)
- `package.json` - Node dependencies for the JS asset build

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
This directory contains the template's original Python/Jupyter scripts for generating publication and talk pages from TSV/BibTeX data. **It is abandoned and not part of the build.** The `*.tsv` files contain only the template's example rows (a few lines) and are wildly out of sync with the ~37 real, hand-maintained publications. Nothing invokes these scripts at build time. Do not regenerate content from them — you would overwrite the real entries with placeholder data.

## Deployment

The site deploys automatically to GitHub Pages on push to `master` (classic Pages build — there is no GitHub Actions deploy workflow). No manual deployment step.

**Important — never break existing URLs.** Changes to permalinks, filenames, or site structure must preserve existing page URLs (publications, talks, posts) to maintain link integrity and search rankings. Treat permalink/filename changes on already-published pages as needing explicit confirmation, even when they look like simple consistency fixes.
