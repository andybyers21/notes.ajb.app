---
layout: note
title: Div Tags
parent: HTML
nav_exclude: true
---

# Div Tags

Tags can contain tags and this is how pages are put together. The `<div>` tag defines a division or a section in an HTML document. It is used as a container for HTML elements:

```html
<div id="intro">
  <h1>Welcome to the site</h1>
  <div class="image-wrapper">
    <img class="image-large" src="team.jpg" />
  </div>
  <p>
    Welcome to our website. You can see the team above, and
    <a href="/team">find out more about them here.</a>
  </p>
</div>
```

Lines of code can be indented to make it more astetic and readable by a coder but the browser cares not and ignores multiple spaces. _Clear code is easier to debug and edit_

**_[[HTML]] and [[CSS]] describe the content and appearance of a page, as well as links to other resources._**
