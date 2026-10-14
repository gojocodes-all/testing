# Git stash

`git stash push` records staged and unstaged changes to tracked files, then removes those changes from the working tree. Plain `git stash` is an alias for `git stash push`.

Untracked and ignored files are excluded by default:

- `git stash push -u` also includes untracked files.
- `git stash push -a` also includes untracked and ignored files.

Use `git stash list` to inspect saved entries before restoring one. `git stash apply` reapplies an entry while keeping it in the stash; `git stash pop` reapplies it and drops it if the operation succeeds.
