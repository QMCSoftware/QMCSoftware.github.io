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
website-specific fields such as an original summary, related projects, tags,
and featured status. The website does not read from AcademicLib at build time,
and no synchronization machinery is part of this prototype.

Quarto reads `data/publications.yml` directly and formats the general catalog
on `publications/index.qmd` with `publications/catalog.ejs.md`. Display order is
independent of the records' physical YAML order: publications are sorted by
year descending and then title ascending within each year. The template groups
ordinary publications under year headings.

## Record convention

Each record should have a stable key, preferably matching its AcademicLib key
when one exists. It should include:

- verified bibliographic fields, an `authors` list, and authoritative URLs;
- tags and related QMCSoftware projects;
- an optional `featured` status;
- an original `description` used as the website's short summary.

An ordinary publication needs only one YAML record. Do not add a slug, rendered
path, publication folder, or separate QMD page. The custom catalog template
prints the title, authors, year, venue, volume and pages when present, links,
tags, and related projects directly on the Publications page.

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

The AcademicLib record `hickirsor_2026_qmc_tutorial` should later be enriched
with the website's structured fields and corrected to replace its current
arXiv DOI with the final Springer DOI,
`10.1007/978-3-032-10590-5_1`. AcademicLib is not modified as part of this
website task.
