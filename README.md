# GIT Help

## Working locally
`git status` will give you the current state of your local branch including file changes.

`git add fileName` will add the file to staging for commits

`git commit -m "my commit message"` will commit all staged changes with the given message. you can then push that commit to the upstream branch on the server

`git checkout -- fileName` will reset changes to a file that isn't staged.

`git reset HEAD fileName` will reset changes to a file that is staged.

`git merge branchToMergeIn` will locally merge a branch, *into* the branch you have checked out.  

You can replace a filename with `.` or `*` to apply a command to all files. for example `git add .` will stage all changes.

## Make a new branch
`git checkout -b myFeatureBranch` will checkout and create a new branch based on whatever branch you are currently on. It's good to checkout master before running this.

## Push a branch to the server
`git push -u origin myFeatureBranch` will create and push to the upstream branch on the server.

## Revert
###The git `revert` command undoes a committed snapshot. But, instead of removing the commit from the project history, it figures out how to undo the changes introduced by the commit and appends a new commit with the resulting content. This prevents Git from losing history.

`git revert <commit>`
Generate a new commit that undoes all of the changes introduced in <commit>, then apply it to the current branch.

## Reset
###Depending on its usage, `reset` removes files or commits.  More importantly it removes HISTORY.  Therefore, be very careful when using it.

`git reset <file>`
Remove the specified file from the staging area, but leave the working directory unchanged. This unstages a file without overwriting any changes.

`git reset`
Reset the staging area to match the most recent commit, but leave the working directory unchanged. This unstages all files without overwriting any changes, giving you the opportunity to re-build the staged snapshot from scratch.

`git reset --hard`
Reset the staging area and the working directory to match the most recent commit. In addition to unstaging changes, the --hard flag tells Git to overwrite all changes in the working directory, too. Put another way: this obliterates all uncommitted changes, so make sure you really want to throw away your local developments before using it.

`git reset <commit>`
Move the current branch tip backward to <commit>, reset the staging area to match, but leave the working directory alone. All changes made since <commit> will reside in the working directory, which lets you re-commit the project history using cleaner, more atomic snapshots.

`git reset --hard <commit>`
Move the current branch tip backward to <commit> and reset both the staging area and the working directory to match. This obliterates not only the uncommitted changes, but all commits after <commit>, as well.
