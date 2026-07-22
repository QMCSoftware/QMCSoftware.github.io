# QMCPy Website Status

## Complete

- [x] Confirmed Quarto-on-`main`, `_site/`, `gh-pages`, and `qmcpy.org`
  architecture.
- [x] Replaced the standalone HTML landing page with one Quarto source site.
- [x] Added Home, About, Blog, News & Events, and Community source pages.
- [x] Added the requested navigation and authoritative external links.
- [x] Added a restrained responsive visual foundation.
- [x] Integrated the existing QMCPy logo in the navbar and homepage hero with
  responsive sizing and accessible alternative text.
- [x] Added GitHub Actions rendering and `gh-pages` publication with explicit
  `CNAME` preservation.
- [x] Added repository guidance, roadmap, ignore rules, and local instructions.
- [x] Rendered locally and inspected the generated site structure and links.

## Underway

- [ ] Collaborator review of the information architecture, visual direction,
  and provisional homepage copy.
- [ ] Browser-based responsive and accessibility review.
- [ ] Live GitHub Pages workflow and custom-domain verification.

## Next recommended task

- [ ] Review the rendered prototype with QMCPy collaborators and approve the
  visual direction and public copy before adding content or migrating posts.

## Decisions and scope boundaries

- Technical documentation stays in `QMCSoftware` and continues to use MkDocs.
- The primary GitHub link targets `QMCSoftware/QMCSoftware`; community links
  may also point to maintained pages within that project.
- The existing 18 blog posts are not imported in this prototype.
- No Reveal.js project, repository rename, speculative infrastructure, or
  Python dependency file is included.
- Generated `_site/` output remains outside the `main` branch.
- No commit or push is part of the current work.
