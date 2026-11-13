# harperlangston.com

Personal site of M. Harper Langston, hosted on GitHub Pages.

Plain HTML and CSS. There is no build step: edit a file, commit, push, and the site updates in a minute or two.

## Layout

| Path | What it is |
| --- | --- |
| `index.html` | Main page: intro, publications, reports, patents, education |
| `code/index.html` | Code page. Pulls your public GitHub repos automatically when the page loads |
| `assets/style.css` | All styling (light and dark mode) |
| `papers/` | Paper PDFs and the thumbnails shown next to each entry |
| `m_harper_langston_cv.pdf` | CV linked from the top of the main page |
| `kifmm3d/` | KIFMM3D documentation (old URLs kept working) |
| `CNAME` | Tells GitHub Pages to serve the site at harperlangston.com |
| `.nojekyll` | Serve files as-is (no Jekyll processing) |

The other files at the top level (videos, slides, tarballs, old pages) came from the old GoDaddy site.
They stay at the same addresses so existing links keep working.

## Adding a publication

Copy an existing `<article class="pub">…</article>` block in `index.html`, paste it under the right year,
and change the title, authors, venue, links and abstract. Put the PDF and a small thumbnail image in `papers/`.
For a new year, copy one of the `<h3 class="year">` headings and the `<div class="year-group">` that follows it.

## Code page

Repositories come from the GitHub API each time the page loads. To control the list, edit near the bottom of `code/index.html`:

- `PIN`: repo names to show first, in order
- `HIDE`: repo names to leave off the page

Forks are hidden unless the visitor ticks "Show forks".

## Previewing locally

```
python3 -m http.server 8000
```

Then open http://localhost:8000.
