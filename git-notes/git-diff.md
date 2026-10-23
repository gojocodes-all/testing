# Git diff

`git diff` compares repository states without changing files or history. The
command you choose determines which changes appear.

## Inspect unstaged changes

```bash
git diff
```

This compares the working tree with the staging area. It shows changes that
have not been staged yet. Once a change is staged with `git add`, that change
no longer appears in plain `git diff`.

## Inspect staged changes

```bash
git diff --staged
```

This compares the staging area with the current commit (`HEAD`). Use it before
committing to review exactly what the next commit will contain.
`git diff --cached` is an equivalent spelling.

## Inspect all changes since the current commit

```bash
git diff HEAD
```

This compares the working tree with `HEAD`, so it includes both staged and
unstaged changes.

Add `-- <path>` to any of these commands to inspect one file or directory:

```bash
git diff -- README.md
git diff --staged -- git-notes/
```

For a compact overview, use `--stat`; to list only affected paths, use
`--name-only`. These commands are read-only and are safe to run while
reviewing work.
