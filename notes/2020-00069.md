---
layout: note
title: Git Security
parent: Version Control
grand_parent: Home
---

# Git Security

Each Git is checksummed before it is stored, then referenced to by that checksum, meaning it is impossible for any changes to be made to your filesystem without Git knowing about it. This is part of the philosophy of Git and built in at the lowest levels.

In addition (in conjunction with local file storage) you can't lose information in transit of get file corruption without Git knowing about it.

> The mechanism that Git uses for this checksumming is called a SHA-1 hash. This is a 40-character string composed of hexadecimal characters (0–9 and a–f) and calculated based on the contents of a file or directory structure in Git. A SHA-1 hash.

Git also stores everything in it's database by the hash value of it's contents rather than arbitrary file names meaning duplication of a filename is impossible.

When you carry out any operations in Git it is (generally) only adding data. It is hard to get the system to do anything that is not undoable or to make it erase data in any way. You will only lose data if you haven't made a commit yet.

---
