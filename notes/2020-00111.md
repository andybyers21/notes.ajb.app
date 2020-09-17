---
layout: note
title: Numbers & Arithmetic in JavaScript
parent: JavaScript
grand_parent: Home
---

# Numbers & Arithmetic in JavaScript

Numbers are the building blocks of programming language. Extra big or small numbers can be written with scientific notation.

- Numbers can be written with or without decimals in JavaScript

```js
var x = 123e5; // 12300000
var y = 123e-5; // 0.00123
```

**JavaScript does not define different types of numbers (integers, short, long, floating-point etc)** unlike many other coding languages. numbers are always stored as _double floating point numbers_. Following the international IEEE 754 standard which stores numbers in the 64 bits, where the number (the fraction) is stored in bits 0 to 51, the exponent in bits 52 to 62, and the sign in bit 63.

---
