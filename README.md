# gikallergis.github.io

Personal academic site — Georgios Kallergis.

## How to deploy

1. Replace **all files** in your `gikallergis.github.io` repo with the contents of this folder.
2. In your repo settings → Pages, make sure **Source** is set to `Deploy from a branch` → `main` / `root`.
3. Push. GitHub will build with Jekyll automatically — no `Gemfile` needed.

## How to edit

- **Add a photo:** put your image in the repo root (e.g. `photo.jpg`), then in `_layouts/default.html` replace the `<div class="avatar">GK</div>` line with:
  ```html
  <img src="/photo.jpg" class="avatar-img" alt="Georgios Kallergis">
  ```
- **Add a publication:** copy the `<div class="pub-card">...</div>` block in `index.md` and edit the fields.
- **Edit your bio / stack:** edit `about.md` — it's plain Markdown.
- **Add a repo card:** copy a `<a class="repo-item">` block in `projects.md`.
- **Add a CV link:** add `<a href="/cv.pdf">📎 CV</a>` to the `quick-links` div in `_layouts/default.html`, and drop your PDF in the repo root.

## File structure

```
_config.yml          # Site title, description, nav tabs
_layouts/default.html # Shared header, tab bar, footer
assets/css/style.css  # All styling
index.md             # Publications tab (home page)
projects.md          # Projects tab
about.md             # About tab
contact.md           # Contact tab
```
