# Glycoverse Tutorials

An online book for analyzing glycomics and glycoproteomics data with the
[Glycoverse](https://github.com/glycoverse) ecosystem.

[Read the book](https://glycoverse.github.io/glycoverse-tutorial/).

## Build locally

Install Quarto and the R dependencies described in the case studies, then run:

```sh
quarto render
quarto preview
```

The Quarto book includes a searchable chapter sidebar, numbered sections,
a per-chapter table of contents, and previous/next navigation. Chapter order
and parts are defined in `_quarto.yml`; visual styles are in `styles.scss`.
Add new chapters to `book.chapters` in `_quarto.yml`.

The rendered book is written to `docs/`. Commit the rendered output along with
source changes: the GitHub Pages workflow publishes `docs/` when changes reach
`main`; it does not run R or render the book.

Execution uses `freeze: auto`, so unchanged computational chapters reuse their
checked-in results in `_freeze/`. To refresh all R results explicitly, run
`quarto render --execute` with the tutorial dependencies installed. For a
layout-only build using the saved results, run `quarto render --freeze`.

Existing tutorial URLs remain unchanged.
