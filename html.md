# HTML

This guide provides essential information about using HTML in web development, covering basic elements, structure, attributes, and common practices. HTML (Hypertext Markup Language) is the standard language used to create web pages. It provides the basic structure of web documents, including headings, paragraphs, links, images, and forms.

## Index

- [Introduction to HTML](#introduction-to-html)
  Overview of HTML and its key features.
  
- [Setting Up HTML](#setting-up-html)
  Instructions on how to set up and create an HTML file.
  
- [HTML Structure](#html-structure)
  Learn about the structure of an HTML document.
  
- [HTML Elements](#html-elements)
  Overview of common HTML elements and their usage.
  
- [HTML Attributes](#html-attributes)
  How to use attributes in HTML elements.
  
- [Working with Forms](#working-with-forms)
  How to create and handle forms in HTML.
  
- [Common Use Cases for HTML](#common-use-cases-for-html)
  Practical examples of how HTML is used.

---

## Introduction to HTML

HTML (Hypertext Markup Language) is the fundamental language for creating web pages and web applications. It defines the structure and layout of web content and is the building block of all websites.

Key features of HTML:
- **Document Structure**: Defines the organization of web content.
- **Semantics**: Uses tags to define the meaning of content (e.g., headings, paragraphs, lists).
- **Accessibility**: Helps ensure web content is accessible to all users, including those with disabilities.
- **Hyperlinks**: Allows linking between pages, documents, and resources.

---

## Setting Up HTML

To get started with HTML, you need to create an HTML file with the `.html` extension. This file will contain your HTML content.

### Basic HTML Document

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
  <p>This is a simple HTML page.</p>
</body>
</html>
```

---

## HTML Structure

An HTML document is made up of several key sections. These sections provide the framework for a webpage.

### The `<!DOCTYPE html>` Declaration

This declaration defines the document type and version of HTML (in this case, HTML5).

```html
<!DOCTYPE html>
```

### The `<html>` Element

The `<html>` element is the root of the HTML document and contains all other HTML elements.

```html
<html lang="en">
  <!-- Content goes here -->
</html>
```

### The `<head>` Element

The `<head>` element contains metadata about the document, including the title, character encoding, and links to external resources like stylesheets or scripts.

```html
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document Title</title>
</head>
```

### The `<body>` Element

The `<body>` element contains the visible content of the web page, such as text, images, and links.

```html
<body>
  <h1>Title of the Page</h1>
  <p>Content of the page.</p>
</body>
```

---

## HTML Elements

HTML elements are the building blocks of a webpage. They are defined by tags and usually come in pairs: a start tag and an end tag.

### Common HTML Elements

- **Headings**: `<h1>` to `<h6>` tags represent headings of different levels.
  ```html
  <h1>This is a Heading Level 1</h1>
  <h2>This is a Heading Level 2</h2>
  ```

- **Paragraphs**: The `<p>` tag is used for paragraphs.
  ```html
  <p>This is a paragraph of text.</p>
  ```

- **Links**: The `<a>` tag defines a hyperlink.
  ```html
  <a href="https://example.com">Visit Example</a>
  ```

- **Images**: The `<img>` tag is used to embed images.
  ```html
  <img src="image.jpg" alt="Description of image">
  ```

- **Lists**: Unordered lists use `<ul>` and ordered lists use `<ol>`.
  ```html
  <ul>
    <li>Item 1</li>
    <li>Item 2</li>
  </ul>

  <ol>
    <li>First item</li>
    <li>Second item</li>
  </ol>
  ```

---

## HTML Attributes

Attributes provide additional information about HTML elements and are added to the opening tag of an element.

### Common Attributes

- **`href`**: Specifies the URL in the `<a>` tag.
  ```html
  <a href="https://www.example.com">Go to Example</a>
  ```

- **`src`**: Specifies the source of an image in the `<img>` tag.
  ```html
  <img src="image.jpg" alt="Example Image">
  ```

- **`alt`**: Provides an alternative text description for images.
  ```html
  <img src="image.jpg" alt="A beautiful landscape">
  ```

- **`id`**: Uniquely identifies an element in the document.
  ```html
  <div id="uniqueElement">Content</div>
  ```

- **`class`**: Specifies a class name for styling or targeting by JavaScript.
  ```html
  <p class="highlight">Highlighted Text</p>
  ```

---

## Working with Forms

Forms are used to collect user input, such as text, selections, and buttons.

### Basic Form Structure

```html
<form action="/submit" method="POST">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name">
  
  <label for="email">Email:</label>
  <input type="email" id="email" name="email">
  
  <input type="submit" value="Submit">
</form>
```

### Form Elements

- **Text Input**: `<input type="text">`
- **Password Input**: `<input type="password">`
- **Submit Button**: `<input type="submit">`
- **Checkbox**: `<input type="checkbox">`
- **Radio Button**: `<input type="radio">`

---

## Common Use Cases for HTML

HTML is used for a wide variety of purposes in web development. Here are some common use cases:

- **Building Web Pages**: Structure content like text, images, links, and more.
- **Forms**: Collect user input via forms for sign-ups, surveys, and logins.
- **Embedding Multimedia**: Embed videos, audio, and other media types using tags like `<video>` and `<audio>`.
- **Building Navigation**: Create navigation menus and links to different sections of a website or external sites.

---

## Additional Resources

- [MDN Web Docs - HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [W3Schools - HTML Tutorial](https://www.w3schools.com/html/)
- [HTML.com](https://html.com/)

