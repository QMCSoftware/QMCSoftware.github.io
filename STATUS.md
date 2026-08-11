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
- [x] Added working Blogs, News & Events, and Publications listings.
- [x] Preserved Home, About, Blogs, News & Events, and Community pages.
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
- [x] Migrated the complete 18-post QMCPy blog archive into self-contained
  Quarto posts while retaining the technical documentation and notebooks in
  the QMCPy repository.
- [x] Standardized blog chronology on one last-revised `date` per post, with no
  separate first-publication field, and retained the approved revised version
  of “Why Add Q to MC?”.
- [x] Preserved and published all 48 blog images in the local render, expanded
  MkDocs code snippets, converted callouts and image groups, and normalized
  legacy mathematical delimiters for Quarto.
- [x] Rendered all 30 site pages and completed local link, desktop, mobile, and
  per-post browser checks for the 18-post archive.
- [x] Widened the shared blog reading column modestly and made title metadata
  responsive so realistic author names and dates wrap without clipping.
- [x] Added a responsive, YAML-driven QMC Software Directory under Community,
  separate from the organization-owned projects in Software.

## Underway

- [ ] Collaborator review of the information architecture, visual direction,
  and provisional homepage copy.
- [ ] Accessibility review beyond the completed desktop and mobile browser
  checks.
- [ ] Live GitHub Pages workflow and custom-domain verification.

## Next recommended task

- [ ] Review and approve the completed local 18-post archive before any branch
  is pushed or a pull request is opened.

## Decisions and scope boundaries

- Technical documentation stays with each software project.
- The Website owns the broader community QMC software directory; the Software
  section remains limited to projects maintained by the QMCSoftware
  organization.
- The primary GitHub link targets the QMCSoftware organization; project pages
  link to their respective repositories and documentation.
- The site uses `qmcsoftware.org` as its canonical URL and custom domain;
  redirect behavior from the former domain still requires verification.
- The complete 18-post QMCPy blog archive is migrated locally; publishing it
  remains approval-gated.
- Blog cards and title blocks use each post's last-revised date; the archive is
  sorted newest revision first and does not carry a separate first-published
  date.
- “Why Add Q to MC?” remains the approved living article; the other 17 posts
  preserve the visible content of their source articles.
- No Reveal.js project, speculative infrastructure, or Python dependency file
  is included.
- Generated `_site/` output remains outside the `main` branch.
- The completed prototype is maintained on a review branch until it is approved
  for merge into `main`.
