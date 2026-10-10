# Personal site

A minimal Jekyll site for GitHub Pages. All content is in Markdown.

## Files you'll edit

| File | What it is |
|---|---|
| `_config.yml` | Your name, email, nav links |
| `index.md` | Home page bio and links |
| `research.md` | Papers, talks, teaching |
| `other.md` | Hobbies and everything else |
| `cv/cv.tex` | Your CV in LaTeX (built to PDF automatically) |
| `assets/files/` | Photos, paper PDFs, etc. |
| `assets/css/style.css` | Colors and fonts (the palette is at the top) |

## Publish on GitHub Pages

1. Create a repo named `yourusername.github.io` (this gives you the root URL).
2. Upload these files to it, including the hidden `.github/` folder (or `git push`).
3. In the repo: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
4. Every push to `main` now compiles `cv/cv.tex`, copies the PDF to `assets/files/cv.pdf`, and deploys the site. Progress shows in the **Actions** tab.

If you use a different repo name instead, set `baseurl: "/repo-name"` in `_config.yml`.

## Editing the CV

Edit `cv/cv.tex` and push. If the LaTeX fails to compile, the Actions tab shows a red X with the log, and the previous version of the site stays live.

## Preview locally (optional)

```
bundle install
bundle exec jekyll serve
```
Then open http://localhost:4000.

## Adding a new page

Create `newpage.md` in the root:

```
---
layout: default
title: New Page
permalink: /newpage/
---
Content here.
```
To put it in the header, add it under `nav:` in `_config.yml`.
