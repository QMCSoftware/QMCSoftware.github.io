# Website Author Workflow

This repository is maintained by a small group of trusted collaborators using
both human and agent-assisted work across multiple machines. Small, validated
changes may be published directly to `main`; pull requests are available when
review or isolation would help, but are not required by default.

## Before starting

1. Inspect the worktree with `git status` and preserve unrelated changes.
2. When the worktree is clean, update `main` from `origin/main` with a
   fast-forward-only pull.
3. Read `AGENTS.md` and `notes/NEXT.md`, then inspect the files relevant to the
   task.
4. Check recent history or remote branches when another collaborator may be
   working in the same area.

`notes/NEXT.md` communicates the latest durable handoff, but it is not an
active-work lock. For work that will span sessions or may overlap another
contributor, create and push a short-lived branch so the activity is visible.

## Direct change or branch

Work directly on `main` when a change is focused, low risk, expected to finish
in one session, and unlikely to overlap another task.

Use a short-lived branch when work:

- spans sessions or machines;
- changes site architecture, deployment, or a large body of content;
- overlaps another contributor's likely work; or
- would benefit from explicit review.

A branch does not require a pull request. Trusted collaborators may integrate
a validated branch into `main` directly when review is unnecessary. Never
force-push shared branches.

## While working

- Keep commits focused and preserve unrelated work.
- Keep public claims sourced and project technical documentation in its owning
  repository.
- Do not commit `_site/` or other generated Quarto working files.
- Record durable direction in `PLAN.md`, milestone progress in `STATUS.md`, and
  immediate resumption information in `notes/NEXT.md`.

## Validate and publish

1. Run `quarto render` for production validation and inspect representative
   rendered pages affected by the change.
2. Run focused structural, link, accessibility, or content checks appropriate
   to the change, followed by `git diff --check`.
3. Review the complete diff, including new files.
4. Fetch `origin` again. If `origin/main` advanced, integrate it without
   rewriting published history and repeat affected validation.
5. Commit with a concise message and push to `origin/main`.
6. Confirm that the GitHub Pages workflow completes successfully when the
   change affects the published site.

## Leave an operational handoff

Inspect `notes/NEXT.md` whenever work concludes. Update it only when the
current state, immediate next task, constraints, unresolved questions, or
definition of done materially changed. Keep historical detail in Git and
milestone progress in `STATUS.md`; do not turn `notes/NEXT.md` into a session
log.

If a task stops midstream, state exactly what remains, what was validated, and
where the next collaborator should resume. Push the working branch when doing
so is safe and useful.
