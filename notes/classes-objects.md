---
layout: note
title: Classes and Objects
parent: Python
nav_exclude: true
---

# Classes and Objects

**Everything in python is an object.** (Ref: [[Object Oriented Programming]]) Objects are an encapsulation of variables, [[Functions]] etc into a single entity. **Objects get their variables and functions from classes. Classes are a template of your objects.** Note: Classes cannot be empty, every class must have at least one object. (_use `pass` if your class is empty_).

To assign a class to an object:

```py
object_name = ClassName
```

Now `object_name` holds and object of `ClassName`

## To access a variable within a class

Works much like any other variable

```py
object.variable
```

## To access a function within a class

```py
new_object.function()
```