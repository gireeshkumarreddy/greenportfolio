# Gireesh — a designer's working desk

A responsive, six-page UI/UX portfolio inspired by a green cutting mat and tactile studio stationery. Serve the `dist` directory with any static web server. There is no build step or runtime dependency. Links use root-relative paths.

The homepage lives in `dist/index.html`; the archive and biography are `dist/work.html` and `dist/about.html`. Three complete case studies live in `dist/projects/`. Shared styles and interactions are in `dist/styles.css`, `dist/expanded.css`, and `dist/app.js`. Optimized original imagery and self-hosted fonts live in `dist/assets`.

Project descriptions and experience are illustrative portfolio copy. Contact uses the illustrative address `hello@gireesh.design`; replace this address in index.html with the real address before sharing publicly.

Includes full project navigation, archive filters, keyboard-operable experience tabs, pause-motion preference, pointer parallax, draggable stationery, off-screen object entrances, directional card reveals, a scroll-scrubbed three-step process scene, interactive typography and color experiments, and reduced-motion support. The process sequence renders as a normal readable stack when motion is paused.

Animation uses native CSS transforms and requestAnimationFrame. The scroll sequence follows ordinary page scroll and does not capture wheel or touch scrolling. Reveal positions are measured before transform effects, so cards entering from outside the viewport can still be triggered reliably.

## Run locally

Serve the static output with Python:

```sh
python3 -m http.server 8080 --directory dist
```

Open `http://localhost:8080`. Use a web server rather than opening HTML files directly, because the pages use root-relative links.

## Deploy

This is a complete static site with no package installation, build step, API keys, or external asset dependencies. Set the host's publish/output directory to `dist`, leave the build command empty, and serve its contents from the domain root. Keep the `projects` and `assets` directories intact.

All six pages, original project visuals used on the site, stationery cutouts, local fonts, styles, and JavaScript animations are included. The `.openai/hosting.json` file records the existing Sites publication; a standard static host does not need it.
