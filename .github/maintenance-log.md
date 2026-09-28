# Maintenance log

## 2026-09-28 — Repository guide and note index

- **Rationale:** The README described the repository in one sentence but did not index its fourteen Git notes, distinguish the workflow records from command guidance, or explain how to practise and contribute safely.
- **Files changed:** `README.md`, `.github/maintenance-log.md`
- **Validation:** Verified every documented path; checked all relative Markdown links; reviewed commands against the repository's existing Git-learning purpose; ran `git diff --check`.
- **Risk:** Low. Documentation-only; no repository history, runtime code, configuration, dependencies, or workflows are changed.
- **Rollback:** Revert the maintenance commit to restore the previous short README and remove this log entry.
