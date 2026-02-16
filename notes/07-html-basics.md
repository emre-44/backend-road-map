# HTML (Hypertext Markup Language)

HTML is a markup language for creating web pages. **NOT** a programming language.

## Basic HTML Structure
```html
<!doctype html>
<html>
    <head>
        <title>Page Title</title>
    </head>
    <body>
        Visible content goes here
    </body>
</html>
```

## Common Tags

**Headings and Text**

```html
<h1> to <h6>: Headings (h1 most important, h6 least)

<p>: Paragraph

<!-- comment -->: HTML comment
```
**Links**
```html
<a href="url">Link text</a>: Creates a hyperlink
```
**Lists**
```html
<ul>           <!-- Unordered (bulleted) list -->
    <li>Item 1</li>
    <li>Item 2</li>
</ul>

<ol>           <!-- Ordered (numbered) list -->
    <li>First</li>
    <li>Second</li>
</ol>
```

**Images**
```html
<img src="image.jpg" alt="description">: Embeds an image

src: Image source (URL or file path)

alt: Alternative text for accessibility
```

**Tables**
```html
<table>
    <tr>        <!-- Table row -->
        <th>Header 1</th>  <!-- Table header -->
        <th>Header 2</th>
    </tr>
    <tr>
        <td>Row 1, Cell 1</td>  <!-- Table data/cell -->
        <td>Row 1, Cell 2</td>
    </tr>
</table>
```

## Document Structure
```html
<!doctype html>: Declares HTML5 document

<html>: Root element

<head>: Container for metadata

<body>: Container for visible content

<main>: Main content of the document (unique)

<div>: Block-level container/division

<span>: Inline container
```
**Metadata**
```html
<title>: Document title (browser tab)

<meta>: Metadata like charset, description, keywords

<link>: Links external resources (CSS, favicon)

<style>: Internal CSS styles

<base>: Base URL for relative links
```

**Text Formatting**
```html
<strong>: Important/bold text

<em>: Emphasized/italic text

<mark>: Highlighted text

<small>: Smaller text

<del>: Deleted text (strikethrough)

<ins>: Inserted text (underline)

<sub>: Subscript

<sup>: Superscript

<br>: Line break

<hr>: Horizontal rule

<blockquote>: Block-level quotation

<q>: Inline quotation

<abbr>: Abbreviation

<address>: Contact information

<cite>: Citation

<code>: Code snippet

<pre>: Preformatted text
```
**Semantic/Structural Tags**
```html
<header>: Introductory content

<footer>: Footer for section/page

<nav>: Navigation links

<section>: Thematic section

<article>: Self-contained content

<aside>: Sidebar content

<figure>: Self-contained content (images, diagrams)

<figcaption>: Caption for <figure>
```
**Forms**
```html
<form>: Input form container

<input>: Input field (text, password, checkbox, radio, etc.)

<textarea>: Multi-line text input

<button>: Clickable button

<select>: Dropdown list

<option>: Option in dropdown

<label>: Label for form element

<fieldset>: Groups related form elements

<legend>: Caption for <fieldset>

<datalist>: Autocomplete options

<output>: Calculation result
```
**Media**
```html
<img>: Image

<audio>: Audio content

<video>: Video content

<source>: Media source for <audio>/<video>

<track>: Subtitles/captions

<iframe>: Inline frame (embed another page)

<embed>: External application/plugin

<object>: Embedded object

<param>: Parameters for <object>

<picture>: Responsive images

<canvas>: Drawing graphics via JavaScript

<svg>: Scalable Vector Graphics
```
**Lists**
```html
<ul>: Unordered list

<ol>: Ordered list

<li>: List item

<dl>: Description list

<dt>: Term in description list

<dd>: Description of term
```
**Tables**
```html
<table>: Table container

<caption>: Table caption

<thead>: Table header section

<tbody>: Table body section

<tfoot>: Table footer section

<tr>: Table row

<th>: Table header cell

<td>: Table data cell

<col>: Column properties

<colgroup>: Group of columns
```
**Interactive**
```html
<details>: Expandable details

<summary>: Visible heading for <details>

<dialog>: Dialog box/modal

<menu>: Menu/toolbar

```
**Scripting**
```html
<script>: JavaScript code

<noscript>: Content for non-JavaScript browsers

<template>: HTML template (cloned via JavaScript)

<slot>: Shadow DOM slot
```

**Global Attributes (work on all tags)**
```html
id: Unique identifier

class: CSS class name(s)

style: Inline CSS

title: Tooltip text

lang: Language

dir: Text direction (ltr/rtl)

tabindex: Tab order

hidden: Hide element

data-*: Custom data attributes
    ```