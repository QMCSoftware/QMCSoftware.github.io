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
  existing documentation, and cross-repository planning, but must not be
  modified from this repository. Changes there use its separate issue, branch,
  review, and pull-request workflow.
- `MATH565Fall2026` may be inspected for Quarto structure and deployment
  patterns, but must not be modified.
- Other neighboring repositories are read-only references unless the user
  explicitly authorizes work in them.
- Preserve unrelated user changes and inspect `git status` before editing.

## Branch, build, and deployment conventions

- `main` is the Quarto source branch.
- Quarto renders the complete site to `_site/`.
- `_site/` and Quarto-generated working files are not committed to `main`.
- `.github/workflows/quarto-gh-pages.yml` renders on pushes to `main` and
  publishes `_site/` to `gh-pages`.
- The root `CNAME` must contain exactly `qmcsoftware.org`, and deployment must retain
  it as `_site/CNAME`.
- Use `quarto preview` for local authoring and `quarto render` for production
  validation.
- Scoped, validated Website changes may be committed and pushed directly to
  `main` without asking for separate permission each time. This standing
  authorization applies only to this repository. Respect an explicit request
  to keep particular work local or to hold it for review.
- Before beginning work, inspect `git status` and synchronize with
  `origin/main`. Pull with `--ff-only` when the worktree is clean; if it is not
  clean, inspect and preserve the existing work before synchronizing.
- Fetch again before publishing. If `origin/main` advanced, integrate those
  changes without rewriting published history, rerun affected validation, and
  then push. Never force-push.
- Direct work on `main` is appropriate for small, focused changes. Use a
  short-lived branch for work that spans sessions, overlaps another active
  task, or carries enough risk to benefit from isolation. A pull request is
  optional unless the user requests one.

## Coordination and handoff

- Read `notes/NEXT.md` before starting substantive work. It is the operational
  handoff, not a lock; inspect recent Git history and remote branches when
  concurrent work is possible.
- Follow `AUTHOR_WORKFLOW.md` for the shared human-and-agent workflow across
  machines.
- Keep document responsibilities distinct:
  - `AGENTS.md` contains durable agent rules and repository boundaries.
  - `AUTHOR_WORKFLOW.md` contains the collaboration, validation, and
    publication workflow.
  - `notes/NEXT.md` contains the immediate focus, current state, unresolved
    questions, and resumption point.
  - `PLAN.md` contains the durable roadmap and architectural direction.
  - `STATUS.md` records milestone-level progress and scope decisions.
  - `README.md` provides public repository orientation and setup instructions.
- At the end of work, reconcile only the handoff files whose information
  materially changed. Always inspect `notes/NEXT.md`; keep it concise and
  operational rather than turning it into a session log.

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
- Do not re-import or overwrite the migrated blog archive from the QMCPy
  repository unless a specific migration or reconciliation task is authorized.
- Do not add a Reveal.js slides project.
- Do not rename this or any related repository.
- Do not add speculative services, frameworks, or data pipelines.
