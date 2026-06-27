# Changelog

All notable changes to the Andy Bateman Personal Website project are documented in this file.

## [Unreleased]

### Planned
- Convert the Mohoe coffee map to the shared head/theme
- Apply the type system to the home body and interactive games
- Performance: trim or subset Bootstrap; enable HTML compression

## [3.0.0] - 2026-06-27

### Added
- **Story blog restored** — 57 posts (2001–2011) recovered from the kitjunkie
  travel blog, with a new readable article layout
- **`/travelmap/`** — full-screen Leaflet/OpenTopoMap plotting every geotagged
  story chronologically with a route line and popups
- **Per-post location maps** — posts with `lat`/`lng` show a small map of where
  the story happened; 39 of 57 posts geotagged (coordinates recovered from the
  original WordPress export)
- **"The Logbook" theme** — distinctive visual identity: Bricolage Grotesque +
  Space Mono, brand yellow/ink with marker-red accent pulled from the map pins;
  `/posts/` rebuilt as a route-line journey grouped by year
- Shared `_includes/head.html` and `_includes/scripts.html`; `map.css` for map
  pages; `Gemfile` for working local builds (modern Jekyll, not `github-pages`)
- Recovered 4 kit-review photos from the 2018 backup (`images/posts/`)

### Changed
- Logo migrated from a ~50KB base64 PNG sprite to SVG (`images/logo.svg` +
  `logo-hover.svg`), later updated to the cleaner ab-05 pin
- Unified the `<head>` across all pages (content vs map) so the map/chart pages
  now get fonts, GA4, SEO and favicon they previously lacked
- Home masthead restyled (Bricolage brand, Space Mono nav) with a Stories link

### Fixed
- Post titles were rendering as the logo (global `h1` rule); scoped to the home
  hero only
- Story posts rendered unstyled (post layout was missing the Bootstrap CSS link)
  and used dead Universal Analytics / deprecated meta — brought to parity via the
  shared head
- Content cleanup across all posts: mojibake (`donâ€™t` → `don't`), WordPress
  front-matter cruft and exposed author emails removed, dead Flickr shortcodes
  resolved, broken image paths fixed

## [2.1.0] - 2025-12-30

### Added
- **Mohoe Coffee Map** (`mohoe/`) - Interactive Leaflet.js map for tracking Mojo coffee locations
  - 25 Mojo locations across Wellington, Auckland, and Christchurch
  - Interactive map with markers and popups
  - Sidebar with location list and progress statistics
  - New location highlighting (🆕 badges)
  - Visited/pending status tracking
- Navigation link to Mohoe map in main menu
- **iPhone-friendly responsive design**:
  - Mobile layout with sidebar at top (40vh max height)
  - Touch-optimized interactions (44px minimum tap targets)
  - Safe area support for notches and Dynamic Island
  - Momentum scrolling with `-webkit-overflow-scrolling`
  - Proper viewport configuration for iOS web app
  - Responsive breakpoint at 768px

### Changed
- Updated navigation to include Mohoe link
- Enhanced location-based content section in README
- Map responsive: desktop (side-by-side) and mobile (stacked)

### Discovered
- 4 new Mojo locations (total increased from 24 to 25):
  - Mojo AUT - Auckland
  - Mojo Quay - Auckland
  - Mojo CSB Hospital - Wellington
  - The Beanery by Mojo - Wellington

## [2.0.0] - 2025-12-12

### Added
- **PARA Project Structure:** Reorganized entire project using Projects, Areas, Resources, Archives method
- **Code Cleanup:** Refactored Will's Superhero Adventure game with improved documentation
- **Comprehensive README:** Added detailed project documentation
- **Changelog:** Implemented version tracking and change history
- **JSDoc Comments:** Added function documentation throughout codebase
- **Configuration Constants:** Centralized magic numbers and configuration values

### Changed
- **Code Organization:** Separated concerns (DOM manipulation, game logic, configuration)
- **CSS Structure:** Added section headers and improved visual hierarchy
- **Variable Naming:** Improved clarity and consistency throughout codebase
- **Template Literals:** Replaced string concatenation with modern JavaScript syntax
- **Game State Management:** Centralized game state in single object

### Improved
- Code readability and maintainability
- Function organization and structure
- CSS organization with clear sections
- Game logic flow and clarity
- Error handling and validation

## [1.5.0] - 2025-12-11

### Added
- Will's Superhero Adventure game (`will/hero/`)
  - 9 different superhero personas
  - Multiple story branches with win/fail scenarios
  - Stats tracking (decisions, victories, failures)
  - Terminal-style interface
  - Click-to-choose and keyboard input support
  - Responsive design for mobile devices

### Changed
- Reorganized project structure with `will/` namespace
- Moved macaroon game to `will/macaroon/`
- Moved spacle project to `will/spacle/`

## [1.4.0] - 2025-12-10

### Added
- Project generation script (`generate-all-projects.sh`)
- Raycast quicklinks integration
- Projects database (projects.json)
- Interactive Projects HTML dashboard

### Changed
- Updated project metadata tracking
- Improved last modified date tracking
- Enhanced project status detection

## [1.3.0] - 2025-11-15

### Added
- Health tracking page
- New Zealand hills walking guides
- Wellington hills walking information
- Enhanced navigation structure

### Changed
- Updated site styling and layout
- Improved responsive design
- Enhanced mobile experience

## [1.2.0] - 2025-10-01

### Added
- Satellite Phones project documentation
- Enhanced kit review section
- Additional travel content

### Changed
- Updated blog post organization
- Improved category structure
- Enhanced post metadata

## [1.1.0] - 2025-09-01

### Added
- QR code generation page
- Enhanced icon system
- Additional brand assets

### Changed
- Updated favicon and app icons
- Improved asset organization
- Enhanced CDN structure

## [1.0.0] - 2025-06-09

### Added
- Initial Jekyll site setup
- Basic site structure and layout
- Blog post system
- Navigation and menu
- Footer and header components
- Basic styling with Bootstrap
- SEO plugins and configuration
- Sitemap generation
- 404 error page

### Changed
- Initial project creation

## [0.9.0] - 2025-05-01

### Added
- Design assets and branding
- Logo variations
- Font files (Batemans-Logos)
- Photo assets
- Design templates

## [0.5.0] - 2025-04-01

### Added
- Project planning and structure
- Initial design concepts
- Branding guidelines
- Asset collection

---

## Version Numbering

This project follows [Semantic Versioning](https://semver.org/):
- **MAJOR** version for incompatible changes
- **MINOR** version for new functionality (backwards compatible)
- **PATCH** version for bug fixes

## How to Contribute

When making changes, please:
1. Update this CHANGELOG.md file
2. Follow the format: `### Added/Changed/Fixed/Removed`
3. Include date in ISO 8601 format (YYYY-MM-DD)
4. Commit with descriptive message

## Release Process

1. Update version number in relevant files
2. Update CHANGELOG.md with all changes
3. Create git tag: `git tag -a v1.0.0 -m "Release version 1.0.0"`
4. Push changes and tags: `git push origin master --tags`

---

**Last Updated:** 30 December 2025
**Current Version:** 2.1.0
**Status:** Active Development
