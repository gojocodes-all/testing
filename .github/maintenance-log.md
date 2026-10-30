# Maintenance log

## 2026-10-30 — Correct Git add staging guidance

- **Rationale:** The `git add` note said changes are moved into the staging area, obscuring that Git records the path's content at the moment the command runs. A learner could edit the file again and wrongly expect the newer content to be staged automatically. The note now explains the index snapshot, staged-versus-unstaged review, partial staging, and safe unstaging without discarding working changes.
- **Files changed:** `git-notes/git-add.md`, `README.md`, and `.github/maintenance-log.md`.
- **Validation:** Verified whole-file staging, post-stage edits, staged and unstaged diffs, partial staging, and `git restore --staged` in a disposable Git repository; checked the README link and summary; ran `git diff --check`; and reviewed the complete diff for command safety, Git terminology, compatibility, and repository scope.
- **Risk:** Low. Documentation only; no repository history, runtime code, dependencies, configuration, or workflows are changed.
- **Rollback:** Revert this pull request's squash commit to restore the previous one-line note and README summary.

## 2026-10-23 — Clarify Git diff states

- **Rationale:** The `git diff` note described the command as showing pre-commit differences without explaining that plain `git diff` excludes staged changes. A learner could stage work, see an empty diff, and incorrectly assume there was nothing left to review.
- **Files changed:** `git-notes/git-diff.md`, `README.md`, `.github/maintenance-log.md`
- **Validation:** Verified plain, staged, `HEAD`, path-limited, `--stat`, and `--name-only` behavior in a disposable Git repository; checked the README link and practice-loop commands; ran whitespace validation on the final diff.
- **Risk:** Low. Documentation-only; no repository history, runtime code, dependencies, configuration, or workflows are changed.
- **Rollback:** Revert this pull request to restore the previous one-line diff note and README summary.

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
