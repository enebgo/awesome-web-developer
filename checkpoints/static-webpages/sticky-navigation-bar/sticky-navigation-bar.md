
# Sticky Navigation Bar

## Key Concepts:
### Block-Level Elements
- `display: block` is used to make `<a>` inside the nav bar behave like block-level elements. 
  - Allows the entire area of the link to be clickable. 
  - Enables setting width and height on the links
- `text-align: center` As the anchor is now a block-level element, the block nature creates a container in which the text can be aligned.
  - Applies to inline content inside the block.
  - Centers the text **horizontally** within the block-level anchor.

### Flexbox Layout
- `display: flex` is used on the `<ul>` to create a flexible container.
  - Allows the child elements (list items) to be laid out in a flexible row.
- `flex-grow: 1` is used to make the list items grow to fill the available space.
  - Distributes the available space equally among the list items.
  - Makes the list items take up the full width of the container.

### Sticky Positioning
- `position: sticky` is used to make the navigation bar stick to the top of the viewport.
  - The element is treated as relative positioned until it crosses a specified threshold, then it is treated as fixed positioned.

### Sticking Position
- `top: 0` is used to specify the position where the element should stick.
  - 0 means it will stick to the very top of its containing block.

### Stacking Order
- `z-index: 100` is used to determine the stacking order of elements.
  - A higher value (like 100) ensures this element appears on top of other elements with lower z-index values.

### Pseudo-Class
- `:hover` is a pseudo-class that applies styles when the mouse hovers over an element.
  - Used to create a hover effect on the navigation links.

## Steps to Create a Sticky Navigation Bar

### Step 1: HTML Structure
Create an HTML file named `index.html` with the following content:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sticky Navigation Bar</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <nav id="sticky-nav">
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
    
    <main>
        <!-- Your page content goes here -->
    </main>
</body>
</html>
```

### Step 2: Create CSS File
Create a file named `styles.css` in the same directory as your HTML file.

### Step 3: Basic CSS Setup

```css
body {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
}
```

Explanation:
- `margin: 0;`: This property sets the outer spacing of the element. A value of 0 removes any default margin around the body.
- `padding: 0;`: This property sets the inner spacing of the element. A value of 0 removes any default padding inside the body.
- `font-family: Arial, sans-serif;`: This sets the typeface for text. It specifies Arial as the first choice, falling back to any sans-serif font if Arial is unavailable.

### * Step 4: Style the Navigation Container

```css
#sticky-nav {
    background-color: #333;
    position: sticky;
    top: 0;
    z-index: 100;
}
```

Explanation:
- `background-color: #333;`: This sets the background color of the element. #333 is a dark gray color in hexadecimal notation.
- `position: sticky;`: This is a positioning method where the element is treated as relative positioned until it crosses a specified threshold, then it is treated as fixed positioned.
- `top: 0;`: This specifies the position where the element should stick. 0 means it will stick to the very top of its containing block.
- `z-index: 100;`: This determines the stacking order of elements. A higher value (like 100) ensures this element appears on top of other elements with lower z-index values.

### Step 5: Style the Navigation List

```css
#sticky-nav ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    display: flex;
}
```

Explanation:
- `list-style-type: none;`: This removes the default bullet points from the list items.
- `margin: 0;` and `padding: 0;`: These remove any default spacing around and within the list.
- `display: flex;`: This enables flexbox layout. It allows the child elements (list items) to be laid out in a flexible row.

### Step 6: Style Navigation Links

```css
#sticky-nav li a {
    display: block;
    color: white;
    text-align: center;
    padding: 14px 16px;
    text-decoration: none;
}
```

Explanation:
- `display: block;`: This makes the anchor tags behave like block-level elements, allowing them to have dimensions.
- `color: white;`: This sets the text color to white.
- `text-align: center;`: This centers the text within each link.
- `padding: 14px 16px;`: This adds space inside each link. 14px on top and bottom, 16px on left and right.
- `text-decoration: none;`: This removes the default underline from links.

### Step 7: Add Hover Effect

```css
#sticky-nav li a:hover {
    background-color: #111;
}
```

Explanation:
- `:hover`: This is a pseudo-class that applies styles when the mouse hovers over an element.
- `background-color: #111;`: This changes the background color to a darker shade (#111 is nearly black) when the link is hovered over.
