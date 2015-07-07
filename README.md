# Git Cheat Sheet
This is written to teach myself Git and to be a quick reference of useful Git commands.
## Initialisation
Start with a new Git project
```bash
$ git init
```
Start with an existing Git project
```bash
$ git clone [url]
```
## Configuration
Set username and email
```bash
$ git config --global user.name [name]
$ git config --global user.email [email]
```
Enable colour
```bash
$ git config --global color.ui auto
```
List all configs
```bash
$ git config --list
```
## Working commands
To get current status of the repository
```bash
$ git status
```
### Branches
Display local branches and the current branch is starred
```bash
$ git branch
```
Display all branches, especially to see the branch origin/master
```bash
$ git branch -a
```
Add a new branch
```bash
$ git branch [newBranchName]
```
### Checkouts
Change to a commit version
```bash
$ git checkout [commitId]
```
Change to a branch
```bash
$ git checkout [branchName]
```
Create and change to a branch
```bash
$ git checkout -b [newBranchName]
```
### Remotes
Display remotes
```bash
$ git remote
```
Display remotes with more information
```bash
$ git remote -v
```
Add remote
```bash
$ git remote add [remoteName] [url]
```
**Note:** Useful remote names: origin or upstream
Update changes from local to remote
```bash
$ git push [toBranch] [fromBranch]
```
Update changes from remote to local
```bash
$ git pull [fromBranch] [toBranch]
```
Update changes from remote to local remote branch
```bash
$ git fetch [fromBranch]
```
### Merges
Merge two branches (branch1 and branch2) into current branch
```bash
$ git merge [branch1] [branch2]
```
**Note 1:** If having conflicts, resolve, add and commit

**Note 2:** Fast-forward merge happens when the branch to merge into is an ancestor of the other

Abort a merge
```bash
$ git merge --abort
```
### Staging
Add all current changes to staging area
```bash
$ git add .
```
Add a file to staging area
```bash
$ git add [file]
```
### Removes
Remove a file from Git repository
```bash
$ git rm [file]
```
Remove a directotry from Git repository
```bash
$ git rm -r [directory]
```
### Commits
Commit staged changes with commit message
```bash
$ git commit -m "message"
```
Commit and add local changes in tracked files wiht commit message
```bash
$ git commit -am "message"
```
### Logs
Display a log of commits
```bash
$ git log
```
Display a log of commits with more information
```bash
$ git log --stat
```
Display commit tree
```bash
$ git log --graph --oneline [branch1] [branch2]
```
Display a fixed number of commits
```bash
$ git log -n [number]
```
Display a log of commits for branch specified
```bash
$ git log [branch]
```
Show information about a commit
```bash
$ git show [commitId]
```
