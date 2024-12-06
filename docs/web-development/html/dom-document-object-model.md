---
sidebar_position: 3
---

# DOM (Document Object Model)

The **Document Object Model (DOM)** is a programming interface for HTML and XML documents. It represents the structure of a document as a tree-like hierarchy of objects, allowing programs to dynamically access and manipulate the content, structure, and style of web documents.

## Basic Concepts

### 1. Node

A Node is the most basic unit in the DOM tree. Every object in the DOM hierarchy is a type of Node. Nodes can represent elements, text, comments, or other parts of the document. The Node interface provides properties and methods that are inherited by more specific node types.

### 2. Element

An Element is a specific type of Node that represents an HTML or XML element in the document. Elements can have attributes, child nodes, and can be manipulated using various DOM methods. Examples of elements include `<div>`, `<p>`, and `<a>` tags.

### 3. Document

The Document object represents the entire HTML or XML document. It serves as the root of the DOM tree and provides methods to access and manipulate the document's content, structure, and styles. The document object is the entry point for working with the DOM.

### 4. Window

The Window object represents the browser window or tab. It is the global object in client-side JavaScript and contains properties and methods for controlling the browser window, managing the document, and interacting with the user. The window object is the top-level object in the browser's JavaScript hierarchy.

## Key Characteristics

1. **Hierarchical Structure**: Represents documents as a tree of `Nodes`.
2. **Language-Independent**: Can be used with any programming language.
3. **Platform-Independent**: Works across different operating systems and devices.
4. **Dynamic**: Allows real-time updates to document content and structure.

## Accessing DOM Elements

- `getElementById()`: Finds an element by its ID.
- `getElementsByClassName()`: Returns a collection of elements with a specific class.
- `getElementsByTagName()`: Returns a collection of elements with a specific tag name.
- `querySelector()`: Returns the first element that matches a CSS selector.
- `querySelectorAll()`: Returns all elements that match a CSS selector.

## DOM Manipulation

- **Creating Elements**: `document.createElement()`
- **Modifying Elements**:
    - Changing content: `element.textContent`, `element.innerHTML`
    - Modifying attributes: `element.setAttribute()`, `element.removeAttribute()`
- **Adding/Removing Elements**:
    - `element.appendChild()`, `element.removeChild()`, `element.replaceChild()`
- **Changing Style**:
    - `element.style.color = 'red';`, `element.style.fontSize = '16px';`
- **Adding/Removing Classes**:
    - `element.classList.add('newClass');`, `element.classList.remove('oldClass');`

## Traversing the DOM

- **Parent Node**: `element.parentNode;`
- **Child Node**: `element.childNodes;`
- **Sibling Nodes**:
    - `element.nextSibling;`
    - `element.previousSibling;`

## Event Handling

The DOM allows attaching event listeners to elements:
```javascript
element.addEventListener('click', function() {
    // Event handler code
});
```

## DOM API Examples
```javascript
// Selecting an element
let header = document.getElementById('main-header');

// Modifying content
header.textContent = 'New Header Text';

// Creating and appending a new element
let newParagraph = document.createElement('p');
newParagraph.textContent = 'This is a new paragraph.';
document.body.appendChild(newParagraph);

// Adding an event listener
header.addEventListener('click', function() {
    alert('Header was clicked!');
});
```
