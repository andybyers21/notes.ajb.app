---
layout: note
title: Namespaces
parent: Python
nav_exclude: true
---

# Namespaces

An assignment statement creates a _symbolic name_ that you can use to reference an object.

```py
mystring = "This is my string"
# (symbolic name) assigned = to (object)
```

Python organises symbolic names and objects into namespaces. **A namespace is a collection of the currently defined symbolic names and imformation about the objects assigned to them.** As python executes a program it creates namespaces and deletes them when they're no longer necessary. The 4 types of namespace.

1. **Built-in**
2. **Global**, Defined at the top level of the program or module.
3. **Enclosing**, defined within [[Functions]].
4. **Local**, Defined at the innermost scope (nested functions for example).

Python will start at the local scope and work it's way out to find what it's looking for.