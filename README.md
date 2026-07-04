# CANOP Website

Static one-page site for cano.p — Sydney temporary housing coordination.

## Project structure

```
canop-website/
├── index.html          # the full site (nav, hero, sections, footer)
├── images/
│   ├── canop_logo.png  # included
│   ├── homelyvibes.jpg  # placeholder — add your property photo here
│   ├── cosycottage.jpg  # placeholder — add your property photo here
│   └── georgeshall.jpg  # placeholder — add your property photo here
└── README.md
```

Only `canop_logo.png` was available, so the three property photos referenced
in the "Our properties" section are missing. Drop matching files into
`images/` with those exact names (or update the `src` paths in `index.html`
around lines 952, 963, 974) and they'll appear.

## Opening in Cursor

1. Unzip/copy this `canop-website` folder anywhere on your machine.
2. In Cursor: **File → Open Folder…** and select `canop-website`.
3. Everything is in one file (`index.html`) with inline `<style>` — no
   build step, no dependencies. You can ask Cursor's chat/agent to edit
   sections directly (e.g. "update the hero headline" or "add a testimonials
   section").

## Previewing changes

Since it's a plain static file, open it right in a browser, or for
auto-reload on save:

- **VS Code/Cursor extension:** install "Live Server," right-click
  `index.html` → *Open with Live Server*.
- **No extension:** run `python3 -m http.server 8000` from this folder,
  then visit `http://localhost:8000`.

## Notes on links already wired into the page

- Booking call: `https://calendly.com/monhe/30min`
- Airbnb listings: Homely Vibes, Cosy Cottage Patch, Georges Hall (all live
  external links)
- Contact: `hello@canop.com.au`, `0473 777 017`
- Host registration currently points to `/hosts` — this page doesn't exist
  yet, so either build it or point the link at a form (e.g. Typeform/Google
  Form) until it does.

## Deploying later

Once you're happy with it in Cursor, the whole folder can be dropped as-is
onto any static host — Netlify, Vercel, GitHub Pages, or Cloudflare Pages
all work with zero configuration for a single `index.html`.
