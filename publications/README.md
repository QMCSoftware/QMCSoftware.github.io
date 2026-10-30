# Publication data convention

The website uses three deliberately separate citation conventions:

1. Blog citations remain ordinary, hard-coded Markdown within each blog post.
   Do not create or use a shared BibTeX file for blogs at this stage.
2. `HickernellAcademicLib/classlib/quarto/metadata/hickernell-papers.yml`
   remains the broad shared scholarly reference registry.
3. This repository's `data/publications.yml` is the website-owned, curated
   catalog. It contains only publications selected for the QMCSoftware
   website.

Relevant AcademicLib records may be copied manually into the website catalog.
Before adding them, verify and correct the bibliographic metadata and add
website-specific fields such as an original summary, related projects,
and featured status. The website does not read from AcademicLib at build time,
and no synchronization machinery is part of this prototype.

Quarto reads `data/publications.yml` directly and formats the general catalog
on `publications/index.qmd` with `publications/catalog.ejs.md`. Display order is
independent of the records' physical YAML order: publications are sorted by
year descending and then title ascending within each year. The template renders
one continuous catalog, without separate year headings.

## Record convention

Each record should have a stable key, preferably matching its AcademicLib key
when one exists. It should include:

- verified bibliographic fields, an `authors` list, and authoritative URLs;
- related QMCSoftware projects, when relevant;
- optional tags retained as catalog metadata;
- an optional `featured` status;
- an original `description` used as the website's short summary.

An ordinary publication needs only one YAML record. Do not add a slug, rendered
path, publication folder, or separate QMD page. The custom catalog template
prints the title, authors, year, venue, volume, issue, pages or article number
when present, links, and related projects directly on the Publications page.
Tags are not displayed.

Use the current formal publication's bibliographic year, venue, and DOI or
publisher URL when available. Retain any arXiv URL as metadata, but show the
arXiv button only when no formal publication link is available. Label theses
and preprints separately, and mark forthcoming work explicitly rather than
inventing volume or page information. Record the verification date in
`metadata_checked` and its evidence in `metadata_sources`; status evidence can
use a separate `status_url` when the manuscript is still the available text.

The introductory tutorial is written by hand as the featured item on
`publications/index.qmd`. Its YAML record remains for catalog consistency and
has `featured: true`, so it is omitted from the general catalog and is not
displayed twice.

## Contribution workflow

1. Add one verified record to `data/publications.yml`.
2. Render the complete site with `quarto render`.
3. Confirm the publication appears correctly on the Publications page.

That single YAML edit is the complete source change required for an ordinary
publication.

## Restored WordPress publications

The WordPress content export dated 2026-05-26 contains 24 papers on the
former `https://qmcpy.org/publications/` page, plus a reference to the GAIL
project website for 2011–2019. These papers are represented in the YAML
catalog. The existing featured tutorial is the same work as the old
`arXiv:2502.03644` entry and is retained once. Together with the two additional
2026 preprints, the restored collection contains 26 papers: one featured and
25 ordinary entries. The GAIL reference remains a separate link on the page.

Restored entries retain `source_url`, `source_snapshot`, `source_year_group`,
and the exact `source_citation` from the export. These fields document the
historical source; the original citation is not a claim that its publication
status is still current. All 26 records were checked on 2026-10-29.
`metadata_sources` records the primary sources used to check each entry.
The historical workshop link for “Four Ways to
Grow Scientific Software” is preserved but has not been independently
revalidated.

The displayed year uses the publisher's bibliographic year where verified:
the two MCQMC 2022 chapters were published in 2024, the MCQMC 2020 software
survey in 2022, and the Hilbert-space tractability article in 2024. Their old
year groups remain available in the provenance fields. The importance
sampling article retains its journal issue year, 2021; the journal website
also records a later online publication date. The QMCPy preprint uses the
current arXiv title, while its original title remains in `source_citation`.

The latest check replaces five preprint citations with formal records:
“High-dimensional quasi-Monte Carlo via combinatorial discrepancy,” “Neural
Low-Discrepancy Sequences,” “Fast Bayesian multilevel quasi-Monte Carlo,”
“Empirical Bernstein and betting confidence intervals for randomized
quasi-Monte Carlo,” and “Enhancing Neural Autoregressive Distribution
Estimators for Image Reconstruction.” The Bayesian multilevel paper uses its
publisher-assigned 2027 issue year; its Crossref registration date is not
treated as an online publication date. “Low Stein Discrepancy via
Message-Passing Monte Carlo” uses its accepted ICLR 2025 workshop record.
“Multilevel Sampling in Algebraic Statistics” is marked forthcoming based
on the coauthor's publication list, without unverified journal details.

With the 15 earlier papers described below, the catalog currently contains
41 papers: one featured and 40 ordinary entries. These comprise 32 formal
journal, proceedings, or workshop records, six preprints without a matching
formal record located, one thesis, one forthcoming article, and the preserved
historical workshop report.

## Pre-2020 QMC and low-discrepancy papers

On 2026-10-29, 15 papers were selected from Fred J. Hickernell's Google
Scholar profile using publication before 2020, more than 90 total citations,
and direct relevance to quasi-Monte Carlo or low-discrepancy sampling/design.
The source profile, record link, observed count, and check date are retained
in `scholar_url`, `scholar_citations`, `scholar_checked`, and `scholar_year`.
These counts are dated selection evidence, not automatically updated metrics,
and are not displayed on the page. No tags were added to these records.

The selection includes discrepancy-based experimental-design papers and the
two multilevel integration papers whose constructions use lattice rules or
scrambled digital sequences. It excludes the unrelated fluid-stability and
sparse-learning papers, and does not import the held error-block-coding paper.

For “Extensible Lattice Sequences for Quasi-Monte Carlo Quadrature,” the
displayed year follows SIAM's current 2000 issue metadata; Scholar's 2001 year
and the discrepancy are retained in the record. “Control variates for
quasi-Monte Carlo” uses article-only pages 1–18, with the combined discussion
and rejoinder pagination 1–31 documented in `metadata_note`. The 1997 corrected
printing of the 1996 quadrature-error paper is noted rather than counted twice.

The AcademicLib record `hickirsor_2026_qmc_tutorial` should later be enriched
with the website's structured fields and corrected to replace its current
arXiv DOI with the final Springer DOI,
`10.1007/978-3-032-10590-5_1`. AcademicLib is not modified as part of this
website task.
