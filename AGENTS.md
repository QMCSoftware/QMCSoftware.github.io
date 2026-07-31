# AGENTS.md

## Repository purpose

This repository contains the public-facing QMCSoftware organization website.
It is a Quarto website intended for software introductions, publications,
community information, news and events, and blog content.

Each project's technical documentation remains with its software repository.
Link to that documentation; do not migrate, duplicate, or replace it from this
repository.

## Repository boundaries

- Write only within `qmcsoftware-website` unless the user explicitly changes the
  scope.
- `QMCSoftware` may be inspected for authoritative project information,
  existing documentation, and later blog-migration planning, but must not be
  modified from this repository.
- `MATH565Fall2026` may be inspected for Quarto structure and deployment
  patterns, but must not be modified.
- Other neighboring repositories are read-only references unless the user
  explicitly authorizes work in them.
- Preserve unrelated user changes and inspect `git status` before editing.

## Branch, build, and deployment conventions

- `main` is the eventual Quarto source branch.
- Quarto renders the complete site to `_site/`.
- `_site/` and Quarto-generated working files are not committed to `main`.
- `.github/workflows/quarto-gh-pages.yml` renders on pushes to `main` and
  publishes `_site/` to `gh-pages`.
- The root `CNAME` must contain exactly `qmcpy.org`, and deployment must retain
  it as `_site/CNAME`.
- Use `quarto preview` for local authoring and `quarto render` for production
  validation.
- Do not commit or push unless the user explicitly asks.

## Content and design principles

- Keep public copy accurate, concise, and understandable to both prospective
  users and contributors.
- Prefer links to maintained sources over duplicated technical information.
- Do not invent claims, biographies, announcements, dates, or community roles.
- Use simple, maintainable Quarto conventions and a small amount of local
  styling.
- Keep navigation clear, responsive, and accessible.
- Add content incrementally and validate source, rendered pages, and links.
- Record durable architectural changes in `PLAN.md` and construction progress
  in `STATUS.md`.

## Scope exclusions

- Do not migrate the MkDocs technical documentation.
- Do not import or convert the existing 18 blog posts until the blog-migration
  phase is explicitly authorized.
- Do not add a Reveal.js slides project.
- Do not rename this or any related repository.
- Do not add speculative services, frameworks, or data pipelines.
