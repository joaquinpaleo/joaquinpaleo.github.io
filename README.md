# Academic website — Joaquin Paleo

A small, static job-market website (no build step, no framework). It is one
long page with three sections (About, Research, Teaching); the nav links are
shortcuts that scroll to each section. It hosts free on GitHub Pages.

```
website/
├── index.html        The whole site: About, Research, Teaching sections
├── style.css         Shared styles (edit colors/fonts here)
├── favicon.svg       Browser-tab monogram
├── headshot.svg      Placeholder portrait — replace with headshot.jpg
└── README.md         This file
```

Files still to add to this folder when ready: `cv.pdf`, `jmp.pdf`,
`jmp_slides.pdf`, `unions_education.pdf`, `research_statement.pdf`,
`teaching_statement.pdf`, `headshot.jpg`.

## 1. Preview it locally

Just double-click `index.html` to open it in your browser. To see it exactly as
it'll be served (relative links, fonts), run a local server from this folder:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## 2. Fill in the placeholders

Anything in `[square brackets]` is a placeholder. Search the files for `[` and
`EDIT` (I left `<!-- EDIT -->` comments at each spot). Checklist:

- [x] **Surname** — done (Joaquin Paleo).
- [ ] **Email** — `[you]@ucdavis.edu` in `index.html`.
- [ ] **Google Scholar** link (`index.html`, `research.html`).
- [ ] **CV** — save your CV as `cv.pdf` in this folder (the nav already links to it).
- [ ] **Headshot** — add `headshot.jpg` (roughly 5:6 portrait), then change
      `src="headshot.svg"` to `src="headshot.jpg"` in `index.html`.
- [ ] **JMP title** — confirm/replace the working title in `index.html` and `research.html`.
- [ ] **JMP abstract** — paste your real abstract into `research.html` (the current
      text is a draft I wrote from your project description — replace it).
- [ ] **JMP PDF / slides** — add `jmp.pdf` and `jmp_slides.pdf`.
- [ ] **Coauthors** — add or delete the "with [Coauthor(s)]" lines.
- [ ] **Fields** — confirm primary/secondary fields in `index.html`.
- [ ] **Teaching** — confirm course titles for ECN 100B and ECN 130, add terms/years,
      finalize the award name in `teaching.html`.
- [ ] Delete any section you don't need yet (e.g., the Working Papers block).
- [ ] Optional: add `research_statement.pdf` and `teaching_statement.pdf`.

Want a Contact page or a Data page like some of the sites you liked? Copy any
existing HTML file, swap the content, and add a link to the `<nav>` in all pages.

## 3. Put it online — GitHub Pages (free)

**Option A — username site (cleanest URL: `yourname.github.io`)**

1. Create a GitHub account if you don't have one.
2. Make a new **public** repository named exactly `yourusername.github.io`.
3. Upload everything in this folder to the repo root (drag-and-drop in the
   browser works, or use git). `index.html` must be at the top level.
4. Go to the repo's **Settings → Pages**, set Source to "Deploy from a branch",
   branch `main`, folder `/ (root)`, Save.
5. Wait a minute, then visit `https://yourusername.github.io`.

**Option B — project site (`yourusername.github.io/website`)**

Same as above but name the repo anything (e.g., `website`). The URL gets the
repo name appended.

**Custom domain (optional, ~$12/yr):** buy a domain (Namecheap, Cloudflare,
Google Domains), then in Settings → Pages add it under "Custom domain" and
point a CNAME at `yourusername.github.io`. Several of the sites you liked do
this (e.g., `carlos-brito.com`).

## 4. Changing the look

All design choices live in `style.css` at the top, under `:root`:

- `--heading` / `--link` / `--link-hover` — heading and link colors (currently black, burgundy on hover)
- `--accent` — the single accent (burgundy)
- `--paper` / `--ink` — background and text
- Fonts: **Newsreader** (serif headings) + **Public Sans** (body), loaded from
  Google Fonts in each HTML `<head>`. Swap the family names in both places to
  change them.

The aesthetic deliberately mirrors the sites you sent: minimal, fast, with the
job market paper front and center. If you want it even plainer (no headshot
block, single accent only), it's a couple of lines to remove.
