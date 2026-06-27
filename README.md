# Andy Bateman Personal Website & Projects

A comprehensive personal website and portfolio project featuring Jekyll-based static site generation, interactive games, and organized project management using the PARA method.

## Overview

This project contains the source code and assets for **www.andybateman.com**, a personal website showcasing work, projects, and interactive experiences. The site is built with Jekyll and hosted on GitHub Pages.

## Project Structure

```
20200609_AndyBateman/
├── 1_Projects/
│   ├── Current Site/
│   │   └── andybateman.github.io (Active Jekyll site)
│   ├── Features/
│   │   ├── playground.andybateman.com (Experimental projects)
│   │   └── signpost (Interactive signpost application)
│   └── Content Updates/
│
├── 2_Areas/
│   ├── Branding/
│   ├── Design System/
│   ├── Content/
│   └── Performance & SEO/
│
├── 3_Resources/
│   ├── Design Assets/
│   │   ├── Logos (SVG, AI files)
│   │   ├── Fonts (glyphter, transfonter)
│   │   ├── Photos (headshots, passport, etc.)
│   │   ├── Design files (PSD, LBX, AI)
│   │   └── Scrapbook/ (historical designs)
│   ├── Documentation/
│   │   ├── Resumes (all versions)
│   │   ├── Spreadsheets (Calendar, Travel, Walks, Pay)
│   │   ├── Speech files
│   │   └── Database files
│   └── Templates/
│       └── Themeforest template
│
└── 4_Archives/
    ├── Old Versions/
    │   ├── also_not_current
    │   ├── not_current
    │   └── www (original www folder)
    ├── Backups/
    │   └── backups (GitLab backups, SQL dumps, etc.)
    └── Deprecated/
```

## Key Features

### 🌐 Main Website
- **Technology:** Jekyll static site generator
- **Hosting:** GitHub Pages (andybateman.github.io)
- **Domain:** www.andybateman.com
- **Framework:** Bootstrap SCSS
- **Plugins:** jekyll-seo-tag, jekyll-sitemap, jekyll-redirect-from

### 🎮 Interactive Projects
- **Will's Superhero Adventure** (`will/hero/`) - Interactive text-based game with 9 different superhero personas
- **Spacle** (`will/spacle/`) - Solar system visualization
- **Macaroon Game** (`will/macaroon/`) - Will's game with interactive elements
- **QR Code Generator** (`qr/`) - QR code generation page
- **Health Tracker** (`health/`) - Personal health tracking page

### 📍 Maps & Location-Based Content
All maps use **Leaflet + OpenTopoMap** (no Google Maps, no API keys).
- **Travel Map** (`travelmap/`) - Full journey; plots every geotagged story chronologically with a route line. Data injected from post front matter at build time.
- **New Zealand Hills** (`newzealandhills/`) - Elevation/distance charts (Chart.js + d3)
- **Wellington Hills** (`wellingtonhills/`) - Interactive map of hills to summit
- **Mohoe Coffee Map** (`mohoe/`) - Interactive Mojo coffee location tracker
- **Sam Nikiel** (`samnikiel/`) - Photo gallery

### 📖 Stories ("The Logbook")
- **`posts/`** - 57 travel-blog posts (2001–2011), recovered from the original kitjunkie blog, presented as a chronological journey grouped by year
- Posts with coordinates show a per-post location mini-map (39 of 57 geotagged)

### 🎨 Design Assets
- Custom brand fonts (Batemans-Logos)
- Logo variations (SVG, AI, PNG)
- Photo assets and headshots
- Design files (PSD, LBX, AI)
- Historical design scrapbook

## Technology Stack

- **Static Site Generator:** Jekyll 4 (local) / GitHub Pages (live build)
- **Styling:** `custom.scss` + Bootstrap 5.3.3 (CDN); `map.css` for map pages
- **Type:** Bricolage Grotesque (display) + Space Mono (data), via Google Fonts
- **Maps:** Leaflet + OpenTopoMap; charts via Chart.js + d3
- **Hosting:** GitHub Pages (auto-deploy on push to `master`)
- **SEO/build plugins:** jekyll-seo-tag, jekyll-sitemap, jekyll-redirect-from
- **Shared `<head>`:** `_includes/head.html` serves every page, branching on
  front-matter flags `map:` / `leaflet:` (map pages) vs content pages

## Getting Started

GitHub Pages builds and deploys the live site itself. For local work:

### Prerequisites
- Ruby 3.x+ (the macOS system Ruby 2.6 is too old). On this Mac, the Homebrew
  Ruby works — put it on PATH first.

### Local Development

```bash
cd andybateman.github.io
export PATH="/opt/homebrew/opt/ruby/bin:$PATH"
bundle install
bundle exec jekyll serve     # http://localhost:4000 (rebuilds on save)
bundle exec jekyll build     # one-off → _site/
```

> **Note:** the `Gemfile` uses modern Jekyll 4 + `liquid ~> 4.0.4` rather than
> the `github-pages` gem, which pins a Jekyll too old to run on current Ruby.
> Output is equivalent for this site; the live build is unaffected (plugins are
> declared in `_config.yml`).

## Content

### Blog Posts
The site includes 50+ blog posts covering:
- Travel experiences (Tahiti, Fiji, New Zealand, Australia, Malaysia, Nepal)
- Kit reviews and gear recommendations
- Personal updates and life events
- Wedding and family milestones

### Pages
- **Home** - Main landing page
- **Posts** - Blog archive
- **Health** - Health tracking and recovery information
- **Kit** - Gear and equipment reviews
- **Walks** - New Zealand hills and walking guides

## Branding

### Andy Bateman Brand
- **Primary Color:** #FBCA12 (Andy Bright Yellow)
- **Ink:** #1A1813 (near-black text)
- **Accent:** #C0392B (Marker Red — from the map pins; used for links, category tags, active nav)
- **Display face:** Bricolage Grotesque · **Mono face:** Space Mono
- **Logo:** `images/logo.svg` (solid) + `images/logo-hover.svg` (outline on hover), from `ab-05.svg`
- **Personality:** Bold, creative, approachable, energetic

### Main Street Network Brand
- **Primary Color:** #9ad17b (Main Street Green)
- **Secondary Color:** #b1c0a2 (Main Street Sage)
- **Accent Color:** #c9a2bf (Main Street Mauve)
- **Personality:** Technical, reliable, innovative, community-focused

## Project Management

This project uses the **PARA method** for organization:
- **Projects:** Active work with clear endpoints
- **Areas:** Ongoing responsibilities and domains
- **Resources:** Reference material and assets
- **Archives:** Completed and inactive items

## Recent Updates

### Latest Changes (2026-06-27)
- **Restored the story blog** — 57 travel posts (2001–2011) with a new readable layout
- **Added the Travel Map** (`travelmap/`) and per-post location maps; recovered 39 posts' coordinates
- **"The Logbook" theme** — new visual identity (Bricolage Grotesque + Space Mono, marker-red accent); `/posts/` redesigned
- **Unified the `<head>`** across all pages; map/chart pages now get fonts, GA4, SEO and favicon
- **Logo → SVG** (ab-05), replacing the base64 PNG sprite; fixed post titles that were rendering as the logo
- **Local builds fixed** (modern Jekyll Gemfile) and post content cleaned (mojibake, WordPress cruft, dead links)
- See `CHANGELOG.md` for the full 3.0.0 entry

### Previous Updates
- Reorganized project structure using PARA method
- Cleaned up and refactored Will's Superhero Adventure game code
- Improved code documentation and organization
- Moved experimental projects to Features section
- Consolidated design assets and resources

### Game Code Improvements
- Added comprehensive JSDoc comments
- Organized code into logical sections
- Improved variable naming and clarity
- Used template literals for better readability
- Separated concerns (DOM, Logic, Configuration)
- Added configuration constants for magic numbers

## Deployment

The site is automatically deployed to GitHub Pages when changes are pushed to the master branch.

### Manual Deployment
```bash
git add .
git commit -m "Update: description of changes"
git push origin master
```

## Contributing

This is a personal project. For suggestions or improvements, please contact Andy Bateman.

## License

All content and code in this project are proprietary and belong to Andy Bateman unless otherwise noted.

## Contact

- **Website:** https://www.andybateman.com
- **Email:** andy@andybateman.com
- **Twitter:** @andybateman

## Status

**Status:** Active

This project is actively maintained and updated regularly.

---

*Last Updated: 27 June 2026*
