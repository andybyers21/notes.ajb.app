---
layout: note
title: HTML Basics
parent: HTML
grand_parent: Home
---

# HTML Basics

ref: - Mozilla [HTML elements reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)

**Hypertext Markup Language** is a language for clients and servers to speak to each other to describes the content and structure of a webpage (but not the appearance). **The only way to control the content and structure of a web page is through HTML [[Anchor Tags]].** It is a document format used for defining the semantic structure of a single web page. _HTML is not a programming language, rather a markup language that defines the structure of your content._ The primary and essential function of any web browser is to render and display HTML.

A pair of tags and their content describe an HTML element, for example, a heading, a paragraph, or even a list of items.

An HTML element should be wrapped in tags eg:
`<tag> ELement statement goes here </tag>`
`<h1> Statements... </h1>`
Elements are wrapped in tags.

\*\*Add in something about HTML images and src tag.

## HTML Example

```html
<!DOCTYPE html>
<html>
  <head>
    <!-- "head" metadata goes here -->
    <title>Title of my page, that appears at the top of a browser window</title>
    <link rel="stylesheet" href="some-css.css" />
  </head>
  <body>
    <h1>Ruby Monstas HTML Example</h1>
    <p>One paragraph of text.</p>
    <p>Another paragraph of text, containing an emphasized <em>word</em>.</p>
    <h2>A list of items</h2>
    <ul>
      <li>First item</li>
      <li>Second item</li>
      <li>Third item</li>
    </ul>
  </body>
</html>
```

If you look at this document you’ll notice the recurring pattern of “tags” that start with `<something>` and then are closed with `</something>`. E.g. the entire document starts with an opening `<html>` tag, and ends with a closing `</html>` tag. (The **DOCTYPE** declaration is an instruction to tell the browser to render everything to HTML specification). The `<html>` element wraps your code like any other tag you might use.

`<link rel="stylesheet" href="some-css.css" />` - `link` inferrs that we want the html code to find a route to something. - `rel` is an attribute which specifies a relationship between documents.

HTML entirely consists of tags that have a certain meaning, can be nested, and contain content.^[By using tags such as these it also makes it easier for search engines like Google to apply weighting and relevance to different levels of the document (or ultimately your webpage).] If a word is contained in the `<head>`, the `<title>` and under top-level headlines (eg, `<h1>` then it’s probably important. Even more so, if other pages link to this document using link texts that also contain that word, then this adds social proof to the mix, and search results should probably list this page higher up in the results. - `<head>` contains the page metadata which is not displayed on the page in browser. Data such as `<title>`, `<date>`, and `<link>` (the URL you will visit to view this page). - `<body>` contains the content you wish to view on the page.

Another handy feature of this is that by inspecting the headline tags of an HTML document we can quickly and easily generate a table of contents for the document or site without an author having to manually update it every time they make a change. Many content management systems (CMS) do this, including, for example, Wikipedia.

`<!-- This is a comment in html, It won't appear on the web page. -->`

```html
<p>This text is inside a paragraph tag.</p>
<p>This is a second paragraph following the first.</p>
```

Note: The closing tag prefixes characters with a forward slash

The main parts of our element are as follows: - **The opening tag:** This consists of the name of the element (in this case, p), wrapped in opening and closing angle brackets. This states where the element begins or starts to take effect — in this case where the paragraph begins. - **The closing tag:** This is the same as the opening tag, except that it includes a forward slash before the element name. This states where the element ends — in this case where the paragraph ends. Failing to add a closing tag is one of the standard beginner errors and can lead to strange results. - **The content:** This is the content of the element, which in this case, is just text. - **The element:** The opening tag, the closing tag and the content together comprise the element.

---
