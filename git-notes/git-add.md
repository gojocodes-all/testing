# Git add

`git add <path>` copies the path's current content into Git's index (also called
the staging area), preparing that version for the next commit. It does not move
or delete the working file.

```bash
git add README.md
git diff --staged
```

Staging records the content that exists when `git add` runs. If you edit the
file again afterward, the earlier version remains staged while the newer edits
are unstaged. Use `git diff --staged` to review the staged snapshot and plain
`git diff` to review the additional working-tree edits. Run `git add` again if
the newer content should replace the staged version.

Stage selected change hunks instead of the whole file with:

```bash
git add -p README.md
```

To unstage a path without discarding its working-tree changes, use:

```bash
git restore --staged -- README.md
```

Review the staged diff before committing so the next snapshot contains only
the intended changes.
