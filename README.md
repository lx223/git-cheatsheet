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
### Working with remotes
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
$ git remote add origin [url]
```
Update remote
```bash
$ git push [toBranch] [fromBranch]
```
Update local
```bash
$ git pull [fromBranch] [toBranch]
```
Update local remote
```bash
$ git fetch [fromBranch]
```
### Working with merges
Merge two branches (branch1 and branch2) into current branch
```bash
$ git merge [branch1] [branch2]
```
If having conflicts, resolve, add and commit

### Working with logs
Display a log of commits
```bash
$ git log
```
Display a log of commits for branch specified
```bash
$ git log [branch]
```
