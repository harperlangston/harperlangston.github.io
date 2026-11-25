# CV

- `m_harper_langston_cv.pdf` is the official CV linked from the website, built from `cv.tex`.
- `archive/m_harper_langston_cv_2019.pdf` is the previous (2019) CV, kept for reference and not linked.
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
To publish an update, rebuild and copy `cv.pdf` over `m_harper_langston_cv.pdf`.
