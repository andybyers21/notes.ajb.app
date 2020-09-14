---
layout: note
title: Function Scope and Conflicts
parent: JavaScript
nav_exclude: true
---

# Function Scope and Conflicts

When you create a function, the variables and various other items defined within that function are inside their own separate scope. They are locked away, untouchable by any of the code outside of that function. _The top level of your code, things that can be defined from anywhere in the code is called the **global scope**._ JavaScript is set up in this way for security and organization. Sometimes you won't want variables to be accessed from outside the scope, which could mess with your code. Or, importantly, by external scripts that will have access to your data from the global scope.

For example, say you have an HTML file that is calling in two external JavaScript files, and both of them have a variable and a function defined that use the same name:

```html
<!-- Excerpt from my HTML -->
<script src="first.js"></script>
<script src="second.js"></script>
<script>
  greeting();
</script>
```

```js
// first.js
let name = 'Chris';
function greeting() {
  alert('Hello ' + name + ': welcome to our company.');
}
```

```js
// second.js
let name = 'Zaptec';
function greeting() {
  alert('Our company is called ' + name + '.');
}
```

Both functions you want to call are called `greeting()`, but you can only ever access the first.js file's `greeting()` function (the second one is ignored). In addition, attempting to declare the name variable a second time with the let keyword in the second.js file results in an error. Keeping parts of your code locked away in functions avoids such problems, and is considered the best practice.
