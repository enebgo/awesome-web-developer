---
sidebar_position: 2
---

# HTML Syntax and Structure

## Fundamentals: Tags, Attributes, and Elements

HTML (Hypertext Markup Language) is built on three core concepts: **tags**, **attributes**, and **elements**.

### Tags

Tags are markup codes that define the structure and purpose of content in an HTML document.

- Enclosed in angle brackets: `< >`
- Usually come in pairs: opening tag and closing tag
- Closing tags include a forward slash: `</>`

Examples:
- Opening tag: `<p>`
- Closing tag: `</p>`
- Self-closing tag: `<img>` or `<br>`
- Syntax: `<tagname>content</tagname>`

### Attributes

Attributes provide additional information about HTML elements.

- Specified in the opening tag
- Syntax: Come in name/value pairs: `name="value"`
- Common attributes (id, class, style)
- Boolean attributes

Example:
```html
<img src="image.jpg" alt="A beautiful landscape">
```
Here, `src` and `alt` are attributes of the `<img>` tag.

### Elements

An element is the complete unit of content in an HTML document.

Components of an element:
- Opening tag
- Attributes (if any)
- Content
- Closing tag

Example:
```html
<p class="intro">This is a paragraph.</p>
```

## Block and Inline Elements

In HTML, elements are typically classified into two main categories: block-level elements and inline elements. Understanding the difference between these two types is crucial for proper page layout and styling.

### Block-level Elements

Block-level elements have the following characteristics:

- Start on a new line
- Take up the full width available by default
- Have a top and bottom margin

Common block-level elements include:

- `<div>`
- `<p>`
- `<h1>` to `<h6>`
- `<ul>` and `<ol>`
- `<section>`
- `<article>`

Example:
```html
<p>This is a paragraph.</p>
<div>This is a div element.</div>
```

### Inline Elements

Inline elements have the following characteristics:

- Do not start on a new line
- Only take up as much width as necessary
- Do not have top and bottom margins

Common inline elements include:

- `<span>`
- `<a>`
- `<strong>`
- `<em>`
- `<img>`
- `<br>`
- `<input>`

Example:
```html
<p>This is a <span style="color: red;">red</span> word in a paragraph.</p>
```

> **Note**:
>
> All block-level elements have an opening and closing tags. As a result, self-enclosing elements are inline elements. (eg. `<input>`, `<img>`, `<br>`)
>
> Exceptions to the block/inline elements: list items for the `<li>`, table, table rows, table cells for `<table>`, `<tr>` and `<td>` respectively

### Changing Display Behavior

You can change how an element behaves using CSS. The `display` property can be used to make a block-level element behave like an inline element, or vice versa:

```css
/* Make a div behave like an inline element */
div {
    display: inline;
}

/* Make a span behave like a block-level element */
span {
    display: block;
}
```

### Inline-Block

There's also a hybrid display value called `inline-block`. Elements with this display value:

- Flow with the text (like inline elements)
- Can have width and height set (like block elements)

```css
.inline-block-example {
    display: inline-block;
    width: 100px;
    height: 100px;
}
```

## HTML Structure Hierarchy

### Concepts of Relationships between Elements

```html
<div id="parent">
  <h1>Welcome to <span class="highlight">Our Website</span></h1>
  <p>We have <strong>amazing</strong> content for <em>you</em>.</p>
  <ul>
    <li>Item <a href="#">One</a></li>
    <li>Item <span style="color: red;">Two</span></li>
  </ul>
</div>
```

Now, let's explain the relationships and nesting:

1. **Block-level elements**:
    - `<div>`, `<h1>`, `<p>`, `<ul>`, and `<li>` are block-level elements.

2. **Inline elements**:
    - `<span>`, `<strong>`, `<em>`, and `<a>` are inline elements.

3. **Nesting**:
    - Inline elements (`<span>`) are nested within the block-level `<h1>`.
    - Multiple inline elements (`<strong>` and `<em>`) are nested within the `<p>`.
    - Inline elements (`<a>` and `<span>`) are nested within block-level `<li>` elements.

4. **Parent-Child relationships**:
    - The `<div>` is a parent to `<h1>`, `<p>`, and `<ul>`.
    - The `<h1>` is a parent to the nested `<span>`.
    - The `<p>` is a parent to the nested `<strong>` and `<em>`.
    - Each `<li>` is a parent to its nested inline element (`<a>` or `<span>`).

5. **Siblings**:
    - The `<h1>`, `<p>` and `<ul>` are siblings within the `<div>`.
    - The inline `<strong>` and `<em>` within the `<p>` are siblings.

6. **Ancestors and Descendants**:
    - The `<div>` is an ancestor to all nested elements, including both block-level and inline elements.
    - All elements within the `<div>` are descendants of the `<div>`, regardless of whether they are block-level or inline.

## Basic HTML Structure

Every HTML document follows a standard structure. Let's break down the essential components of an HTML document.

### 1. DOCTYPE Declaration

Every HTML5 document starts with a DOCTYPE declaration. This tells the browser that this is an HTML5 document.

```html
<!DOCTYPE html>
```

- It's not case-sensitive, but it's common practice to write it in uppercase.
- Unlike in older HTML versions, this declaration is simple and doesn't require a reference to a DTD (Document Type Definition).

### 2. HTML Root Element

The `<html>` element is the root element of an HTML page. All other elements must be descendants of this element.

```html
<html lang="en">
  <!-- Other elements go here -->
</html>
```

- The `lang` attribute specifies the language of the document. It's important for accessibility and search engines.

### 3. Head Section

The `<head>` element contains meta information about the HTML page.

```html
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Page Title</title>
</head>
```

Key elements within the `<head>`:

- `<meta charset="UTF-8">`: Specifies the character encoding for the document (typically UTF-8).
- `<meta name="viewport">`: Ensures proper rendering on mobile devices.
- `<title>`: Specifies a title for the page, which is shown in the browser's title bar or page's tab.

Other common elements in the `<head>`:
- `<link>`: to link to external stylesheets
- `<script>`: to include JavaScript files or code
- `<style>`: to include internal CSS

### 4. Body Section

The `<body>` element defines the document's body. It contains all the visible contents, such as headings, paragraphs, images, hyperlinks, tables, lists, etc.

```html
<body>
  <h1>This is a Heading</h1>
  <p>This is a paragraph.</p>
  <!-- More content goes here -->
</body>
```

### 5. Putting It All Together

Here's an example of a basic HTML5 document structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First HTML Page</title>
</head>
<body>
    <h1>Welcome to My Website</h1>
    <p>This is a paragraph on my web page.</p>
</body>
</html>
```

This structure provides the foundation upon which you'll build more complex web pages and applications. As you progress, you'll add more elements within this basic structure, but the core components outlined here will remain consistent across most HTML documents you create.
