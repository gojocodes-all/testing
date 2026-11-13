# Git switch

`git switch <branch>` changes the current branch and updates the working tree
and staging area to match that branch's commit, while preserving changes Git
can carry across safely.

Switch to an existing branch:

```bash
git switch learn/topic-name
```

Create a new branch from the current commit and switch to it:

```bash
git switch -c learn/topic-name
```

Before switching, review the current work:

```bash
git status
git diff
git diff --staged
```

Git normally keeps compatible uncommitted changes during a switch and refuses
the operation when it would overwrite them. A successful switch is therefore
not a cleanup step: the changes may follow you to the destination branch.
Commit work that belongs in history, or stash it deliberately, before changing
context.

To return to the previously checked-out branch, use:

```bash
git switch -
```

After switching, run `git status` again and confirm the branch named in its
first line before editing, committing, or pushing.
