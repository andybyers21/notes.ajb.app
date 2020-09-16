---
layout: note
title: Variables in the Real World
parent: JavaScript
grand_parent: Home
---

# Variables in the Real World

The easiest way to visualize a variable is as a box with data inside and a sticker on the outside. For instance, the variable "message" can be imagined as a box labeled "message" with the value "Hello!" in it. YOu can put whatever value you like in a box and also change it out later in the code when required.

```js
let message;

message = 'Hello!';

message = 'World!'; // value changed

alert(message);
```

When the value is changed, the old data is tossed out in favor of the new.

We can also copy data from one box (variable) into another:

```js
let hello = 'Hello world!';

let message;

// copy 'Hello world' from hello into message
message = hello;

// now two variables hold the same data
alert(hello); // Hello world!
alert(message); // Hello world!
```

However, declaring a variable twice will trigger an error.

```js
let message = 'This';

// repeated 'let' leads to an error
let message = 'That'; // SyntaxError: 'message' has already been declared
```

So we should declare a variable only once then call it by name without the `let`.

There are only two limitations to variable naming in JavaScript:

1. The name must contain either letters, numbers or the symbols `$` or `_`. No other symbols are allowed in the naming scheme.
2. The name cannot start with a number. (However any other character can be a number).

When the name contains multiple words, camelCase is commonly used. That is: words go one after another, each word except first starting with a capital letter: `myVeryLongName`. There is a list of [reserved words](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Keywords), which cannot be used as variable names because they are used by the language itself, names such as `let`, `class`, `return`, and `function` will return a syntax error.

A variable should always be named before using it. (Although it is technically possible to create a variable by by assignment only it's not good problems and will probably cause you an issue down the road).

---
