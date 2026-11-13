# Git branches

A branch is a movable name that points to a commit. Creating a branch does not
copy the repository or change files; it creates another reference from which
new commits can continue independently.

List local branches and show the current one with an asterisk:

```bash
git branch
```

Create a branch without switching to it:

```bash
git branch learn/topic-name
```

For the usual start-a-task workflow, create the branch and switch to it in one
step:

```bash
git switch -c learn/topic-name
```

Choose a short name that describes the work. Before creating a task branch,
switch to the intended base branch and update it so the new branch starts from
the correct commit.

After a branch has been merged and is no longer needed, inspect branches whose
tips are already reachable from the current branch:

```bash
git branch --merged
```

Then delete the local branch with:

```bash
git branch -d learn/topic-name
```

The lowercase `-d` form refuses to delete an unmerged branch. Treat that
refusal as a prompt to inspect the branch and its pull request; do not replace
it with forced deletion unless losing the unmerged commits is intentional.
Deleting a local branch does not delete a same-named branch on a remote.
