# QMCSoftware Website Prototype Plan

## Purpose and architecture

This repository will provide the single public-facing website for the
QMCSoftware organization. Quarto source lives on `main`, renders to `_site/`,
and is published by GitHub Actions to the `gh-pages` branch. The canonical
custom domain is `qmcsoftware.org`.

Technical documentation remains with each software repository and is linked
from this site. The website adds a shared public entry point; it does not
replace project documentation.

## Guiding principles

- Keep the prototype small, navigable, and easy to maintain.
- Reuse proven structural and deployment ideas without importing course or
  slide architecture.
- Treat maintained project sources as authoritative and avoid speculative copy.
- Separate source from generated output and validate each phase before adding
  complexity.
- Make later content migration explicit and reviewable.

## Phased roadmap

### Phase 0 — Confirm direction and inspect references

- [x] Confirm the repository roles, source branch, output directory, publish
  branch, custom domain, and scope exclusions.
- [x] Inspect the starting QMCPy-only prototype files.
- [x] Inspect relevant Quarto and deployment patterns in `MATH565Fall2026`.
- [x] Confirm the maintained documentation and GitHub destinations from
  `QMCSoftware`.

### Phase 1 — Prepare the repository

- [x] Replace the standalone `index.html` with Quarto source.
- [x] Add ignore rules for generated Quarto output.
- [x] Preserve the root `CNAME` during prototype setup.
- [x] Add repository purpose, local-render instructions, project guidance,
  roadmap, and status documentation.
- [x] Avoid unnecessary runtime dependencies; no `requirements.txt` is needed
  for the current non-executable content.

### Phase 2A — Establish the original site skeleton

- [x] Configure a Quarto website that renders to `_site/`.
- [x] Add Home, Blog, News & Events, Community, Documentation, and GitHub
  navigation.
- [x] Add initial Home and About sources.
- [x] Create `blog/`, `news/`, `community/`, `assets/`, `styles/`, and workflow
  structure.
- [x] Link Documentation to the existing MkDocs site and GitHub to the primary
  QMCSoftware repository.

### Phase 2B — Establish the visual foundation

- [x] Add a restrained initial color palette, typography, spacing, hero, and
  responsive button treatment.
- [x] Keep the styling local and independent of classroom-specific styles.
- [ ] Review the prototype with collaborators and align it with any approved
  QMCSoftware visual identity or assets.
- [ ] Complete browser-based responsive and accessibility review.

### Phase 3 — Convert to the QMCSoftware umbrella

- [x] Replace the QMCPy-specific homepage with an organization-wide homepage.
- [x] Add a Software section for QMCPy, QMCToolsCL, QuasiMC.jl, and LDData.
- [x] Add a Publications prototype without inventing a complete bibliography.
- [x] Update shared navigation, metadata, footer, and organization-wide copy.
- [x] Keep each project's detailed documentation in its maintained repository.
- [x] Retain `qmcpy.org` and the existing `CNAME` during the initial transition.
- [x] Set `qmcsoftware.org` as the long-term canonical domain and custom domain.
- [ ] Verify any required redirects from the former domain.
- [ ] Approve an organization-level visual identity and navbar mark, if any.

### Phase 4 — Refine the homepage

- [x] Add a concise prototype introduction and primary documentation/GitHub
  actions.
- [x] Add clear pathways to learning, updates, and community information.
- [ ] Replace provisional wording only with collaborator-approved public copy.
- [ ] Add approved imagery, examples, or impact highlights if they provide
  clear value.

### Phase 5 — Migrate the blog

- [x] Migrate “Why Add Q to MC?” as the first self-contained Quarto post,
  preserving its authorship, mathematical explanation, equations, figures, and
  captions.
- [x] Revise “Why Add Q to MC?” as a living article with one last-revised date,
  qualified convergence claims, and practical guidance.
- [x] Establish listing metadata and a discoverable Blog index.
- [ ] Inventory the existing 18 posts and their assets without modifying the
  source repository.
- [ ] Define Quarto post metadata, URL preservation, authorship, categories,
  and redirect requirements.
- [ ] Convert and review posts in small batches.
- [ ] Verify dates, authors, links, code, mathematics, images, and legacy URLs.
- [ ] Publish the complete archive only after collaborator review.

### Phase 6 — Build news and events

- [x] Add the section entry page without invented announcements.
- [x] Add a sourced prototype news item and a discoverable News & Events
  listing.
- [ ] Define lightweight metadata and archive conventions.
- [ ] Add only confirmed news, talks, workshops, releases, and events.
- [ ] Decide how past and upcoming events should be presented.

### Phase 7 — Develop community content

- [x] Link to maintained community and contribution resources.
- [ ] Agree on the intended audience and approved community narrative.
- [ ] Add verified governance, contributor, support, and participation
  information without duplicating maintained technical guidance.
- [ ] Review names, roles, affiliations, and acknowledgements with
  collaborators before publication.

### Phase 8 — Integrate documentation pathways

- [x] Add links to maintained project documentation and repositories.
- [x] State clearly that technical documentation remains with each project.
- [ ] Review reciprocal links from the software repositories and documentation.
- [ ] Verify that users can distinguish public, learning, API-reference, and
  contribution destinations.

### Phase 8A — Develop publications

- [x] Add a selected local YAML publication catalog.
- [x] Render ordinary publication records directly from YAML on the
  Publications page, without per-publication folders or QMD files.
- [x] Sort the curated website catalog by year descending and title ascending,
  grouping ordinary publications under year headings.
- [x] Add a reviewed prototype publication with publisher, DOI, and arXiv
  links as a hand-written featured introduction.
- [x] Document the one-record YAML contribution convention.
- [ ] Correct and enrich the corresponding AcademicLib record in a separately
  authorized AcademicLib task.
- [ ] Agree on bibliography scope, review ownership, and migration priorities.

### Phase 9 — Test the site

- [x] Validate the Quarto configuration and a complete local render.
- [x] Inspect generated page structure, internal destinations, external
  destinations, and custom-domain output.
- [ ] Perform browser checks at desktop and mobile sizes.
- [ ] Run accessibility, HTML, and link checks appropriate to the final
  content.
- [ ] Test from a fresh clone with the documented Quarto setup.

### Phase 10 — Validate deployment

- [x] Add GitHub Actions rendering from `main` to `_site/` and publishing to
  `gh-pages`.
- [x] Explicitly preserve `CNAME` in the rendered publish directory.
- [ ] Review repository Pages settings and workflow permissions.
- [ ] Trigger the workflow on GitHub and verify the `gh-pages` branch contents.
- [ ] Verify HTTPS and `qmcsoftware.org` after deployment.

### Phase 11 — Collaborator review and prototype decision

- [ ] Review information architecture, visual direction, and provisional copy
  with QMCSoftware collaborators.
- [ ] Record requested changes and resolve launch-blocking issues.
- [ ] Agree on ownership and cadence for blog, news, and community updates.
- [ ] Approve the prototype before beginning the 18-post blog migration.
