# Changelog

All notable changes to the Andy Bateman Personal Website project are documented in this file.

## [Unreleased]

### Planned
- Enhanced mobile responsiveness for all interactive games
- Additional superhero personas for Will's game
- Performance optimization for image assets
- SEO improvements and metadata updates

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

**Last Updated:** 12 December 2025
**Current Version:** 2.0.0
**Status:** Active Development
