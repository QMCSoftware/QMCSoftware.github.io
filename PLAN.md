# QMCPy Website Prototype Plan

## Purpose and architecture

This repository will provide the public-facing QMCPy website. Quarto source
lives on `main`, renders to `_site/`, and is published by GitHub Actions to the
`gh-pages` branch. The custom domain is `qmcpy.org`.

The existing technical documentation remains in `QMCSoftware`, continues to
use MkDocs, and is linked prominently from this site. The website adds a public
entry point; it does not replace the package documentation.

## Guiding principles

- Keep the prototype small, navigable, and easy to maintain.
- Reuse proven structural and deployment ideas without importing course or
  slide architecture.
- Treat maintained QMCPy sources as authoritative and avoid speculative copy.
- Separate source from generated output and validate each phase before adding
  complexity.
- Make later content migration explicit and reviewable.

## Phased roadmap

### Phase 0 — Confirm direction and inspect references

- [x] Confirm the repository roles, source branch, output directory, publish
  branch, custom domain, and scope exclusions.
- [x] Inspect the starting `qmcpy-website` files.
- [x] Inspect relevant Quarto and deployment patterns in `MATH565Fall2026`.
- [x] Confirm the maintained documentation and GitHub destinations from
  `QMCSoftware`.

### Phase 1 — Prepare the repository

- [x] Replace the standalone `index.html` with Quarto source.
- [x] Add ignore rules for generated Quarto output.
- [x] Preserve the root `CNAME` for `qmcpy.org`.
- [x] Add repository purpose, local-render instructions, project guidance,
  roadmap, and status documentation.
- [x] Avoid unnecessary runtime dependencies; no `requirements.txt` is needed
  for the current non-executable content.

### Phase 2A — Establish the site skeleton

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
  QMCPy visual identity or assets.
- [ ] Complete browser-based responsive and accessibility review.

### Phase 3 — Develop the homepage

- [x] Add a concise prototype introduction and primary documentation/GitHub
  actions.
- [x] Add clear pathways to learning, updates, and community information.
- [ ] Replace provisional wording only with collaborator-approved public copy.
- [ ] Add approved imagery, examples, or impact highlights if they provide
  clear value.

### Phase 4 — Migrate the blog

- [ ] Inventory the existing 18 posts and their assets without modifying the
  source repository.
- [ ] Define Quarto post metadata, URL preservation, authorship, categories,
  and redirect requirements.
- [ ] Convert and review posts in small batches.
- [ ] Verify dates, authors, links, code, mathematics, images, and legacy URLs.
- [ ] Publish the complete archive only after collaborator review.

### Phase 5 — Build news and events

- [x] Add the section entry page without invented announcements.
- [ ] Define lightweight metadata and archive conventions.
- [ ] Add only confirmed news, talks, workshops, releases, and events.
- [ ] Decide how past and upcoming events should be presented.

### Phase 6 — Develop community content

- [x] Link to maintained community and contribution resources.
- [ ] Agree on the intended audience and approved community narrative.
- [ ] Add verified governance, contributor, support, and participation
  information without duplicating maintained technical guidance.
- [ ] Review names, roles, affiliations, and acknowledgements with
  collaborators before publication.

### Phase 7 — Integrate documentation pathways

- [x] Add prominent links to the existing MkDocs documentation.
- [x] State clearly that technical documentation remains a separate maintained
  site.
- [ ] Review cross-links from both sites and identify any minimal reciprocal
  navigation changes for a separately authorized `QMCSoftware` task.
- [ ] Verify that users can distinguish public, learning, API-reference, and
  contribution destinations.

### Phase 8 — Test the site

- [x] Validate the Quarto configuration and a complete local render.
- [x] Inspect generated page structure, internal destinations, external
  destinations, and custom-domain output.
- [ ] Perform browser checks at desktop and mobile sizes.
- [ ] Run accessibility, HTML, and link checks appropriate to the final
  content.
- [ ] Test from a fresh clone with the documented Quarto setup.

### Phase 9 — Validate deployment

- [x] Add GitHub Actions rendering from `main` to `_site/` and publishing to
  `gh-pages`.
- [x] Explicitly preserve `CNAME` in the rendered publish directory.
- [ ] Review repository Pages settings and workflow permissions.
- [ ] Trigger the workflow on GitHub and verify the `gh-pages` branch contents.
- [ ] Verify HTTPS and `qmcpy.org` after deployment.

### Phase 10 — Collaborator review and prototype decision

- [ ] Review information architecture, visual direction, and provisional copy
  with QMCPy collaborators.
- [ ] Record requested changes and resolve launch-blocking issues.
- [ ] Agree on ownership and cadence for blog, news, and community updates.
- [ ] Approve the prototype before beginning the 18-post blog migration.
