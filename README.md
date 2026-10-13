# Personal academic website: Angelo Cuzzola

Source for https://acuz.github.io (GitHub Pages, built with Jekyll by GitHub; nothing to install).
Replaces sites.google.com/view/angelocuzzola.

Content source of truth: `academic_jobs_application/profile/publications/publications.bib`
and the latest CV. When those change, mirror the change here.

## Updating the site

Edit a file (locally or with the pencil icon on github.com), commit, push. GitHub rebuilds the
site in about a minute; the build log is under the repository's **Actions** tab.

| To change | Edit |
|---|---|
| A paper (status, journal, links, abstract), or add one | `_data/papers.yml` (instructions at the top of the file) |
| A coauthor's name or link | `_data/people.yml` |
| Home page text, contact details | `index.md` |
| Teaching | `teaching.md` |
| The CV | add or replace `cv.pdf`; when first adding it, set `cv: /cv.pdf` and un-comment the cv menu item in `_config.yml` |
| Email, profile links, menu | `_config.yml` |
| Fonts, colours, spacing | `assets/css/site.css` (colours are the variables at the top) |
| Photo | add `assets/img/photo.jpg`, set `photo: /assets/img/photo.jpg` in `_config.yml` |

Moving a paper from working paper to published: in `papers.yml` change `section:` to
`published`, set `venue`, `details` and `year`, and swap the links.

## Layout

```
_config.yml              site settings, menu, profile links
_data/papers.yml         every paper on the Research page
_data/people.yml         coauthors and their pages
_layouts/default.html    the page frame (header, menu, footer)
_includes/paper.html     how one paper entry is displayed
assets/css/site.css      all styling
index.md                 home
research.html            research (generated from papers.yml)
teaching.md              teaching
cv.pdf                   CV (not added yet)
tools/green-products/    green products classification tool (standalone HTML, not processed by Jekyll)
```

## Local preview (optional)

Needs Ruby: `gem install jekyll jekyll-seo-tag jekyll-sitemap`, then `jekyll serve` in this folder and
open http://localhost:4000.
Not required; pushing is enough.
