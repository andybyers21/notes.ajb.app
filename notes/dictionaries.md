---
layout: note
title: Dictionaries
parent: Python
nav_exclude: true
---

# Dictionaries

Dictionaries are similar to arrays. They use **keys** and **values** to manage data (rather than indexes). Each value can be accessed by calling it's key. A value can be any object (strings, ints, lists etc). **Only immutable object can be written to a dictionary. Use tuples, not lists.** (Ref: [[Tuples and Lists]])

Dictionaries can be written as follows:

```py
phonebook = {}
phonebook["Bill"] = "98765432"
phonebook["George"] = "44765292020298"
phonebook["Sue"] = "019191872653"
```

_- or -_

```py
phonebook = {"Bill" = "98765432",
             "George" = "44765292020298",
             "Sue" = "019191872653"}
```

Note: **Dictionaries don't keep key-value pairs in order**. You will need to use a for loop to iterate over a dictionary:

```py
for name, number in phonebook.items():
    print(f"{name}'s number is {number}")
```

Remove a value:

```py
del phonebook["George"]
```

_- or -_

```py
phonebook.pop["Bill"]
```
## Backlinks
* [[Tuples and Lists]]
	* **Since lists are mutable they cannot be used in [[Dictionaries]].**

