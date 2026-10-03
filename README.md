# Himesh Vats · 3D walk-through portfolio

Static site: `index.html` + `assets/`. Three.js 0.169 loads from jsDelivr via an import map, so there is no build step.

## Run locally
The GLB is fetched, so open it through a server, not file://
    npx serve .        # or: python3 -m http.server

## Deploy
Any static host works (Cloudflare Pages, GitHub Pages, Netlify). Upload the folder as is.

## Where to change things
- Projects and copy: the `<section class="stop">` blocks in index.html. Keep the 7 sections in order; each is one waypoint.
- Path the character walks: `PTS` (one point per section).
- Camera angle per section: `RIGS` (a = ahead of him, b = to his right, c = height, la/lb/lc = look-at, fov, shift = where he sits on screen).
- 3D objects at each waypoint: the "Stations" block (3D knot, data bars, AI network, phones, photo frames, portal).
- Glow strength: `UnrealBloomPass(..., strength, radius, threshold)`.

3D character: "Male Phone Walking (40 frames loop)" by Denys Almaral, Sketchfab Standard license (credit kept in the footer).

## Themes
Dark and light are both built in. It follows the visitor's OS setting until they use the moon/sun toggle, which is remembered. Scene colours live in `PAL`; page colours are the CSS tokens at the top.
