---
layout: note
title: Constant Variables
parent: JavaScript
grand_parent: Home
---

# Constant Variables

**To declare a constant, an unchanging variable, use `const` instead of `let`** These cannot be reassigned and doing so would return an error in your code.^[When a programmer is sure that a variable will never change, they can declare it with `const` to guarantee and clearly communicate that fact to everyone.involved.]

It is a widespread practice to use constants as aliases for difficult-to-remember values that are known prior to execution, **such constants are named using capital letters and underscores.** For example, constants for colors in hex format:

```js
const COLOR_RED = '#F00';
const COLOR_GREEN = '#0F0';
const COLOR_BLUE = '#00F';
const COLOR_ORANGE = '#FF7F00';

// ...when we need to pick a color
let color = COLOR_ORANGE;
alert(color); // #FF7F00
```

The benefits of this are:

- COLOR_ORANGE is much easier to remember than "#FF7F00".
- It is much easier to mistype "#FF7F00" than COLOR_ORANGE.
- When reading the code, COLOR_ORANGE is much more meaningful than #FF7F00.

The code itself does not care if you use capitals to name your constants however there are constants that are known prior to execution (like the hexadecimal example above) and _there are constants that are calculated in run-time, during the execution,_ but do not change after their initial assignment:

`const pageLoadTime = /* time taken by a webpage to load */;`

The value of `pageLoadTime` is not known prior to the page load, so it’s named normally. But it’s still a constant because it doesn’t change after assignment. In other words, **capital-named constants are only used as aliases for “hard-coded” values.**

---
