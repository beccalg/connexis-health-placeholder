# Connexis Health — Placeholder Site

A minimal "more information coming soon" placeholder. No navigation, no
internal links, no content meant to be indexed — this is intentionally a
single static screen ahead of the real site launching on Wix.

## Structure

```
index.html              The deployable page
styles.css               Its styles (colors/type/spacing as CSS variables)
assets/logo.png          Logo, used as the page's primary content
Connexis Placeholder v2.dc.html   Claude Design canvas source (editable at claude.ai/design)
support.js                Claude Design's canvas runtime — only needed to
                           preview/edit the .dc.html file in Claude Design,
                           not part of the deployed site
```

`index.html` + `styles.css` + `assets/logo.png` is the whole deployable
site — everything else is design-source material kept for reference and
future edits.

## Why it's built this way

- **Not searchable on purpose.** `<meta name="robots" content="noindex,
  nofollow, noarchive, nosnippet, noimageindex">` tells every crawler to
  skip it. There's no meta description either — nothing here is meant to
  rank.
- **Image-led.** The logo/wordmark is the primary content, not text run
  through SEO copywriting.
- **Responsive.** Fluid image sizing, `clamp()`-based spacing, and a
  layout that works from small phones to wide desktops.
- **Extensible.** Colors, fonts, and spacing live as CSS custom
  properties in `styles.css` so the look can change without touching
  markup, and the HTML is plain/semantic enough to build on when the
  real site replaces it.

## Wix migration

This static version isn't hosted from this repo — it exists so the
design is version-controlled and easy to hand off. When rebuilding in
Wix: reuse `assets/logo.png` as the hero image, and carry over the
palette (`#17365c` navy, `#0f7b73` teal, `#4a5560` body text, `#fcfcfb`
background) and the Jost typeface (Google Fonts).

A full launch kit — the asset, copyable brand values and exact copy
text, and step-by-step instructions for both Wix's Coming Soon mode and
a manual single-page build — is at:
https://claude.ai/code/artifact/cdb21512-88fe-4b72-8df5-fd924176a2b5

## Editing the design source

The `.dc.html` files are Claude Design canvases — open this project at
[claude.ai/design](https://claude.ai/design) to edit them visually, or
edit `index.html`/`styles.css` directly for the deployable version.
