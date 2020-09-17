---
layout: note
title: Literals
parent: C-Sharp
grand_parent: Home
---

# Literals

With the exception of interface and dynamic (and one or two edge cases), every type in C-Sharp should be derived from objects ([[Object Oriented Programming]]).

## String Literals

All [[Simple Types]], by default, have the [[Methods]] `.ToString()` which returns the fully qualified name of the type of the Object.

```cs
var makeString = 22.ToString();
// "22"
```

## Template Literals

Template literals make complex [[Handling strings in C-Sharp]] easier to maintain by using string interpolation. Simply put, filling in the blanks in a string by using elements in an object.

String literals can be multiline which removes the need for line breaks `\n` and can also concatenate. `"${a + b}";`

## Object Literals

(WIP)

---
