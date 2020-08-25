---
layout: note
title: Methods
parent: C#
nav_exclude: true
---

# Methods
In C# every statement is executed within a method. Methods are blocks of code that carry out a single, pre-defined function. They can be defined inside of [[Classes]], structures and interfaces. e.g.

- `=>` Arrow functions should not be used for methods
    - Works well with `.this`
Methods should end with arguments`()`.

[[Object Oriented Programming]]

### Calling a Method
Calling the method WriteLine inside of the class Console:
```cs
Console.WriteLine("Hello World");
// Class.Method("Statement")
```