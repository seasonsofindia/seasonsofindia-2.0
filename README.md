# Seasons of India

An interactive static website for a modern Indian fine-dining experience in Orlando. The page combines seasonal menu content, accessible navigation, responsive layouts, and a cinematic Three.js atmosphere.

## What it includes

- Menu items loaded from `menu-items.json`.
- Category ordering controlled by `menu-misc.json`.
- Search, category filtering, and tag filtering.
- Responsive two-column menu presentation on larger screens.
- FAQ content, anchor navigation, reduced-motion support, and a WebGL fallback.

## How it is made

This is a deliberately small static site. `index.html` contains the document structure, CSS, menu rendering, procedural scene construction, scroll choreography, and interaction logic. A vendored Three.js build provides the visual atmosphere without a package manager or build step.

## Run locally

From the repository root, run:

```bash
python3 -m http.server 4173 --bind 127.0.0.1
```

Then visit [http://127.0.0.1:4173/](http://127.0.0.1:4173/).

The JSON files must be served over HTTP; opening `index.html` directly with a `file://` URL can prevent the menu data from loading.

## Deploy

The project can be deployed as-is to Netlify, GitHub Pages, or any static hosting provider.

For Netlify:

```text
Build command: leave empty
Publish directory: .
```

There is no build step, environment variable, analytics script, or runtime network dependency.

## Project structure

```text
seasonsofindia-2.0/
├── index.html
├── menu-items.json
├── menu-misc.json
├── PROMPT.md
├── assets/
└── secret-pathways-assets/
```

## Attribution

The vendored Three.js runtime retains its MIT license notice and copyright attribution. Site-specific artwork and content belong to Seasons of India.
