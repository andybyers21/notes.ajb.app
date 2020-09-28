---
layout: note
title: Git Fundamentals
parent: Version Control
grand_parent: Home
---

# Git Fundamentals

ref:- [[Git Command Line Reference]]

ref:- [[Git Glossary]]

Git is different from many other version control systems (VCS) in the way it handles data. Most other systems (CVS, Subversion, Perforce, Bazaar, and so on) work by saving a copy of your data, then saving a document of the changes made to your files at any given time. This is commonly described as delta-based version control.

Git, on the other hand stores your data as a series of snapshots of the filesystem. Essentially, every time you **commit**, Git takes a picture of what your data looks like in comparison to the previous images. To be efficient, if any of the files haven't changed it won't bother taking a picture of that document again and will provide a link to the previous file that is already in storage. This makes Git more like a mini filesystem (with some powerful tools built on top) rather than "just" a VCS.

When working on a project stored in Git, Git provides clarity on **when you changed a file**, **why you did it** and **what the contents of the change were** open for review at any time in the future. There are many different ways you can use Git, such as from the command line or via one of many different GUI's with varying different levels of capability.

## The 3 states of Git

### Modified, Staged, and Committed

- **Modified** means that you have changed the file but have not committed it to your database yet.
- **Staged** means that you have marked a modified file in its current version to go into your next commit snapshot.
- **Committed** means that the data is safely stored in your local database.

## The 3 main sections of a Git project

### The working tree, the staging area, and the Git directory.

- **The working tree**, also know as the working directory, are where the files are pulled from the database for you to work on.
- **The staging area**, is a file in you Git directory that stores information on what will go into your next commit. (Sometimes known as an "index").
- **The Git directory** is where Git stores the _metadata_ and _object database_ for your project. This is the most important part of Git. (It is what is copied when you clone a repository from another computer).

---
