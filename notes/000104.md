---
layout: note
title: Modules
parent: Python
grand_parent: Home
---

# Modules

Modules are like a mini program that can be dropped into your Python programs. Each module is an individual file that can be combined to create a program, app, website or whatever else you can think of. This means you can modify or edit one particular element of your app without affecting the rest (following [[Object Oriented Programming]] principals).

A python module can contain a set of variables, [[Functions]] and [[Classes and Objects]]. **A module is a mini-program in itself.**

Use:

```py
import module_name
```

When you need to use code from another module in your app. Alternatively import module code within [[Namespaces]]:

```py
from module_name import object_name
```

_- or -_

```py
from module_name import *
```

to import all objects

**When you import a module into python code it will only initialize once.** No matter how many times you use it.

---
