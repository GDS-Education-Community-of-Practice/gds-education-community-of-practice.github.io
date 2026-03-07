# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

All the updates should be incremental and minimal and only what content change is being asked of you. Always test to make sure the changes you made work visually for both desktop and mobile screens.

## Project Overview

This is the website for the **Data Science Education Community of Practice (DSECOP)** that supports physics educators in integrating data science into undergraduate curricula. The live site is at **dsecop.org**.

## Build & Serve

This project requires **Ruby 3.2.6** via `rbenv` (pinned in `.ruby-version`). Ensure `rbenv` is initialized in your shell (`eval "$(rbenv init - zsh)"` in `~/.zshrc`). The system Ruby and Homebrew Ruby 4.x are **not compatible** with the `github-pages` gem.

```bash
bundle install          # Install dependencies (first time / after Gemfile changes)
bundle exec jekyll serve   # Local dev server at http://localhost:4000
bundle exec jekyll build   # Build static site to _site/
```

Uses the `github-pages` gem, so the site builds identically on GitHub Pages. No custom CI/CD — pushing to the `gh-pages` branch deploys automatically.

## Architecture

**Jekyll static site** using Bootstrap 3, based on the [Allan Lab](http://www.allanlab.org/) theme.

### Data-driven content (`_data/`)

Most content updates happen by editing YAML files, not page templates:

| File | Purpose | Used by |
|------|---------|---------|
| `news.yml` | News feed items (date + headline with markdown links) | `_includes/news.html`, `_pages/allnews.md` |
| `pis.yml` | Principal Investigators (name, photo, info, website, email, aff) | `_pages/team.md` |
| `fellows.yml` | 2022 Fellows cohort | `_pages/team.md` |
| `fellows_2023.yml` | 2023 Fellows cohort | `_pages/team.md` |
| `speakers.yml` | Webinar speakers (name, bio, photo) | `_pages/webinars.md` |
| `social.yml` | Social media links (id, href, title, fa-icon) | `_pages/resources.md` |

### Layouts (`_layouts/`)

All layouts extend `default.html` which includes head, header (navbar), content, and footer.

- **`homelay`** — Two-column: content (col-8) + news sidebar (col-4)
- **`gridlay`** — Full-width (col-12), used for webinars, workshops, team
- **`textlay`** — Full-width, used for resources page
- **`team`** — Similar to gridlay, for team page variants
- **`page`** / **`post`** — Standard page/post layouts

### Pages (`_pages/`)

Pages use front matter with `permalink` for clean URLs. Key pages: home (`/`), webinars (`/webinars/`), workshops (`/workshops/`), team (`/team/`), resources (`/resources`), fellowship (`/fellowship/`). Also includes `404.md` and `allnews.md`.

### Custom plugin (`_plugins/markdown.rb`)

Provides a `{% markdown filename %}` Liquid tag that reads from `_includes/`, processes Liquid, then renders Kramdown. Note: custom plugins don't run on GitHub Pages — this may only work locally.

### Styling

- SASS in `_sass/` imports Bootstrap
- Custom styles in `css/main.scss` (navbar spacing, grid overrides, image styling)
- Uses `<pubtit>` custom element for bold speaker/publication titles

### Assets

- `images/teampic/` — Team member photos (referenced by `photo` field in YAML data files)
- `images/eventpic/` — Speaker/event photos
- `images/logopic/` — Sponsor logos
- `assets/22_Workshop/`, `assets/23_Workshop/` — Workshop slide PDFs and materials
- `fonts/` — Glyphicons for Bootstrap 3

## Common Tasks

**Add a news item:** Prepend to `_data/news.yml` with `date` and `headline` fields. Headlines support inline markdown.

**Add a team member:** Add entry to `_data/fellows.yml` (or `fellows_2023.yml`) with fields: `name`, `photo`, `info`, `bio`, `website`, `email`, `aff`, `title`. Place photo in `images/teampic/`.

**Add a webinar/workshop:** Edit `_pages/webinars.md` or `_pages/workshops.md` directly — these are content-heavy markdown pages with inline HTML for Bootstrap grid layouts.

## Conventions

- The team page uses a modulo-2 Liquid loop pattern to render members in two-column Bootstrap rows
- Workshop/webinar pages mix raw HTML (Bootstrap grid `<div class="row">`, `<div class="col-sm-6">`) with markdown content
- Kramdown is configured with `parse_block_html: true` to allow markdown inside HTML blocks
- `.ruby-version` pins Ruby 3.2.6 for rbenv — do not change without verifying `github-pages` gem compatibility
- The deploy branch is `gh-pages` (also the default/main branch)
