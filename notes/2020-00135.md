---
layout: note
title: String Operations
parent: Python
grand_parent: Home
---

# String Operations

```py
string = "This is my string"
```

---

- Index of the first occurrence:

```py
string.index("s")
# 3
```

- How many occurrences of:

```py
string.count("s")
# 3
```

- Length:

```py
len(string)
# 17
```

- Starts with / ends with (produces a bool):

```py
string.startswith("a") # False
string.endswith("g") # True
```

- Upper/ Lowercase:

```py
string.upper()
string.lower()
```

## Slice

- Slice, you can use negative numbers to count from the end of the string:

```py
string[4:14]
# ' is my str'
```

- Leave the first number blank to start at the beginning `[:14]`
- Leave the last number blank to end at the end `[4:]`

- Split a string into a list at a defined place:

```py
string.split("m")
# ['this is ', 'y string']
```

---
