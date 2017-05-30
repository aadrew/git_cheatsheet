# GIT Help

## Working locally
* `git status` will give you the current state of your local branch including file changes.
* `git add fileName` will add the file to staging for commits
* `git commit -m "my commit message"` will commit all staged changes with the given message. you can then push that commit to the upstream branch on the server
* `git checkout -- fileName` will reset changes to a file that isn't staged.
* `git reset HEAD fileName` will reset changes to a file that is staged.
* `git merge branchToMergeIn` will locally merge a branch, *into* the branch you have checked out.  
* You can replace a filename with `.` or `*` to apply a command to all files. for example `git add .` will stage all changes.

## Make a new branch
* `git checkout -b myFeatureBranch` will checkout and create a new branch based on whatever branch you are currently on. It's good to checkout master before running this.

## Push a branch to the server
* `git push -u origin myFeatureBranch` will create and push to the upstream branch on the server.
