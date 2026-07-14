# AGENTS.md

## Cursor Cloud specific instructions

This repo is a single **LaTeX CV/résumé template** (the `awesome-source-cv` class). There is no
web/server app, no test suite, and no linter — "running the application" means compiling the
LaTeX source into `awesome-cv.pdf`.

### Build / run

- Main document: `awesome-cv.tex` (the `README.md` refers to a `huajh-awesome-cv.tex`, but the
  actual entry file in this branch is `awesome-cv.tex`).
- Engine is **lualatex** (see the `% !TEX TS-program = luatex` header and `\RequirePackage{fontspec}`).
- Build from the repo root so the bundled `fontawesome.sty` and the `fonts/` directory (used via
  the `localFont` class option) are found:
  - `latexmk -lualatex -interaction=nonstopmode awesome-cv.tex`, or
  - `lualatex -interaction=nonstopmode awesome-cv.tex`
- Output is a 2-page A4 PDF (`awesome-cv.pdf`).

### Non-obvious gotcha: benign `\FA` error / non-zero exit code

The build prints `! LaTeX cmd Error: Command '\FA' already defined.` and `lualatex`/`latexmk` exit
with a **non-zero status**, but the correct 2-page `awesome-cv.pdf` is still produced. The clash
comes from the repo's own files (both the bundled `fontawesome.sty` and `awesome-source-cv.cls`
define `\FA`) — it is not an environment problem, and fixing it would require editing the template.
Do **not** treat the non-zero exit as a build failure: verify success by checking for
`Output written on awesome-cv.pdf` in the log (or that the PDF has 2 pages via `pdfinfo`).

### Preview

- Render pages to images with `pdftoppm -png -r 110 awesome-cv.pdf out` (poppler-utils).
