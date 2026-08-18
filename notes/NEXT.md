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
- Community includes extensible directories for QMC software and university
  courses using QMCSoftware.
- The QMC software directory still exists in `QMCSoftware`. Removing it is a
  separate future task that must use that repository's issue and pull-request
  workflow.

## Current focus

Use the coordination workflow in `AGENTS.md` and `AUTHOR_WORKFLOW.md` to finish
reviewing and publishing the two-post expansion, then continue applying it to
the next several real Website tasks. Refine it only in response to observed
ambiguity, overlap, or unnecessary friction.

## Immediate next task

1. Verify the production deployment of the merged two-post expansion.
2. For the next substantive Website change, follow the start, validation,
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
