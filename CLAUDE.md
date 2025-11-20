# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based portfolio website showcasing professional iOS development experience. The site is hosted on GitHub Pages with a custom domain (www.acorderoperez.com) and built from the "Treat" Jekyll template by CloudCannon.

**Important Concept:** Posts in `_posts/` are project showcases, not chronological blog articles. The date in the filename controls sort order on the homepage, not the actual project timeline.

## Development Commands

### Setup
```bash
bundle install
```

### Local Development
```bash
bundle exec jekyll serve
```
Site will be available at `http://localhost:4000`

### Build for Production
```bash
bundle exec jekyll build
```
Output directory: `_site/`

### Common Issue
If you encounter `cannot load such file -- webrick (LoadError)`, the `webrick` gem (~> 1.8) is already in the Gemfile. Run `bundle install` to resolve.

## Architecture

### Layout Hierarchy
```
default.html (base layout with header/footer/sidebar)
  └── post.html (project detail pages)
```

All pages use a two-column layout: main content area + persistent author sidebar.

### Content Model

**Posts as Projects:** Each markdown file in `_posts/` represents a portfolio project entry.

**File naming:** `YYYY-MM-DD-project-name.md` (date determines homepage sort order)

**Front matter structure:**
```yaml
---
date: YYYY-MM-DD
title: Project Name - Short Description
categories:
  - Category Name
featured_image: ../images/project_logo.png
project:
  tech_stack_markdown: |-
    * **Architecture:** Details
    * **Tech Stack:** Technologies
    * **Tools:** Build tools
    * **Team Leadership:** Team composition
  key_features_markdown: |-
    1. **Feature Name:** Description
    2. **Feature Name:** Description
---
```

The `project` metadata has two required sections:
- `tech_stack_markdown`: Technical architecture and tools
- `key_features_markdown`: Numbered list of project highlights

### Category Organization

Projects are organized by categories (FinTech, Retail, E-Networking, Gaming, Immersive Technologies, Services). Categories generate separate landing pages and are displayed on the `/industries.html` page as an image grid.

### Data-Driven Components

- **Navigation menu:** `_data/navigation.yml`
- **Sidebar content:** `_data/sidebar.yml` (English) and `_data/sidebar-es.yml` (Spanish)
- **Company details:** `_data/company_details.yml` (logo, contact)

### Styling Architecture

Modular SCSS in `_sass/`:
- `variables.scss` - Color/font variables
- Component-specific files (navigation, sidebar, blog, forms, etc.)
- Main entry point: `css/screen.scss` imports all modules

## Key Configuration Files

### `_config.yml`
- Site metadata and SEO settings
- Pagination: 10 posts per page
- Plugin configuration (feed, seo-tag, sitemap, paginate)
- Default layouts for posts

### `Gemfile`
- Jekyll 4.3.2
- Essential plugins: jekyll-feed, jekyll-paginate, jekyll-seo-tag, jekyll-sitemap
- Webrick for local development

## Content Conventions

1. **Asset paths in front matter:** Use relative paths like `../images/filename.png`
2. **Image naming:** Project logos follow pattern `*_logo.{png,jpeg}`
3. **Achievement-focused writing:** Emphasize metrics, impact, and quantifiable results in post content
4. **Bilingual support:** Partially implemented - English is primary, Spanish versions exist for about page and sidebar

## Deployment

- **Main branch:** Production (auto-deployed via GitHub Pages)
- **Current working branch:** `feature/new-copies`
- Pushing to `main` triggers automatic deployment
- Custom domain configured via CNAME file

## Template Reuse

The `_posts/_defaults.md` file serves as a template for creating new project posts with the correct front matter structure.

## Optional Services (Currently Disabled)

- Google Analytics (no tracking key configured)
- Disqus comments (no shortname configured)
- MailerLite newsletter (not active)
- CloudCannon CMS (optional editor - site works without it)
