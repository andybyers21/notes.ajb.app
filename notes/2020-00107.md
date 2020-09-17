---
layout: note
title: Python Naming Conventions
parent: Python
grand_parent: Home
---

# Python Naming Conventions

The naming conventions in python are a little messy. When writing code an internal standard will take precedence otherwise you should try to follow the below.

## Overriding Principal

**Names that are visible to a user (as public parts of an API) should follow conventions that reflect usage rather than implementation.**

## Naming Conventions

### Names to Avoid

Never use the characters `l` (lowercase letter L), `O` (uppercase letter O), or `I` (uppercase letter I) as single character variable names.

### Packages and Modules

- Modules should have **short, all-lowercase**. Use underscores if it will improve readability.
- Packages should also have short, all-lowercase names, although the use of underscores is discouraged.

### Class Names

- Class names should use **PascalCase**

### Function Names

Functions should be **alllowercase** with underscores if necessary to improve readability. (mixedCase is allowed only in contexts where that's already the prevailing style (e.g. threading.py), to retain backwards compatibility).

### Variable Names

Variables should follow the same conventions as [[Functions]]

- Type variables should use **PascalCase**
- Global variables should use **alllowercase**. Use underscores if necessary to improve readability.

### Function and Method Arguments

**Always use `self` for the first argument to instance methods.**

**Always use `cls` for the first argument to class methods.**

If a function argument's name clashes with a reserved keyword, it is generally better to append a single trailing underscore rather than use an abbreviation or spelling corruption. Thus `class_` is better than `clss`. (Perhaps better is to avoid such clashes by using a synonym.)

### Method Names and Instance Variables

Use the function naming rules: **lowercase with words separated by underscores as necessary** to improve readability.

Use a leading underscore only for non-public methods and instance variables.

**To avoid name clashes with subclasses, use two leading underscores to invoke Python's name mangling rules.**

### Constants

Constants are usually defined on a module level and written in \***\*ALL_CAPS\*\*** (with underscores separating words). Examples include MAX_OVERFLOW and TOTAL.

---
