# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is an academic website for Madduri Lab built using the **al-folio** Jekyll theme. The site focuses on computational science, AI, and biomedical research at Argonne National Laboratory.

## Development Commands

### Local Development

Using Docker (recommended):
```bash
docker compose pull
docker compose up
```

Visit `http://localhost:8080` to see the site. Changes are automatically rendered in real-time.

Slim Docker image (smaller size):
```bash
docker compose -f docker-compose-slim.yml up
```

### Building and Testing

```bash
# Build the site
bundle exec jekyll build

# Serve locally without Docker
bundle exec jekyll serve

# Run pre-commit checks
pre-commit run --all-files

# Format code with Prettier
npx prettier --write .
```

### Debugging Docker Issues

```bash
docker compose up -d
docker compose logs
docker compose exec -it jekyll /bin/bash
./bin/entry_point.sh
```

## Site Configuration

- Main config: `_config.yml`
- Site URL: https://madduri.github.io/madduri-lab
- Base URL: `/madduri-lab` (subpath for GitHub Pages)

Key settings in `_config.yml`:
- Collections: `books`, `news`, `projects`
- Jekyll Scholar for bibliography management
- Multiple Jekyll plugins for extended functionality

## Content Architecture

### Collections

The site uses Jekyll collections for different content types:

- **`_pages/`**: Core pages (about, CV, publications, etc.)
- **`_posts/`**: Blog posts
- **`_news/`**: News items displayed on homepage
- **`_projects/`**: Research projects with thumbnails
- **`_books/`**: Book reviews
- **`_bibliography/`**: BibTeX files for publications (papers.bib)

### Layouts

Custom Liquid layouts in `_layouts/`:
- `about.liquid`: Homepage/about page
- `bib.liquid`: Bibliography entries
- `cv.liquid`: CV page
- `distill.liquid`: Distill-style posts
- `post.liquid`: Blog posts
- `profiles.liquid`: People/profiles page

### Data Files

YAML data in `_data/`:
- `cv.yml`: CV content (fallback if JSON resume not found)
- `citations.yml`: Publication citations
- `coauthors.yml`: Collaborator information
- `repositories.yml`: GitHub repos to display
- `socials.yml`: Social media links
- `venues.yml`: Publication venues

## Bibliography Management

Jekyll Scholar plugin manages publications:
- Source: `_bibliography/papers.bib`
- Style: APA
- Auto-generates publications page from BibTeX
- Supports metadata: abstract, arxiv, code, pdf, poster, slides, etc.
- Filters by author: Madduri, Ravi, K.

Update citations:
```bash
python bin/update_scholar_citations.py
```

## Deployment

The site uses GitHub Pages with automatic deployment:

1. Push to `main` branch
2. GitHub Actions builds site and pushes to `gh-pages` branch
3. GitHub Pages serves from `gh-pages`

Manual deployment:
```bash
./bin/deploy
```

## Theme Features

This is based on al-folio theme with:
- Light/dark mode toggle
- Responsive design with Bootstrap
- MathJax for equations
- Syntax highlighting
- Image lazy loading
- Collections for organizing content
- Jekyll Scholar for bibliography
- Search functionality
- Social media previews

## Code Quality

Pre-commit hooks check:
- Trailing whitespace
- End-of-file fixers
- YAML validity
- Large files

Prettier formats:
- Liquid templates (via @shopify/prettier-plugin-liquid)
- HTML, CSS, JavaScript

## Key Files to Modify

- `_config.yml`: Site settings, plugins, collections
- `_pages/about.md`: Homepage content
- `_bibliography/papers.bib`: Publications
- `_data/cv.yml`: CV content
- `_news/*.md`: News items
- `_projects/*.md`: Project descriptions
- `assets/`: Images, PDFs, CSS, JS

## Plugin Architecture

Heavy use of Jekyll plugins (see Gemfile):
- `jekyll-scholar`: Bibliography management
- `jekyll-archives-v2`: Archive pages
- `jekyll-feed`: RSS/Atom feed
- `jekyll-minifier`: Asset minification
- `jekyll-toc`: Table of contents
- `jemoji`: Emoji support

Some plugins like `jekyll-terser` use custom forks from GitHub.
