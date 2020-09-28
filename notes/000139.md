---
layout: note
title: The JavaScript Comma
parent: JavaScript
grand_parent: Home
---

# The JavaScript Comma

The comma `,` operator is sometimes used to write shorter code. It allows us to several expressions, dividing them with a comma `,` each is evaluated but only the last is returned. For example:

```js
let a = (1 + 2, 3 + 4);

alert(a);

// 7
```

Here, the first expression `1 + 2` is evaluated and its result is thrown away. Then, `3 + 4` is evaluated and returned as the result. _Note that the comma operator has very low precedence, lower than `=`, so parentheses are important in the example above. Without them: `a = 1 + 2, 3 + 4` evaluates `+` first, summing the numbers into `a = 3, 7`, then the assignment operator `=` assigns `a = 3`, and the rest is ignored. It’s like `(a = 1 + 2), 3 + 4.`_

---
