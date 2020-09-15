---
layout: note
title: Git add-commit Shortcut
parent: Version Control
nav_exclude: true
---

# Git add-commit Shortcut

Find yourself typing the following an awful lot?
```shell
$ git add .
$ git commit -m "an awful lot of typing"
```

Run the following command to use aliases:
```shell
$ git config --global alias.ac '!git add . && git commit -m'
```

Then you can type:
```shell
$ git ac "much better"
```