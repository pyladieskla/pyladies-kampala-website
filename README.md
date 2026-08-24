# PyLadies Kampala Website (static / Netlify template)

The website for **PyLadies Kampala**, built directly from the official
[pyladies/netlify-website-template](https://github.com/pyladies/netlify-website-template) —
the same starting point most PyLadies chapters use, as pointed to by
[pyladies/chapter-websites](https://github.com/pyladies/chapter-websites).

Plain HTML, CSS, and Bootstrap 4 — no build step, no framework, no JavaScript beyond Bootstrap's
own nav toggle. Deploys straight to Netlify or GitHub Pages.

## Pages

- **`index.html`** — landing page: chapter intro, objective, beneficiaries, organizers,
  resources, contact.
- **`events.html`** — Upcoming Events: the 2026 Open Source Workshop (full details, schedule,
  who it's for) and a look back at the 2024 Open Source Summit.
- **`code-of-contact.html`** — Code of conduct: This website has code of conduct that the users and the community follow to keep everyone respected, supported and protected.

## Content source

All copy on both pages is drawn directly from the chapter's PSF grant application and workshop
web copy document (the "PyLadies Open Source Workshop Summit" and "open source summit content
web page" sections) — nothing has been invented or paraphrased into new marketing language.
Refugee-program content from that same document was intentionally left out of this public site.

## What changed from the upstream template

- Replaced the placeholder script logo and cartoon mascot with the **official PyLadies logo**
  (`images/pyladies_logo.png`, the same file used on every chapter page at
  [pyladies.com/locations](https://pyladies.com/locations/)).
- Removed the stock skyline photo, squiggle dividers, and Lorem Ipsum organizer bios/photos —
  no placeholder content ships in this version.
- Replaced the "Events" on-page anchor with a real second page, `events.html`.
- Organizers section lists only names actually present in chapter records (no invented bios).

## Local development

```bash
cd pyladies-kampala-netlify
python -m http.server 8000
```

Then visit `http://localhost:8000/index.html` and `http://localhost:8000/events.html`.

## Deployment

Per the upstream template and the `chapter-websites` process:

1. Push this repo to GitHub (a dedicated repo requested via an issue on
   [pyladies/chapter-websites](https://github.com/pyladies/chapter-websites), or your own repo
   in the meantime).
2. Connect it to [Netlify](https://www.netlify.com/) (no build command needed — it's static) or
   enable GitHub Pages on the `gh-pages`/default branch.
3. Once live, register the chapter repo as a submodule of `chapter-websites` — see that repo's
   README (this is an org-admin step for the chapter organizer, not done from here).

## Updating content

Both pages are plain HTML — edit `index.html` / `events.html` directly. Shared styling lives in
`style.css` (no preprocessor, no build step required).
