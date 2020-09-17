---
layout: note
title: Attribute Selectors
parent: CSS
grand_parent: Home
---

# Attribute Selectors

CSS has the ability to target HTML elements based on any one of their attributes.

I believe the most common use of regular attribute selectors is on inputs. There are text, button, checkbox, file, hidden, image, password, radio, reset, and submit (did I miss any?). All of them are `<input>`’s, and all of them are very different. So doing something like input { padding: 10px; } is a bad idea most of the time. It’s very common to see things like:

```css
input[type='text'] {
  padding: 3px;
}
input[type='radio'] {
  float: left;
}
```

It’s really the only way to get your hands on certain types of inputs without screwing up the others and without adding extra markup.

_Note on Quotes:_ You can usually get away without using quotes in attribute selectors, like `[type=radio]`, but the rules for omitting quotes are weird and inconsistent across actual browser implementations. So, best practice, just use quotes, like `[type="radio"]`. It’s safer and always works.

This is where it starts getting more interesting. The equals sign in attribute selectors may be prefaced by other characters which alter the meaning a bit. For example, `*=` means “match the following value anywhere in the attribute value.” Look at this example:

```html
<h1 rel="xxxexternalxxx">Attribute Contains</h1>
```

```css
h1[rel*='external'] {
  color: red;
}
```

[More info at CSS-Tricks](https://css-tricks.com/attribute-selectors/)

---
