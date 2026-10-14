# Maintenance log

## 2026-10-14 — Correct Git stash file-scope guidance

- **Rationale:** The stash note said plain `git stash` stores uncommitted changes without explaining that untracked and ignored files are excluded. A learner could switch context expecting those files to be protected when they remain in the working tree.
- **Files changed:** `git-notes/git-stash.md`, `README.md`, `.github/maintenance-log.md`
- **Validation:** Reviewed all fourteen Git notes for scope and command consistency; confirmed the installed Git 2.51.1 help exposes `--include-untracked`/`-u` and `--all`/`-a`; verified the README link still targets the corrected note.
- **Risk:** Low. Documentation-only; no repository history, runtime code, configuration, dependencies, or workflows are changed.
- **Rollback:** Revert the maintenance commits or pull request to restore the previous one-line stash note and README summary.

## 2026-09-28 — Repository guide and note index

- **Rationale:** The README described the repository in one sentence but did not index its fourteen Git notes, distinguish the workflow records from command guidance, or explain how to practise and contribute safely.
- **Files changed:** `README.md`, `.github/maintenance-log.md`
- **Validation:** Verified every documented path; checked all relative Markdown links; reviewed commands against the repository's existing Git-learning purpose; ran `git diff --check`.
- **Risk:** Low. Documentation-only; no repository history, runtime code, configuration, dependencies, or workflows are changed.
- **Rollback:** Revert the maintenance commit to restore the previous short README and remove this log entry.
