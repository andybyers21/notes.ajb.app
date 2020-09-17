---
layout: note
title: GitHub Cheatsheet
parent: Version Control
grand_parent: Home
---

# GitHub Cheatsheet

## Configure tooling

_Configure user information for all local repositories_

Set the name you want attached to your commit transactions:

```shell
$ git config --global user.name "[name]"
```

Set the email you want attached to your commit transactions:

```shell
$ git config --global user.email "[email address]"
```

Enable colorization of command line output

```shell
$ git config --global color.ui auto
```

## Branches

_Branches are an important part of working with Git. Any commits you make will be made on the branch you’re currently “checked out” to. Use git status to see which branch that is._

Create new branch:

```shell
$ git branch [branch-name]
```

Switch to the specified branch and update the working directory:

```shell
$ git checkout [branch-name]
```

Combine the specified branch’s history into the current branch. (This is usually done in pull requests, but is an important Git operation.):

```shell
$ git merge [branch]
```

Delete the specified branch:

```shell
$ git branch -d [branch-name]
```

## Create repositories

To start a new repository:

```shell
$ git init
```

link the local repository to an empty GitHub repo:

```shell
$ git remote add origin [url]
```

Turn an existing directory into a Git repository:

- Clone (download) a repository that already exists on GitHub, including all of the files, branches, and commits

```shell
$ git clone [url]
```

## Synchronize changes

_Synchronize your local repository with the remote repository on GitHub.com_

Download all history from the remote tracking branches:

```shell
$ git fetch
```

Combine remote tracking branches into current local branch:

```shell
$ git merge
```

Upload all local branch commits to GitHub:

```shell
$ git push
```

Update your current local working branch with all new commits from the corresponding remote branch on GitHub. (git pull is a combination of git fetch and git merge):

```shell
$ git pull
```

## Make changes

_Browse and inspect the evolution of project files_

List version history for the current branch:

```shell
$ git log
```

List version history for a file, including renames:

```shell
$ git log --follow [file]
```

Show content differences between two branches:

```shell
$ git diff [first-branch]...[second-branch]
```

Output metadata and content changes of the specified commit:

```shell
$ git show [commit]
```

Snapshot file in preparation for versioning:

```shell
$ git add [file]
```

Record file snapshots permanently in version history:

```shell
$ git commit -m "[descriptive message]"
```

## Redo commits

_Erase mistakes and craft replacement history_

Undo all commits after `[commit]`, preserving changes locally:

```shell
$ git reset [commit]
```

Discard all history and changes back to the specified commit:

```shell
$ git reset --hard [commit]
```

**CAUTION! Changing history can have nasty side effects. If you need to change commits that exist on GitHub (the remote), proceed with caution.**

## .gitignore

Sometimes it may be a good idea to exclude files from being tracked with Git. This is typically done in a special file named .gitignore. [templates here](https://github.com/github/gitignore.)

---
