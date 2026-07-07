# Bargavi Sivaraman — Portfolio

Personal portfolio site. Live at **https://bargavi-codes.netlify.app/**

## Structure

```
bargavi-portfolio/
├── index.html                # the whole site (single page)
├── assets/
│   └── images/               # all images live here, one file each
│       ├── profile.jpg
│       ├── favicon.png
│       ├── nasa-jpl-logo.png
│       ├── research-*.jpg    # lab / CSUNposium gallery
│       ├── award-*.jpg
│       └── team-*.jpg
├── netlify.toml              # deploy + caching config
└── README.md
```

## Editing

- All content and styling is in `index.html` (CSS is in the `<style>` block in the head).
- To swap or add a photo, drop the file into `assets/images/` and point the `<img src="...">` at it. Keep images under ~1000px on the long edge and run them through an optimizer (e.g. squoosh.app) before committing.
- Every `<img>` has explicit `width`/`height` and `loading="lazy"` — keep those when adding images so the layout doesn't jump while loading.

## Deploy (Netlify)

The site is static — no build step.

- **Drag & drop:** drag the whole `bargavi-portfolio` folder onto the Netlify dashboard (not just `index.html` — the images live in `assets/`).
- **Git-connected:** push this repo to GitHub and connect it in Netlify. Publish directory: repo root. Build command: none.

## Notes

Images were previously embedded inline as base64 inside `index.html`, which bloated the page to ~2 MB. They are now separate, optimized files, dropping the HTML to ~105 KB. The NASA/JPL logo was duplicated 5×; it's now a single shared file.
