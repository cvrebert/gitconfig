gitconfig
=========

git command aliases to make its interface halfway logical and user-friendly

## Command summary

### Core
* `clobber <filepath(s)>` : Clobbers part of the working copy with the original version from the current branch
* `amend` : Amends the last commit to include the changes currently in staging
* `amend-author 'J. Random <j.random@example.com>'` : Amends the authorship information of the last commit
* `stage <filepath(s)>` : Adds the changes in the given files to the staging area from the working copy
* `stage-patch <optional filepath(s)>` : Interactively stage parts of changes in the given files to the staging area from the working copy
* `unstage <filepath(s)>` : Un-stages the changes in the given files from the staging area back to the working copy

### Diff-related
* `diff-unstaged <optional filepath(s)>` : Diffs the working copy against staging
* `difftool-unstaged <optional filepath(s)>` : Graphically diffs the working copy against staging
* `wdiff-unstaged <optional filepath(s)>` : Wordwise-diffs the working copy against staging

* `diff-staged <optional filepath(s)>` : Diffs staging against the last commit
* `difftool-staged <optional filepath(s)>` : Graphically diffs staging against the last commit
* `wdiff-staged <optional filepath(s)>` : Wordwise-diffs the working copy against the last commit

### Branch-related
* `branches` : Lists all branches, grouped by merge status relative to the current branch
* `new-branch <name>` : Creates a new branch off of the current commit with the given name
* `push-to <remote>` : Pushes the current branch to the given remote
* `force-push-to <remote>` : Forcibly pushes the current branch to the given remote. Also a nice *Star Wars* reference.
* `delete-branch-local <branch>` : Deletes the given branch locally
* `delete-branch-origin <branch>` : Deletes the given branch from the remote origin server
* `set-branch-head <branch> <SHA>` : Sets the HEAD pointer of the given branch to the given commit

### Merge-related
* `resolve` : Opens your graphical merge/diff tool to resolve any outstanding merge conflicts
* `abandon-merge` : Abandons the current merge and returns the working copy to its previous state

### Stash-related
* `stashes` : Lists all stashes
* `stash-changes` : Stashes all uncommitted changes
* `unstash <optional stash ID>` : Un-stashes the changes by applying them to the working copy and staging area
* `delete-stash <optional stash ID>` : Permanently deletes the stashed changes

### Rebase-related
* `rebase-against <branch>` : Rebases the current branch against the given branch such that your commits will now have been made against the given branch's HEAD.
* `rebase-since <SHA>` : Interactively rebases the current branch, allowing you to remix (i.e. squash, reorder, remove) all commits after the given commit
