# Git workflow sandbox

A small learning repository for practising Git and GitHub workflows without
using an application codebase. It contains short command notes plus two records
from branch → pull request → merge exercises.

There is no application, package manifest, build command, dependency install,
or automated test suite in this repository.

## Git notes

Read the notes in roughly this order:

1. [`git-clone`](git-notes/git-clone.md) — copy a remote repository locally.
2. [`git-status`](git-notes/git-status.md) — inspect changed, staged, and untracked files.
3. [`git-add`](git-notes/git-add.md) — stage changes for a commit.
4. [`git-diff`](git-notes/git-diff.md) — inspect line-by-line changes.
5. [`git-commit`](git-notes/git-commit.md) — record a staged snapshot.
6. [`git-log`](git-notes/git-log.md) — inspect commit history.
7. [`git-branch`](git-notes/git-branch.md) — understand parallel lines of work.
8. [`git-switch`](git-notes/git-switch.md) — move between branches or create one.
9. [`git-merge`](git-notes/git-merge.md) — combine another branch into the current branch.
10. [`git-stash`](git-notes/git-stash.md) — temporarily store unfinished changes.
11. [`git-remote`](git-notes/git-remote.md) — understand named remote repositories.
12. [`git-fetch`](git-notes/git-fetch.md) — download remote history without integrating it.
13. [`git-pull`](git-notes/git-pull.md) — fetch and integrate remote changes.
14. [`git-push`](git-notes/git-push.md) — publish local commits to a remote.

## Workflow records

- [`workflow-note-1.md`](docs/workflow-note-1.md) records the first branch → pull request → merge exercise.
- [`workflow-note-2.md`](docs/workflow-note-2.md) records the second exercise.

## Suggested practice loop

Use a disposable branch so the default branch remains readable:

```bash
git switch -c learn/topic-name
# edit or add a note
git status
git diff
git add <path>
git diff --staged
git commit -m "docs: describe topic"
git push -u origin learn/topic-name
```

Then open a pull request, re-read its complete diff, and merge only after the
content and links are correct. Start a fresh branch from an up-to-date default
branch for the next exercise.

## Contributing a note

- Keep each `git-notes/` file focused on one Git command or concept.
- Use commands that can be copied safely, and explain placeholders such as
  `<path>` or `<branch>`.
- Link every new note from this README.
- Check Markdown links and review `git diff --check` before opening a pull request.
