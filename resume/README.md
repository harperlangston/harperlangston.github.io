# CV

- `m_harper_langston_cv.pdf` is the CV currently linked from the website (2019 version).
- `cv.tex` is the LaTeX source for the new CV.
- `build_lists.py` writes `generated/publications.tex`, `generated/reports.tex` and
  `generated/patents.tex` from `../index.html`, so the CV's paper and patent lists always
  match the website. Add new papers to the website, then re-run the script.

Build:

```
python3 build_lists.py
latexmk -pdf cv.tex
```

Anything marked `\todo{...}` in `cv.tex` prints in red until it is filled in.
When the new CV is ready, copy `cv.pdf` over `m_harper_langston_cv.pdf` (or change the
link in `../index.html`) to publish it on the site.
