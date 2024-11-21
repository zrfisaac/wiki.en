# CSS

This guide provides essential information about using CSS (Cascading Style Sheets) for web development, covering basic concepts, syntax, styling properties, and common practices. CSS is used to control the look and layout of a website, allowing you to style elements such as text, colors, and layouts, as well as position elements on a page.

## Table of Contents

- [Introduction to CSS](#introduction-to-css)
  Overview of CSS and its main features.
  
- [Setting Up CSS](#setting-up-css)
  Instructions for how to set up and use CSS in your project.
  
- [CSS Syntax](#css-syntax)
  Understanding the syntax and structure of CSS rules.
  
- [Common CSS Properties](#common-css-properties)
  Overview of commonly used CSS properties and how to apply them.
  
- [CSS Selectors](#css-selectors)
  How to target HTML elements using selectors.
  
- [CSS Layout Techniques](#css-layout-techniques)
  Techniques for controlling layouts using CSS.
  
- [Responsive Design with CSS](#responsive-design-with-css)
  How to create responsive web designs using media queries.

---

## Introduction to CSS

CSS (Cascading Style Sheets) is used to define the visual presentation of a document written in HTML or XML. It allows you to apply styles like fonts, colors, spacing, and layout, giving you complete control over how elements appear on the screen.

Key features of CSS:
- **Separation of content and style**: CSS separates the structure (HTML) from the style (CSS), making websites easier to maintain.
- **Cascading nature**: Styles can be applied in layers, allowing for overriding rules and easier customization.
- **Styling flexibility**: You can style text, backgrounds, borders, and much more.

---

## Setting Up CSS

There are three common ways to include CSS in your HTML documents: inline, internal, and external.

### Inline CSS
Inline CSS is applied directly within an HTML element using the `style` attribute.

```html
<p style="color: blue; font-size: 16px;">This is a blue paragraph.</p>
```

### Internal CSS
Internal CSS is placed inside a `<style>` tag within the `<head>` section of your HTML document.

```html
<head>
  <style>
    body {
      background-color: lightgray;
    }
  </style>
</head>
```

### External CSS
External CSS is defined in a separate `.css` file, which is linked to your HTML document. This is the most efficient way to style larger websites.

```html
<head>
  <link rel="stylesheet" type="text/css" href="styles.css">
</head>
```

---

## CSS Syntax

CSS uses a simple syntax to define style rules. A rule consists of a **selector** and a **declaration block**.

### Basic Syntax

```css
selector {
  property: value;
}
```

- **Selector**: Targets the HTML element you want to style.
- **Property**: The style you want to apply (e.g., `color`, `font-size`).
- **Value**: The value for the property (e.g., `blue`, `16px`).

Example:

```css
h1 {
  color: blue;
  font-size: 24px;
}
```

This rule changes the color of `<h1>` elements to blue and sets the font size to 24 pixels.

---

## Common CSS Properties

Here are some common CSS properties that are used frequently in web development:

### Text Properties
- **`color`**: Specifies the text color.
  ```css
  p {
    color: #333;
  }
  ```

- **`font-size`**: Sets the font size of text.
  ```css
  p {
    font-size: 16px;
  }
  ```

- **`font-family`**: Specifies the font for the text.
  ```css
  body {
    font-family: Arial, sans-serif;
  }
  ```

### Box Model Properties
- **`margin`**: Creates space outside the element.
  ```css
  div {
    margin: 10px;
  }
  ```

- **`padding`**: Creates space inside the element.
  ```css
  div {
    padding: 10px;
  }
  ```

- **`border`**: Adds a border around the element.
  ```css
  div {
    border: 1px solid black;
  }
  ```

### Background Properties
- **`background-color`**: Sets the background color of an element.
  ```css
  body {
    background-color: #f0f0f0;
  }
  ```

- **`background-image`**: Sets an image as the background.
  ```css
  body {
    background-image: url('background.jpg');
  }
  ```

---

## CSS Selectors

Selectors are used to target HTML elements and apply styles. There are various types of selectors in CSS.

### Basic Selectors
- **Universal selector (`*`)**: Selects all elements.
  ```css
  * {
    margin: 0;
    padding: 0;
  }
  ```

- **Element selector (`p`, `h1`, etc.)**: Selects all elements of a given type.
  ```css
  p {
    font-size: 14px;
  }
  ```

- **Class selector (`.class-name`)**: Selects elements with a specific class.
  ```css
  .highlight {
    background-color: yellow;
  }
  ```

- **ID selector (`#id-name`)**: Selects an element with a specific ID.
  ```css
  #main-header {
    color: red;
  }
  ```

### Grouping Selectors
You can group multiple selectors to apply the same styles to different elements.

```css
h1, h2, h3 {
  font-family: 'Arial', sans-serif;
}
```

---

## CSS Layout Techniques

CSS provides various methods for creating layouts, including Flexbox and CSS Grid.

### Flexbox
Flexbox is a one-dimensional layout system that allows for easy alignment of items in a row or column.

```css
.container {
  display: flex;
  justify-content: space-between;
}

.item {
  flex: 1;
}
```

### CSS Grid
CSS Grid is a two-dimensional layout system that provides greater control over both rows and columns.

```css
.container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
}

.item {
  grid-column: span 2;
}
```

---

## Responsive Design with CSS

Responsive design ensures that a website works well on different screen sizes and devices. CSS media queries allow you to apply styles based on the screen width, device type, or orientation.

### Example Media Query

```css
@media (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```

This rule applies the light blue background color when the screen width is 600px or less.

---

## Resources

- [MDN Web Docs - CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [W3Schools - CSS Tutorial](https://www.w3schools.com/css/)
- [CSS-Tricks](https://css-tricks.com/)
