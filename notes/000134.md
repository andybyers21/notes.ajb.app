---
layout: note
title: String Interpolation
parent: Python
grand_parent: Home
---

# String Interpolation

## C Style

- `%s` inject a string
- `%d` inject an int
- `%f` inject a float
- `%.<number of digits>f` Floating point numbers with a fixed amount of digits to the right of the dot.
- `%x`/`%X` Integers in hex representation (lowercase/uppercase)

followed by:

- `% variable_name` to be interpolated.
  _Use brackets if using multiple variables_

```py
name = "Andy"
surname = "Byers"
age = 37

string = "Hello my name is %s %s, I am %s years old" % (name, surname,  age)
# Hello my name is Andy Byers, I am 37 years old
```

## f-String

```py
name = "Andy"
surname = "Byers"
age = 37

string = f"Hello my name is {name} {surname}, I am {age} years old"
# Hello my name is Andy Byers, I am 37 years old
```

---
