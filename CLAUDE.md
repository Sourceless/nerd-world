# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

A Jekyll static site for a West Marches D&D campaign called "Nerd World", deployed to GitHub Pages at `https://Sourceless.github.io/nerd-world/`. There is no local build toolchain — the site is built and deployed entirely by GitHub Actions on every push to `main`.

## Deployment

Push to `main`. GitHub Actions runs `.github/workflows/pages.yml`, which uses `actions/jekyll-build-pages` to build and `actions/deploy-pages` to publish. The site is live within ~2 minutes. No Gemfile, no local Ruby setup, no npm.

## Architecture

- **`_config.yml`** — `baseurl: /nerd-world` (project repo, not user repo). All internal links must use Jekyll's `| relative_url` filter or they will break.
- **`_sass/nerd-world.scss`** — all styles in one file. Entry point is `assets/css/main.scss` (just `@import "nerd-world"`).
- **`_layouts/`** — four layouts: `default` (base), `home` (front page), `page` (wraps content in `.parchment` div), `post` (session reports with front matter metadata).
- **`_includes/`** — `head.html` (Google Fonts + CSS), `header.html` (sticky nav), `footer.html`.
- **`_posts/`** — session reports. Filename must be `YYYY-MM-DD-short-title.md`. Permalink pattern: `/sessions/:year/:month/:day/:title/`.

## Session report front matter

```yaml
layout: post
title: "Title"
date: YYYY-MM-DD
dm: "Name"
players:
  - "Player One"
location: "In-world location"
xp_awarded: 300
tags: [dungeon, combat]
```

All fields except `layout`, `title`, and `date` are optional but render in the post header if present.

## Content pages

Each static page (`rules.md`, `characters.md`, etc.) uses `layout: page` which wraps content in a `.parchment` div (cream background, crimson headings). `index.md` uses `layout: home` for the dark hero + quickstart layout. `sessions.md` uses `layout: default` (no parchment) to render the post listing against the dark background.

## Campaign rules (avoid contradicting these)

- Characters are mercenaries — jobs for gold is the premise
- Standard Array only for ability scores (`15, 14, 13, 12, 10, 8`)
- New replacement characters start at average party level (rounded down)
- Sessions are strictly self-contained — no multi-session arcs
- Sessions run on the third Saturday, 3–6 hours
- Healing potions as bonus action is the only mechanical house rule
- DMs post session reports as Google Docs to the Messenger group (not via GitHub)
