# SPIQE Website - Claude Code Notes

## Project Overview
Hugo-based website for the SPIQE 2026 workshop (Secure Protocol Implementations in the Quantum Era), co-located with Euro S&P in Lisbon, Portugal, July 6-10, 2026.

## Architecture & Key Decisions

### Tech Stack
- **Hugo** v0.152.2 static site generator
- **Bootstrap 5.3.3** (local/offline, no CDN)
- **Tilt Warp font** (local, Google Fonts)
- **Custom theme** in `themes/spiqe/`

### Design Choices
- Hero banner with purple tiled background (`tiles.png`)
- Three-column hero layout: Title (42%) | Subtitle (33%) | Location/CTA (25%)
- Tilt Warp font used for: hero title, hero subtitle, navbar brand
- Sticky navbar with Bootstrap styling
- Full-width hero banner, constrained content area for main text
- Hero banner enabled on both homepage and CFP page
- CFP page kept simple and functional (no extra beautification)
- Floating Lisbon image on homepage to highlight location

### Image Credits
- **Lisbon photo** (`img/lisbon.png`): Photo by [Ekaterina Boltaga](https://unsplash.com/@shkipp) on [Unsplash](https://unsplash.com/photos/jqkGK3ofxi8)

### File Structure
```
content/
  _index.md       - Homepage with hero config
  cfp.md          - Call for Papers with hero config
static/
  2025/           - Previous year's static HTML (relative links)
themes/spiqe/
  assets/css/main.css           - Custom styles
  layouts/
    baseof.html                 - Base template
    home.html                   - Homepage template
    page.html                   - Page template (includes hero support)
    _partials/
      hero.html                 - Hero banner component
      header.html               - Navbar
      footer.html               - Footer
  static/
    css/bootstrap.min.css       - Bootstrap CSS
    js/bootstrap.bundle.min.js  - Bootstrap JS
    fonts/tilt-warp.woff2       - Custom font
    img/tiles.png               - Hero background
```

### Git Repository
- Remote: `git@github.com:lambdafu/spiqe.git`
- Main branch: `main`
- All changes committed with descriptive messages

### Deployment & Domain
- Domain: `spiqe.cool`
- HotCRP instance: `hot26.spiqe.cool`
- No analytics/tracking (keeping it simple, avoiding EU privacy law complexity)

## Future Improvements

### Landing Page Beautification (Priority)
- [ ] Add section-based layout with distinct visual sections
- [ ] Implement alternating background styles/colors for sections while scrolling
- [ ] Increase base font size for better readability
- [ ] Overall visual polish and modern design improvements
- [ ] Consider distinct sections for:
  - About/Introduction
  - Important Dates
  - Organizers
  - Latest Updates
- [ ] Maintain visual hierarchy and breathing room between sections

**Important:** Keep CFP page simple and functional - focus beautification efforts on landing page only.

### Other Potential Improvements
- [ ] Add paper submission button linking to HotCRP at hot26.spiqe.cool
- [ ] Review site for accessibility problems (WCAG compliance, screen readers, keyboard navigation, etc.)
- [ ] Add contact email or form for inquiries
- [ ] Add venue/travel information (beyond just city name)
- [ ] Add registration information when available
- [ ] Better integration/linking of previous workshop (static/2025)
- [ ] Add favicon
- [ ] Add meta tags for social sharing (og:image, twitter:card, etc.)

## Completed Work

### Bootstrap Integration
- [x] Downloaded and integrated Bootstrap 5.3.3 locally
- [x] Removed conflicting theme CSS
- [x] Updated all layouts to use Bootstrap components

### Hero Banner
- [x] Created hero partial with responsive layout
- [x] Integrated Tilt Warp font
- [x] Added purple tiled background
- [x] Made full-width with proper breakout CSS
- [x] Added co-location information display
- [x] Enabled on both homepage and CFP page

### Content & Structure
- [x] Converted hugo.toml to hugo.yaml
- [x] Converted LaTeX CFP to Markdown
- [x] Fixed static/2025 links (absolute → relative)
- [x] Removed blog/post functionality from theme
- [x] Created navigation menu structure
- [x] Added .gitignore for Hugo project

### Git & Deployment
- [x] Set up git repository
- [x] Connected to GitHub remote
- [x] All work committed and pushed

## Notes for Future Sessions
- Hugo server runs on port 1313
- Use `hugo server --bind 0.0.0.0` for network access
- Bootstrap classes available for quick styling
- Hero configuration in page front matter (YAML)
