---
layout: note
title: Function Expressions
parent: JavaScript
nav_exclude: true
---

# Function Expressions

In JavaScript a function is a special kind of expression. It can be written as follows:

```javascript
function sayHi() {
  alert('hello');
}
```

Another syntax for creating a function is called a **syntax expression** and can be written as follows:

```javascript
let sayHi = function () {
  alert('hello');
};
```

Here the function is assigned to the variable explicitly. No matter how the function is defined it will always be a value within the variable `sayHi`. The two code snippets product the same output. We can even print out that value using alert:

```javascript
function sayHi() {
  alert('Hello');
}

alert(sayHi); // shows the function code
```

Tha last line does not return the function because there or no parentheses after `sayHi`. _There are programming languages where any mention of a function name causes its execution, but JavaScript is not like that._ In JavaScript, a function is a value, so we can deal with it as a value. The code above shows its string representation, which is the source code.

We can copy a function to another variable:

```javascript
function sayHi() {
  // (1) create
  alert('Hello');
}

let func = sayHi; // (2) copy

func(); // Hello     // (3) run the copy (it works)!
sayHi(); // Hello    //     this still works too (why wouldn't it)
```

Here’s what happens above in detail:

The Function Declaration (1) creates the function and puts it into the variable named `sayHi`.
Line (2) copies it into the variable func. **Please note again: there are no parentheses after `sayHi`.** If there were, then `func = sayHi()` would write the result of the call `sayHi()` into `func`, not the function `sayHi` itself. Now the function can be called as both `sayHi()` and `func()`.

Note that we could also have used a Function Expression to declare sayHi, in the first line:

```javascript
let sayHi = function () {
  alert('Hello');
};

let func = sayHi;
// ...
```

Everything would work the same.

## Why is there a semicolon at the end?

You might wonder, why does Function Expression have a semicolon `;` at the end, but Function Declaration does not:

```javascript
function sayHi() {
  // ...
}

let sayHi = function () {
  // ...
};
```

The answer is simple:

There’s no need for `;` at the end of code blocks and syntax structures that use them like `if { ... }`, `for { }`, `function f { }` etc. A Function Expression is used inside the statement: `let sayHi = ...;`, as a value. It’s not a code block, but rather an assignment. The semicolon `;` is recommended at the end of statements, no matter what the value is. So the semicolon here is not related to the Function Expression itself, it just terminates the statement.
