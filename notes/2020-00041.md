---
layout: note
title: CSS Basics
parent: CSS
grand_parent: Home
---

# CSS Basics

ref: - Mozilla [CSS reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#Keyword_index)

**Cascading Style Sheets** are applied to [[HTML]] to define how elements should look. CSS is embedded into the HTML code or can be referenced by link to an HTML page. The style sheet defines the appearance of a web page or app by defining rules and properties that an element must display. **These rules are defined by a selector**. Like HTML, CSS is also not a programming language. Nor is it a markup language (which HTML is). Rather it is a _style sheet language._

The benefit of having HTML and CSS sheets in a separate document is that while HTML will define the content of a web page you can apply any different style to it at your choosing. (For example depending on your users preference or device that they may be using).

For example:

```css
p {
  font-size: 24px;
  line-height: 1.4;
  margin-bottom: 20px;
}
```

- A CSS selector defines the target of a rule. The selector in this rule is `p`. That means the rule should apply to all paragraph `<p>` elements in the HTML document.
- **The whole structure is called a ruleset (or sometimes just rule). The rule itself should be inside curly braces `{ }`. **
- Each line of code is a **declaration** and should end with a semicolon `;`
- Declarations consist of **properties** and **values** that it should be set to. (eg, font size, line height etc.) For example `font-size` is a **property** of the HTML's `<p>` elements. The **value** of this is `24px`.
- A CSS rule could be defined to any element that matches a particular condition.
- Within each declaration, **you must use a colon (:) to separate the property from its value** or values.
- Within each ruleset, **you must use a semicolon (;) to separate each declaration from the next one.**

You can also select multiple elements as such

```css
p,
li,
h1 {
  color: red;
}
```

The CSS file will contain references to various elements of the HTML to apply styles to that element.

> In HTML a _class_ is an attribute that can be set on an elements [[Div Tags]]. For example `<p class='intro lead'>This is the intro text.</p>` would point to the rule `p` and also `p intro` and `p lead`. You can use anything you like as a class name and can use numerous class's

**CSS rules are always applied in order from least specific to most specific.** Meaning that `p` would take precedance over `p intro` which would take precedence over `p lead` which could target more specific elements.

## More selector types

Here are two more types of selector:

```css
ul,
ol {
  list-style: none;
}

ul li {
  margin-bottom: 10px;
}
```

In a selector, a comma acts like the word ‘or’. The code `ul`, `ol` applies this rule to any `ul` or `ol` elements. This is useful for applying similar properties to many elements at once. A space describes nesting. The code `ul li` targets all `li` elements inside `ul` elements. This rule would affect list items, `li` inside unordered lists, `ul`, but not list items inside ordered lists `ol`. This type of rule is useful for targeting specific elements.

The examples above use element selectors, which select all elements of a given type. But we can make more specific selections as well such as [[Attributes]] and class selectors. There are many more selectors to discover. To learn more, see the [MDN Selectors guide](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors).

`/* This is a comment in CSS.`^[Use `<!-- comment -->` when working in an HTML sheet

## CSS is all about the boxes

Something you'll notice about writing CSS: a lot of it is about boxes. This includes setting size, color, and position. Most HTML elements on your page can be thought of as boxes sitting on top of other boxes. CSS layout is mostly based on the box model. Each box taking up space on your page has properties like:

- **padding**, the space around the content. In the example below, it is the space around the paragraph text.
- **border**, the solid line that is just outside the padding.
- **margin**, the space around the outside of the border.

![box-model.png](./attachments/box-model.png)

---
