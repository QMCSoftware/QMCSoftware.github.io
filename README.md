# QMCPy website

This repository contains the public-facing website for
[QMCPy](https://qmcpy.org), built with [Quarto](https://quarto.org/).

Technical package documentation remains in the
[QMCSoftware repository](https://github.com/QMCSoftware/QMCSoftware) and is
published separately with MkDocs at
[qmcsoftware.github.io/QMCSoftware](https://qmcsoftware.github.io/QMCSoftware/).

## Local preview

Install Quarto, then run:

```bash
quarto preview
```

To create the production output in `_site/`:

```bash
quarto render
```

The `main` branch is the eventual source branch. GitHub Actions renders the
site and publishes `_site/` to `gh-pages`; generated output is not committed to
`main`.
