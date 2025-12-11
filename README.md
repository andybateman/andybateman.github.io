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

### 📍 Location-Based Content
- **New Zealand Hills** (`newzealandhills/`) - NZ walks and hiking information
- **Wellington Hills** (`wellingtonhills/`) - Wellington-specific walks
- **Sam Nikiel** (`samnikiel/`) - Photo gallery

### 🎨 Design Assets
- Custom brand fonts (Batemans-Logos)
- Logo variations (SVG, AI, PNG)
- Photo assets and headshots
- Design files (PSD, LBX, AI)
- Historical design scrapbook

## Technology Stack

- **Static Site Generator:** Jekyll
- **Styling:** SCSS with Bootstrap
- **Hosting:** GitHub Pages
- **Version Control:** Git
- **Build System:** Jekyll with plugins
- **SEO:** jekyll-seo-tag, jekyll-sitemap

## Getting Started

### Prerequisites
- Ruby 2.7+
- Jekyll 4.0+
- Bundler

### Installation

```bash
cd 1_Projects/Current\ Site/andybateman.github.io
bundle install
```

### Local Development

```bash
bundle exec jekyll serve
```

Visit `http://localhost:4000` to view the site locally.

### Building for Production

```bash
bundle exec jekyll build
```

The compiled site will be in the `_site/` directory.

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
- **Secondary Color:** #000000 (Andy Black)
- **Accent Color:** #FFFFFF (Pure White)
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

### Latest Changes
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

*Last Updated: 12 December 2025*
