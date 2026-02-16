# AGENTS.md

This repository uses GitHub Pages with Jekyll + Minimal Mistakes, with the site source in `docs/`.

## Build/Publish Basics

- GitHub Pages source is `docs/` (not repo root).
- Anything outside `docs/` will not publish on Pages.
- Do not manually edit `docs/_site/` (generated output).
- Local build command: `bundle exec jekyll build` from `docs/`.

## Theme + Color Decisions (Current)

- Main CTA buttons (`.btn--primary`) use:
  - Default: `#e17f38`
  - Hover/Focus: `#c97534`
  - Text: white
  - Visited state stays orange (not gray)
- Page background is white.
- Team role subtext (e.g., "Controls Focus") is black.
- Dark outline helper button class exists: `.roam-btn--dark-outline`.

## Hero (Landing) Decisions

- Home hero supports video via custom include override:
  - `docs/_includes/page__hero.html`
- Front matter key in `docs/index.md`:
  - `header.overlay_video: "/assets/videos/landing-hero.mp4"`
- Video behavior:
  - autoplay, muted, loop, playsinline
  - 16:9 treatment with larger hero area
  - caption anchored at bottom of hero

## Team Section Decisions

- Team cards use hover/focus detail overlays.
- Hover cards currently show detail text only (no headshots).
- Team group image appears under the "Meet the Team" kicker.

## Gallery Decisions

- Gallery page: `docs/gallery.md`
- Gallery styling + lightbox CSS: `docs/assets/css/main.scss`
- Click-to-enlarge lightbox is implemented on gallery images.
- Keep image filename case exact in markup (GitHub Pages is case-sensitive).
- If an image does not render, verify:
  - file exists under `docs/assets/images/gallery/`
  - file extension/case in `gallery.md` exactly matches file on disk
  - HTML attributes are well-formed (no malformed `alt`/`loading` attributes)

## Content Conventions

- Keep descriptions concise and project-focused.
- Use absolute site paths in markup (e.g., `/assets/images/...`).
- Prefer adding media in `docs/assets/images/gallery/` and then wiring in `docs/gallery.md`.

## Common Pitfalls Encountered

- Putting media in repo root `Documentation/` does not publish; copy into `docs/` path.
- Theme defaults can override button colors (`:visited` especially).
- Windows can hide case-sensitivity issues that break on GitHub Pages.
