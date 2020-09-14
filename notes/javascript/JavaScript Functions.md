---
layout: note
title: JavaScript Functions
parent: JavaScript
nav_exclude: true
---

# JavaScript Functions

Functions are a way of packaging functionality into a block in your code that you want to reuse multiple times. It is possible to define a function that executes when you call a functions name in your code. (A good alternative to writing out the same code multiple times). For example (The following commands, `document.querySelector` and `alert` are built in to all major browsers):

`let myVariable = document.querySelector('h1');`

`alert('hello!');`

**Something that looks like a variable name but is followed by something in brackets `( )` it is probably a function.** Functions often take **arguments**, bits of data they need to do their jobs. Which go inside the brackets, **separated by commas if there is more than one.** For example. The `alert(*)` function will make a pop up box appear inside a browser window. We need to give that a string (see above) as an argument to tell it what to say.

You can also define your own functions, such as:

```js
function multiply(num1, num2) {
  let result = num1 * num2;
  return result;
}
```

The above JS code takes two numbers as arguments and multiplies them. _Note: The return statement tells the browser to return the result variable out of the function so it is available to use. This is necessary because variables defined inside functions are only available inside those functions. This is called variable scoping. (Read more about variable scoping.)_

Rather than having to write out blocks of code every time you want your browser to execute a task you can call the function simply by typing the name followed by two parenthesis. e.g. `multiply ()`

## Functions Within Functions

You can even call functions from within functions, like so:

```js
function random(number) {
  return Math.floor(Math.random() * number);
}
```

This is often used as a way to keep code tidy — if you have a big complex function, it is easier to understand if you break it down into several sub-functions:

```js
function myBigFunction() {
  let myValue;

  subFunction1();
  subFunction2();
  subFunction3();
}

function subFunction1() {
  console.log(myValue);
}

function subFunction2() {
  console.log(myValue);
}

function subFunction3() {
  console.log(myValue);
}
```

Just make sure that the values being used inside the function are properly in scope. The example above would throw an error ReferenceError: myValue is not defined, because although the myValue variable is defined in the same scope as the function calls, it is not defined inside the function definitions — the actual code that is run when the functions are called. To make this work, you'd have to pass the value into the function as a parameter, like this:

```js
function myBigFunction() {
  let myValue = 1;

  subFunction1(myValue);
  subFunction2(myValue);
  subFunction3(myValue);
}

function subFunction1(value) {
  console.log(value);
}

function subFunction2(value) {
  console.log(value);
}

function subFunction3(value) {
  console.log(value);
}
```

## Outer variables

A function can access an outer variable (a variable in the global scope) as well, for example:

```js
let userName = 'John';

function showMessage() {
  let message = 'Hello, ' + userName;
  alert(message);
}

showMessage(); // Hello, John
```

The function has full access to the global scope. It can modify it as well.

```js
let userName = 'John';

function showMessage() {
  userName = 'Bob'; // (1) changed the outer variable

  let message = 'Hello, ' + userName;
  alert(message);
}

alert(userName); // John before the function call

showMessage();

alert(userName); // Bob, the value was modified by the function
```

**The outer variable is only used if there’s no local one.** If a same-named variable is declared inside the function then it shadows the outer one. For instance, in the code below the function uses the local userName. The outer one is ignored:

```js
let userName = 'John';

function showMessage() {
  let userName = 'Bob'; // declare a local variable

  let message = 'Hello, ' + userName; // Bob
  alert(message); // Hello Bob
}

// the function will create and use its own userName
showMessage();

alert(userName); // John, unchanged, the function did not access the outer variable
```
