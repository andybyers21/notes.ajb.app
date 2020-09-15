---
layout: note
title: Function Parameters
parent: JavaScript
nav_exclude: true
---

# Function Parameters

Some functions require parameters to be specified when you are invoking them — these are values that need to be included inside the function parentheses, which it needs to do its job properly. _Note: Parameters are sometimes called arguments, properties, or even attributes._

The browser's built-in `string.replace()` function however needs two parameters — the substring to find in the main string, and the substring to replace that string with:

```javascript
let myText = 'I am a string';
let newString = myText.replace('string', 'sausage');
```

_Note: When you need to specify multiple parameters, they are separated by commas._ It should also be noted that sometimes parameters are optional — you don't have to specify them. If you don't, the function will generally adopt some kind of default behavior. As an example, the array `join()` function's parameter is optional:

```javascript
let myArray = ['I', 'love', 'chocolate', 'frogs'];
let madeAString = myArray.join(' ');
// returns 'I love chocolate frogs'
let madeAString = myArray.join();
// returns 'I,love,chocolate,frogs'
```

If no parameter is included to specify a joining/delimiting character, a comma is used by default.

In the example below, the function has two parameters: from and text.

```javascript
function showMessage(from, text) {
  // arguments: from, text
  alert(from + ': ' + text);
}

showMessage('Ann', 'Hello!'); // Ann: Hello! (*)
showMessage('Ann', "What's up?"); // Ann: What's up? (**)
```

When the function is called the given values are copied to local variables from and text. Then the function uses them.

Here’s one more example: we have a variable from and pass it to the function. Please note: the function changes from, but the change is not seen outside, because a function always gets a copy of the value:

```javascript
function showMessage(from, text) {
  from = '*' + from + '*'; // make "from" look nicer

  alert(from + ': ' + text);
}

let from = 'Ann';

showMessage(from, 'Hello'); // *Ann*: Hello

// the value of "from" is the same, the function modified a local copy
alert(from); // Ann
```
