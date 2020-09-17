---
layout: note
title: Underscores in Interactive Mode
parent: Python
grand_parent: Home
---

# Underscores in Interactive Mode

## In interactive mode, the last printed expression is assigned to the variable `_`

This means that when you are using Python as a desk calculator, it is somewhat easier to continue calculations, for example:

```py
>>> tax = 12.5 / 100
>>> price = 100.50
>>> price * tax
12.5625
>>> price + _
113.0625
>>> round(_, 2)
113.06
```

---
