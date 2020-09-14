---
layout: default
title: JavaScript
nav_order: 10
has_children: true
has_toc: false
---

# JavaScript

\__currently working on transferring notes over from obsidian.md_

## JavaScript Basics

- [JavaScript Basics](../javascript/JavaScript Basics)
- [The JavaScript Comma](../javascript/The JavaScript Comma)
- [JavaScript Comments](../javascript/JavaScript Comments)
- [JavaScript Events](../javascript/JavaScript Events)

## JavaScript Functions

- [JavaScript Functions](../javascript/JavaScript Functions)
  - [Anonymous Functions](../javascript/Anonymous Functions)
  - [Function Parameters](../javascript/Function Parameters)
  - [Function Scope and Conflicts](../javascript/Function Scope and Conflicts)
  - [Function Return Values](../javascript/Function Return Values)
  - [Default Values in Functions](../javascript/Default Values in Functions)
- [Functions Summary](../javascript/Functions Summary)
- [Function Expressions](../javascript/Function Expressions)
  - [Callback Functions](../javascript/Callback Functions)

## JavaScript Variables

- [Variables in JavaScript]
  - [Variables in the Real World - JS]
  - [Constant Variables]
- [The Difference Between Var and Let]

## Data Types in JavaScript

A value in JavaScript is always of a certain type. There are **8 major datatypes** including strings and numbers. We can put any type of dataset in a variable, for example it could be a string then change to a number later on. Programming languages that allow such things, such as JavaScript, are called “dynamically typed”, meaning that there exist data types, but variables are not bound to any of them.

```javascript
let message = 'hello';
message = 123456;
```

### Numbers and Arithmetic

- [JS Hexadecimal]
- [Numbers and Arithmetic in JavaScript]
  - [Adding Numbers and Strings]
  - [Arithmetic in JavaScript]
- [JavaScript Precision]
- [JavaScript Operators]
- [Unary +]
- [JavaScript = Assignment]
- [Modify-in-Place]
- [NaN is Not a Number]
- [Infinity (in JavaScript - not the stones)]
- [Increment - Decrement]
- [Type Conversion Examples]

### Handling text — strings in JavaScript

- [Strings (Handling Text in JavaScript)]
  - [Concatenation in Context]
- See also [Adding Numbers and Strings] (duplicate from previous section).
- [Template Literals (or Embeds)]

In JavaScript, primitive values, like `"Java is not JavaScript"` **can** have properties or methods, as the language treats all values as objects when executing.

- [Searching a Strings Properties], such as string length, indexOf and search.
- [Extracting String Parts]
- [Replacing String Content]
- [Converting Upper case to Lower case]

An exhaustive list of string methods and properties [can be found here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)

- [Converting a String to an Array]

### Additional Data Types

In addition to text strings and numbers there are 6 more major data types to be found in JavaScript.

- [BigInt]
- [Boolean (true-false logical type)]
- [The Null Value]
- [The Undefined Value]
- [Objects and Symbols]
- [The typeof Operator]

## Conditionals Operators in JavaScript

- [Conditionals in JavaScript]
  - [JavaScript Comparisons]
  - [if, else and elseIf]
  - [Conditional operator (question mark)]
  - [The Switch Statement]

### Logical Operators

- [Truthy and Falsy Values]

There are three logical operators in JavaScript. They can be applied to any value of any type (not just boolean) and can return a result of any type.

- [The OR Logical Operator]
- [The AND Logical Operator]
- [The NOT Logical Operator]

## JavaScript Best Practices

**Do not create Number objects. It slows down execution speed. The new keyword complicates the code. This can produce some unexpected results**

**wrap your code block with curly braces `{}` every time you use an if statement, even if there is only one statement to execute and it is not necessary. Doing so improves readability.**

- [A Variable Should Have Clear and Obvious Naming]
- [Naming a Function]
- [One Function - One Action]

### Writing code in JavaScript

- [Writing JS code]
