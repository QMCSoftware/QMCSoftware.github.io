# QMCSoftware website

This repository contains the public-facing website for
[QMCSoftware](https://github.com/QMCSoftware), built with
[Quarto](https://quarto.org/). It is an umbrella site for the organization's
software, publications, blog, news and events, and community information.

Technical documentation remains with each software repository. The website
links to maintained project documentation instead of duplicating it.

The site uses `https://qmcsoftware.org` as its canonical URL and GitHub Pages
custom domain.

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
