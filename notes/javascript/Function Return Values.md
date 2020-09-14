---
layout: note
title: Function Return Values
parent: JavaScript
nav_exclude: true
---

# Function Return Values

It is important to understand that some functions don't return a significant value. And some do. Return values are, quite simply, the value that a function returns when it completes.

```javascript
let myText = 'The weather is cold';
let newString = myText.replace('cold', 'warm');
console.log(newString); // Should print "The weather is warm"
// the replace() string function takes a string,
// replaces one substring with another, and returns
// a new string with the replacement made
```

The `replace()` function is invoked on the myText string, and is passed two parameters:

1. the substring to find (`cold`).
2. the string to replace it with (`warm`).

When the function completes, it returns a value, which is a new string with the replacement made. In the code above, the result of this return value is saved in the variable `newString`.

To return a value from a custom function, you need to use the `return` keyword.

```javascript
function random(number) {
  const result = Math.floor(Math.random() * number);
  return result;
}
```

We are returning the result of the calculation Math.floor(Math.random() \* number) each time the function is called. This return value appears at the point the function was called, and the code continues.

## Returning a value

A function can return a value back into the calling code as the result. The simplest example would be a function that sums two values:

```javascript
function sum(a, b) {
  return a + b;
}

let result = sum(1, 2);
alert(result); // 3
```

The directive return can be in any place of the function. When the execution reaches it, the function stops, and the value is returned to the calling code (assigned to result above). There may be many occurrences of return in a single function. For instance:

```javascript
function checkAge(age) {
  if (age >= 18) {
    return true;
  } else {
    return confirm('Do you have permission from your parents?');
  }
}

let age = prompt('How old are you?', 18);

if (checkAge(age)) {
  alert('Access granted');
} else {
  alert('Access denied');
}
```

It is possible to use return without a value. That causes the function to exit immediately. For example:

```javascript
function showMovie(age) {
  if (!checkAge(age)) {
    return;
  }

  alert('Showing you the movie'); // (*)
  // ...
}
```

In the code above, `if checkAge(age)` returns false, then showMovie won’t proceed to the alert.

**A function with an empty return or without it returns undefined.** If a function does not return a value, it is the same as if it returns undefined:

```javascript
function doNothing() {
  /* empty */
}

alert(doNothing() === undefined); // true
```

An empty return is also the same as return undefined:

```javascript
function doNothing() {
  return;
}

alert(doNothing() === undefined); // true
```

**Never add a newline between return and the value.** For a long expression in return, it might be tempting to put it on a separate line, like this:

```javascript
return;
some + long + expression + or + whatever * f(a) + f(b);
```

That doesn’t work, because JavaScript assumes a semicolon after return. That’ll work the same as:

```javascript
return;
 (some + long + expression + or + whatever * f(a) + f(b))
So, it effectively becomes an empty return.
```

If we want the returned expression to wrap across multiple lines, we should start it at the same line as return. Or at least put the opening parentheses there as follows:

```javascript
return some + long + expression + or + whatever * f(a) + f(b);
```

And it will work just as we expect it to.
