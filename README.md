# PHY2001 laboratory report template

Queen's University Belfast — Observing Single-Photon Interference.
This is a writing scaffold, with no experimental results or completed report prose.

## Compile

Use TeX Live with `latexmk`, pdfLaTeX, Biber and the packages listed in
`main.tex` installed. From this directory, run:

```sh
latexmk -pdf main.tex
```

The output is `main.pdf`. The local `.latexmkrc` selects pdfLaTeX;
`latexmk` handles the required LaTeX and Biber passes automatically.
The initial scaffold has no citations, so an empty-bibliography warning is
expected. Add real entries to `references.bib` and cite them with
`\cite{source-key}` when writing the report.

In VS Code, install LaTeX Workshop, open this directory and open `main.tex`.
Run **LaTeX Workshop: Build LaTeX project**, then **View LaTeX PDF file**.
The included settings select the `latexmk (pdfLaTeX)` recipe.

To remove auxiliary files while retaining the PDF:

```sh
latexmk -c main.tex
```

## Write and organise

- Edit the student name and experiment date in `main.tex`; the experiment
  title and module are already filled in and can be edited there.
- Replace the abstract placeholder and write in `sections/`. Both the
  discussion and limitations sections live in `sections/discussion.tex`.
- Put report-ready PDF, PNG or JPG figures in `figures/selected/`. This is
  the graphics search path, so use the filename in `\includegraphics{...}`.
- Keep unused figures in `figures/archive/` and analysis scripts, notebooks
  and data in `analysis/`. Existing files elsewhere in this folder are untouched.
- Follow the labelled comments and commented equation, figure, table and
  citation examples. Replace placeholders before enabling examples.
- Aim for approximately five pages when complete; the empty scaffold is
  shorter. There are no forced page breaks or fixed page-count controls.

LaTeX auxiliary files are ignored by Git; sources, figures, analysis files
and the final PDF remain trackable. `.gitkeep` files preserve empty folders.
