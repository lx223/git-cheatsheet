# Git Cheat Sheet
This is written to teach myself Git and to be a quick reference of useful Git commands.

## Table of Contents
- [Initialisation](#initialisation)
- [Configuration](#configuration)
- [Work cases](#work-cases)
    - [Initialise repository](#initialise-repository)
    - [Setting up Git aliases for Linux style terminal](#setting-up-git-aliases-for-linux-style-terminal)
- [Specific commands](#working-commands)
    - [Branches](#branches)
    - [Checkouts](#checkouts)
    - [Remotes](#remotes)
    - [Merges](#merges)
    - [Staging](#staging)
    - [Removes](#removes)
    - [Commits](#commits)
    - [Logs](#logs)
    - [Stash](#stash)
    - [Revert](#revert)

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

## Work cases
### Initialise repository
To start with an empty repository
```bash
$ cd [repository]
$ git init
$ git add .
$ git commit -m "Inital commit"
```

To start with a remote repository
```bash
$ cd [repository]
$ git clone [remoteUrl]
```

### Setting up Git aliases for Linux style terminal
If there is no .bash_profile file under ~, create one. Open it with a text editor and enter the following.

```bash
# Setting Git commands aliases
alias gt='gitk --all &'
alias gu='git gui &'
alias gs='git status'
alias gf='git fetch'
alias gb='git branch'
alias gc='git checkout'
alias gp='git pull --rebase'
alias ga='git add'
alias grb='git rebase'
alias gps='git push'
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
Display remote branches
```bash
$ git branch -r
```
Add a new branch
```bash
$ git branch [newBranchName]
```
Delete a branch
```bash
$ git branch -d [branchName]
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
Remove a file from Git repository and file system
```bash
$ git rm [file]
```
Remove a directotry from Git repository and file system
```bash
$ git rm -r [directory]
```
Remove a file from Git repository but not file system
```bash
$ git rm --cached [file]
```
Remove a directotry from Git repository but not file system
```bash
$ git rm --cached -r [directory]
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
### Stash
Stash modified stracked files temporarily
```bash
$ git stash
```
Restore the most recently stashed files
```bash
$ git stash pop
```
### Revert
Revert a commit
```bash
$ git revert [commitId]
```
