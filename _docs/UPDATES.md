# Updates before the changelog

The README's "Recent Updates", moved word for word on 2026-10-15. Everything since is in `CHANGELOG.md` at the repository's root.

## Latest Changes (2026-06-30)
- **Type system modernised:** display → **Hanken Grotesk**, mono → **IBM Plex Mono** (replacing Bricolage Grotesque + Space Mono)
- **Health & Sam Nikiel** brought onto the shared head/Logbook theme; the Health chart migrated CanvasJS → Chart.js
- **Link audit:** fixed dead kitjunkie.org links (world-map → travel map, dead `/kit/` → `/posts/`, unwrapped dead pages), tidied the Spacle CDNs, and repointed 8 of 11 dead photo-gallery links to **Flickr**
- Removed dead Universal Analytics from NZ Hills and Sam Nikiel
- See the root `CHANGELOG.md` for the full 3.1.0 entry

## Latest Changes (2026-06-27)
- **Restored the story blog:** 57 travel posts (2001–2011) with a new readable layout
- **Added the Travel Map** (`travelmap/`) and per-post location maps; recovered 39 posts' coordinates
- **"The Logbook" theme:** new visual identity (Bricolage Grotesque + Space Mono, marker-red accent); `/posts/` redesigned
- **Unified the `<head>`** across all pages; map/chart pages now get fonts, GA4, SEO and favicon
- **Logo → SVG** (ab-05), replacing the base64 PNG sprite; fixed post titles that were rendering as the logo
- **Local builds fixed** (modern Jekyll Gemfile) and post content cleaned (mojibake, WordPress cruft, dead links)
- See the root `CHANGELOG.md` for the full 3.0.0 entry

## Previous Updates
- Reorganised project structure using PARA method
- Cleaned up and refactored Will's Superhero Adventure game code
- Improved code documentation and organisation
- Moved experimental projects to Features section
- Consolidated design assets and resources

## Game Code Improvements
- Added JSDoc comments throughout
- Organised code into logical sections
- Improved variable naming and clarity
- Used template literals for better readability
- Separated concerns (DOM, Logic, Configuration)
- Added configuration constants for magic numbers
