---
layout: note
title: Simple Types
parent: C#
grand_parent: Home
---

# Simple Types

Types are specific forms of data with specific structure & set limits.

- Value types store data directly
- Referance types store referances to data stored elsewheer. (Think of a shortcut on your computer).

In addition to [[Number Types]] there are three more basic types:

```cs
bool myBool; // True || False logical type (8 bit, the smallest value C# will allow you to store)

char myChar; // A single 'Character' represents unicode characters(16 bit, 65,535 possible characters stored)
// Character literals should be written with 'single quotes'

string myString; // An array of char's.
// Strings should be written in "double quotes"
```

- (Further info on [[Strings]] here).

Many other types exist in C#. However those are all made up of the above simple types in combination with [[Number Types]]

```cs
DateTime myDate;
```

and

```cs
TimeSpan myTime;
```

---

## Backlinks

- [[Literals]]
  - All [[Simple Types]], by default, have the [[Methods]] `.ToString()` which returns the fully qualified name of the type of the Object.
- [[Var Data Type and Anonymous Type]]
  - `var` is used to declare an implicitly typed _local_ variable, basically this means that the computer has to figure out what type of variable it is at completion time. It can make your code smaller, more structured and standardized, and easier to maintain by allowing you to replace explicit [[Simple Types]] (`int, bool, string` etc.) with a universal keyword.
