# QMCSoftware Website Status

## Complete

- [x] Confirmed Quarto-on-`main`, `_site/`, `gh-pages`, and `qmcsoftware.org`
  architecture.
- [x] Replaced the standalone HTML landing page with one Quarto source site.
- [x] Converted the QMCPy-only prototype into an umbrella QMCSoftware site.
- [x] Added Software pages for QMCPy, QMCToolsCL, QuasiMC.jl, and LDData.
- [x] Added a Publications prototype and organization-wide navigation.
- [x] Migrated and revised “Why Add Q to MC?” as a living article, preserving
  its mathematical explanation, figures, captions, and authorship while adding
  qualified convergence and practical-use guidance.
- [x] Migrated “A QMCPy Quick Start,” preserving its original authorship, date,
  Keister example, equations, code, output, references, and figure.
- [x] Added a sourced 2026 SIAM Fellow news item.
- [x] Added a hand-written featured publication and a one-record YAML catalog
  convention for ordinary publications.
- [x] Documented the separation between the broad AcademicLib registry,
  website-curated publication records, and blog-local citations; catalog
  display order no longer depends on YAML record order.
- [x] Added working Blog, News & Events, and Publications listings.
- [x] Preserved Home, About, Blog, News & Events, and Community pages.
- [x] Added authoritative project documentation and repository links.
- [x] Added a restrained responsive visual foundation.
- [x] Retained the QMCPy logo asset for possible project-specific use while
  removing it from organization-level branding.
- [x] Added GitHub Actions rendering and `gh-pages` publication with explicit
  `CNAME` preservation.
- [x] Set `qmcsoftware.org` as the canonical site URL and GitHub Pages custom
  domain.
- [x] Added repository guidance, roadmap, ignore rules, and local instructions.
- [x] Rendered the complete 13-page site and verified local link targets and
  rendered `CNAME` preservation.

## Underway

- [ ] Collaborator review of the information architecture, visual direction,
  and provisional homepage copy.
- [ ] Browser-based responsive and accessibility review.
- [ ] Live GitHub Pages workflow and custom-domain verification.

## Next recommended task

- [ ] Review the rendered umbrella prototype with QMCSoftware collaborators and
  approve the visual direction and public copy before adding content or
  migrating posts.

## Decisions and scope boundaries

- Technical documentation stays with each software project.
- The primary GitHub link targets the QMCSoftware organization; project pages
  link to their respective repositories and documentation.
- The site uses `qmcsoftware.org` as its canonical URL and custom domain;
  redirect behavior from the former domain still requires verification.
- Two earlier blog posts are migrated as a pattern; the remainder of the
  archive is outside the current prototype.
- No Reveal.js project, speculative infrastructure, or Python dependency file
  is included.
- Generated `_site/` output remains outside the `main` branch.
- The completed prototype is maintained on a review branch until it is approved
  for merge into `main`.
