# NEXT

## Current state

- `main` is the Website source branch and publishes to `gh-pages` through the
  Quarto workflow.
- Small, validated Website changes may be committed and pushed directly to
  `main`; longer, overlapping, or higher-risk work should use a short-lived
  branch.
- The historic 18-post blog archive and the community QMC Software Directory
  are live on the Website.
- Pull request #4, adding the two May 2026 QMCPy posts, has been merged into
  `main`.
- The Brownian Bridge article and its two figures are in
  `blogs/brownian-bridge/`, using the QMCPy 2.4 API and current demo links.
- Community includes extensible directories for QMC software and university
  courses using QMCSoftware.
- The QMCPy project page presents recent PyPI activity from a cached summary;
  the publication workflow refreshes it from QMCPy's authoritative
  `pypi-stats` branch on every deployment and every Monday.
- The QMC software directory still exists in `QMCSoftware`. Removing it is a
  separate future task that must use that repository's issue and pull-request
  workflow.

## Current focus

The Publications update was approved for publication on 2026-10-30.
The 24-paper WordPress list and two new 2026 preprints are
preserved, with the featured tutorial deduplicated and GAIL link retained.
The 2026-10-29 citation refresh uses verified formal records where available,
with explicit preprint, thesis, forthcoming, and historical-link statuses.

The user has now authorized adding the 15 selected pre-2020 Fred Hickernell
papers with more than 90 Google Scholar citations and direct QMC or
low-discrepancy relevance. The catalog contains 41 papers: 40 ordinary and
one featured. All ordinary entries share a continuous publication-year
descending list, with title ordering within a year and no year sections.
Tags remain hidden; the new records have no tags, and dated Scholar counts
are retained only as selection metadata. The full 35-source-page render,
41-record and rendered-order checks, preservation of the previous 26 records,
all-page local-reference checks, and browser inspection passed. Math in the
new titles renders correctly. Publication page:
`https://qmcsoftware.org/publications/#publication-catalog`.

Continue applying the coordination workflow in `AGENTS.md` and
`AUTHOR_WORKFLOW.md` to real Website tasks. Refine it only in response to
observed ambiguity, overlap, or unnecessary friction.

## Immediate next task

1. For the next substantive Website change, follow the start, validation,
   synchronization, and publication steps in `AUTHOR_WORKFLOW.md`.

## Questions to resolve

- When the collaborator group grows, what threshold should make Website pull
  requests the default rather than optional?
- After several tasks, do pushed branches provide enough visibility, or is a
  lightweight issue-based work-claim convention also useful?

## Definition of done

- The coordination files are published and used successfully across several
  Website tasks or machines.
- Any refinement is based on an observed coordination problem rather than
  speculative process.
- No change is made to `QMCSoftware` until a separate issue and pull request are
  authorized.
