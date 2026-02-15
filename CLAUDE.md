# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Personal academic website for Claudio Sole, built with [al-folio](https://github.com/alshedivat/al-folio) (Jekyll theme). Hosted on GitHub Pages at https://jcsole.github.io.

## Build & Serve Commands

```bash
# Preview locally (requires Ruby, Bundler, Jekyll)
bundle install
bundle exec jekyll serve

# Or using Docker
docker compose up
```

## Architecture

### Project Structure

```
.
├── _config.yml          # Main Jekyll config (site metadata, social links, plugins)
├── _pages/              # Site pages (about, blog, publications, projects, teaching)
│   ├── about.md         # Home page (/ permalink, uses about layout)
│   ├── blog.md          # Blog listing page
│   ├── publications.md  # Publications page (uses Jekyll Scholar + BibTeX)
│   └── projects.md      # Projects page
├── _bibliography/
│   └── papers.bib       # BibTeX file for publications
├── _data/               # YAML data files
│   ├── cv.yml           # CV data
│   ├── coauthors.yml    # Coauthor links
│   ├── venues.yml       # Publication venue URLs
│   └── repositories.yml # GitHub repos to display
├── _projects/           # Project pages (Markdown)
├── _news/               # News/announcements
├── _posts/              # Blog posts
├── _includes/           # Liquid template partials
├── _layouts/            # Page layouts
├── _sass/               # SCSS styles
├── assets/
│   ├── img/             # Images (prof_pic.jpg is profile photo)
│   ├── pdf/             # Publication PDFs
│   └── json/resume.json # JSON Resume data
└── .github/workflows/   # GitHub Actions for deployment
```

### Key Configuration

- **`_config.yml`**: Site title (Claudio Sole), social links (GitHub, LinkedIn, Google Scholar, ResearchGate), Jekyll Scholar settings, plugin list
- **Jekyll Scholar**: Renders publications from `_bibliography/papers.bib`, highlights author name "Sole"
- **Collections**: `_news`, `_projects` are Jekyll collections defined in `_config.yml`

### Adding Content

**New blog post**: Create `_posts/YYYY-MM-DD-title.md` with front matter (layout, title, date, description, tags)

**New publication**: Add BibTeX entry to `_bibliography/papers.bib`. Use `selected={true}` to show on home page.

**New project**: Create `_projects/N_project.md` with front matter (layout, title, description, category, importance)

### Deployment

GitHub Actions workflow deploys on push to master. Uses Jekyll build + GitHub Pages.
