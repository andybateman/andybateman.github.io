# Andy Bateman Personal Website & Projects

<!-- Project metadata: read by the project tools, hidden when the README is rendered.
**Keywords:** personal website, Jekyll, GitHub Pages, static site, portfolio, www.andybateman.com, The Logbook theme, travel blog, kitjunkie archive, travel map, Leaflet, OpenTopoMap, Hanken Grotesk, IBM Plex Mono, Flickr photo albums, Wellington Hills, New Zealand Hills, Mohoe coffee map, Tape Deck pages, Terminal Logo Turtle
**Status:** Active
**Last Updated:** 2026-10-16
-->

A personal website and portfolio project featuring Jekyll-based static site generation, interactive games, and organised project management using the PARA method.

## Overview

This project contains the source code and assets for **www.andybateman.com**, a personal website showcasing work, projects, and interactive experiences. The site is built with Jekyll and hosted on GitHub Pages.

## Documents

| Document | What's in it |
|---|---|
| [CHANGELOG.md](CHANGELOG.md) | Every change, newest first |
| [_docs/STRUCTURE.md](_docs/STRUCTURE.md) | The project's folders, by the PARA method |
| [_docs/UPDATES.md](_docs/UPDATES.md) | The updates of June 2026 and before, from before the changelog took over |

## Key Features

### 🌐 Main Website
- **Technology:** Jekyll static site generator
- **Hosting:** GitHub Pages (andybateman.github.io)
- **Domain:** www.andybateman.com
- **Framework:** none, a small local utility and reset stylesheet (no Bootstrap)
- **Plugins:** jekyll-seo-tag, jekyll-sitemap, jekyll-redirect-from

### 🎮 Interactive Projects
- **Will's Superhero Adventure** (`will/hero/`) - Interactive text-based game with 9 different superhero personas
- **Spacle** (`will/spacle/`) - Solar system visualisation
- **Macaroon Game** (`will/macaroon/`) - Will's game with interactive elements
- **QR Code Generator** (`qr/`) - QR code generation page
- **Health Tracker** (`health/`) - Personal health tracking page
- **Terminal Logo Turtle** (`termlogo/`) - A Logo interpreter with turtle graphics running in the browser (the Python engine through Pyodide, loaded from the jsDelivr CDN). Static files built from [andybateman/termlogo](https://github.com/andybateman/termlogo): from that repository run `python3 tools/build_web.py --out ../andybateman.github.io/termlogo`, which replaces the folder. Live at `/termlogo/`
- **Tape Deck** (`tapedeck/`) - The features page and help for Tape Deck, the cassette music player for iPhone, iPad and Mac. Plain static files (`index.html`, `help.html`, `style.css`, `img/`) kept in step with [andybateman/tape-deck](https://github.com/andybateman/tape-deck)'s `site/tape-deck/`, where they're drafted; the screenshots come from its `docs/screens/`. Live at `/tapedeck/`

### 📍 Maps & Location-Based Content
All maps use **Leaflet + OpenTopoMap** (no Google Maps, no API keys).
- **Travel Map** (`travelmap/`) - Full journey; plots every geotagged story chronologically with a route line. Data injected from post front matter at build time.
- **New Zealand Hills** (`newzealandhills/`) - Elevation/distance charts (Chart.js + d3)
- **Wellington Hills** (`wellingtonhills/`) - Interactive map of hills to summit
- **Mohoe Coffee Map** (`mohoe/`) - Interactive Mojo coffee location tracker
- **Sam Nikiel** (`samnikiel/`) - Photo gallery

### 📖 Stories ("The Logbook")
- **`posts/`** - 57 travel-blog posts (as at 2026-10-15; 2001–2011), recovered from the original kitjunkie blog, presented as a chronological journey grouped by year
- Posts with coordinates show a per-post location mini-map (39 of 57 geotagged, as at 2026-10-15)

### 🎨 Design Assets
- Custom brand fonts (Batemans-Logos)
- Logo variations (SVG, AI, PNG)
- Photo assets and headshots
- Design files (PSD, LBX, AI)
- Historical design scrapbook

## Technology Stack

- **Static Site Generator:** Jekyll 4 (local) / GitHub Pages (live build)
- **Styling:** `custom.scss` (local utilities + reset, no Bootstrap); `map.css` for map pages; HTML minified in production via the `compress.html` layout
- **Type:** Hanken Grotesk (display) + IBM Plex Mono (data), via Google Fonts
- **Maps:** Leaflet + OpenTopoMap; charts via Chart.js + d3
- **Hosting:** GitHub Pages (auto-deploy on push to `master`)
- **SEO/build plugins:** jekyll-seo-tag, jekyll-sitemap, jekyll-redirect-from
- **Shared `<head>`:** `_includes/head.html` serves every page, branching on
  front-matter flags `map:` / `leaflet:` (map pages) vs content pages

## Getting Started

GitHub Pages builds and deploys the live site itself. For local work:

### Prerequisites
- Ruby 3.x+ (the macOS system Ruby 2.6 is too old). On this Mac, the Homebrew
  Ruby works: put it on PATH first.

### Local Development

```bash
cd andybateman.github.io
export PATH="/opt/homebrew/opt/ruby/bin:$PATH"
bundle install
bundle exec jekyll serve     # http://localhost:4000 (rebuilds on save)
bundle exec jekyll build     # one-off → _site/
```

### Linting

```bash
JEKYLL_ENV=production bundle exec jekyll build
bundle exec htmlproofer _site --disable-external --no-enforce-https \
  --checks "Links,Images,Scripts,Favicon,OpenGraph"
```

> **Note:** the `Gemfile` uses modern Jekyll 4 + `liquid ~> 4.0.4` rather than
> the `github-pages` gem, which pins a Jekyll too old to run on current Ruby.
> Output is equivalent for this site; the live build is unaffected (plugins are
> declared in `_config.yml`).

## Content

### Blog Posts
The site includes 57 blog posts (as at 2026-10-15; 2001–2011) covering:
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
- **Primary Colour:** #FBCA12 (Andy Bright Yellow)
- **Ink:** #1A1813 (near-black text)
- **Accent:** #C0392B (Marker Red, from the map pins; used for links, category tags, active nav)
- **Display face:** Hanken Grotesk · **Mono face:** IBM Plex Mono
- **Logo:** `images/logo.svg` (solid) + `images/logo-hover.svg` (outline on hover), from `ab-05.svg`
- **Personality:** Bold, creative, approachable, energetic

### Main Street Network Brand
- **Primary Colour:** #9ad17b (Main Street Green)
- **Secondary Colour:** #b1c0a2 (Main Street Sage)
- **Accent Colour:** #c9a2bf (Main Street Mauve)
- **Personality:** Technical, reliable, innovative, community-focused

## Project Management

This project uses the **PARA method** for organisation:
- **Projects:** Active work with clear endpoints
- **Areas:** Ongoing responsibilities and domains
- **Resources:** Reference material and assets
- **Archives:** Completed and inactive items

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

Active, and updated regularly.
