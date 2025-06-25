# HTML Summary

This document provides a comprehensive summary of the HTML concepts, tags, elements, and attributes covered in this learning project.

## 1. Introduction to HTML

**HTML (HyperText Markup Language)** is the standard language for creating web pages. It describes the structure of a web page using a system of **tags** and **elements**.

-   **Tags**: These are the building blocks of HTML. They are keywords surrounded by angle brackets, like `<html>`. Tags usually come in pairs, like `<p>` and `</p>`, marking the beginning and end of an element.
-   **Elements**: An HTML element is everything from the start tag to the end tag, including the content in between. For example, `<p>This is a paragraph.</p>` is a paragraph element.
-   **Attributes**: Attributes provide additional information about an element and are always specified in the start tag. They usually come in name/value pairs like `name="value"`. For example, in `<a href="https://www.google.com">`, `href` is an attribute.

## 2. Basic HTML Document Structure

Every HTML document has a basic structure that includes the following elements:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Page Title</title>
</head>
<body>

    <h1>My First Heading</h1>
    <p>My first paragraph.</p>

</body>
</html>
```

-   `<!DOCTYPE html>`: Declares that this document is an HTML5 document.
-   `<html>`: The root element of an HTML page.
-   `<head>`: Contains meta-information about the document, such as its title.
-   `<title>`: Specifies a title for the document, which is shown in the browser's title bar or in the page's tab.
-   `<body>`: Contains the visible page content.

---

## 3. HTML Tags, Elements, and Attributes

### Headings

Headings are used to define the titles or subtitles on a webpage.

-   **Tags**: `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`
-   **Usage**: `<h1>` defines the most important heading, while `<h6>` defines the least important.
-   **Example**:
    ```html
    <h1>This is a Main Heading</h1>
    <h2>This is a Sub-heading</h2>
    ```

### Paragraphs

Paragraphs are used to structure text content.

-   **Tag**: `<p>`
-   **Usage**: Wraps blocks of text. Browsers automatically add some space (a margin) before and after each `<p>` element.
-   **Example**:
    ```html
    <p>This is a paragraph of text.</p>
    <p>This is another paragraph.</p>
    ```

### Text Formatting

HTML provides several elements for defining text with a special meaning.

-   `<b>` and `<strong>`: Both make text bold. `<strong>` indicates that the text is important.
-   `<i>` and `<em>`: Both make text italic. `<em>` emphasizes the text.
-   `<u>` and `<ins>`: Both underline text. `<ins>` is used to indicate inserted text.
-   `<mark>`: Highlights text.
-   `<small>`: Makes text smaller.
-   `<del>`: Renders text with a line through it (strikethrough), indicating deleted text.
-   `<sub>`: Defines subscripted text (appears half a character below the normal line).
-   `<sup>`: Defines superscripted text (appears half a character above the normal line).
-   **Example**:
    ```html
    <p>This is <b>bold</b> and this is <strong>important</strong>.</p>
    <p>This is <i>italic</i> and this is <em>emphasized</em>.</p>
    <p>This is <mark>highlighted</mark> text.</p>
    ```

### Anchors (Hyperlinks)

Anchors are used to create links to other web pages or to different sections of the same page.

-   **Tag**: `<a>`
-   **Attributes**:
    -   `href`: Specifies the URL of the page the link goes to.
    -   `target`: Specifies where to open the linked document (e.g., `_blank` opens it in a new tab).
    -   `title`: Provides extra information about the link, often shown as a tooltip.
-   **Example**:
    ```html
    <a href="https://www.google.com" target="_blank" title="Go to Google">Visit Google</a>
    ```

### Images

Images are used to embed pictures on a web page.

-   **Tag**: `<img>` (This is a void element, it has no closing tag).
-   **Attributes**:
    -   `src`: Specifies the path to the image.
    -   `alt`: Provides an alternate text for the image, which is displayed if the image cannot be loaded. It's also crucial for accessibility.
    -   `width` and `height`: Specify the dimensions of the image.
    -   `title`: Provides extra information about the image, often shown as a tooltip.
    -   `loading`: Specifies whether a browser should load an image immediately or to defer loading of off-screen images (`lazy`).
-   **Example**:
    ```html
    <img src="images/my-image.jpg" alt="A descriptive text for the image" width="500" height="300">
    ```

### Figures and Captions

The `<figure>` element is used to wrap an image, illustration, diagram, or code snippet, and can be associated with a caption using `<figcaption>`.

-   **Tags**: `<figure>`, `<figcaption>`
-   **Usage**: `<figure>` groups the content, and `<figcaption>` provides a caption for it.
-   **Example**:
    ```html
    <figure>
        <img src="images/my-image.jpg" alt="A descriptive text">
        <figcaption>Fig.1 - A caption for the image.</figcaption>
    </figure>
    ```

### Picture Element

The `<picture>` element gives web developers more flexibility in specifying image resources. It contains one or more `<source>` elements and one `<img>` element to offer alternative versions of an image for different display/device scenarios.

-   **Tags**: `<picture>`, `<source>`
-   **Attributes for `<source>`**:
    -   `srcset`: Defines the URL of the image to use in different situations.
    -   `media`: A media condition (like a CSS media query) that the user agent will evaluate to select a `<source>`.
    -   `type`: Specifies the MIME type of the resource.
-   **Example**:
    ```html
    <picture>
       <source media="(min-width: 650px)" srcset="images/large-image.jpg">
       <source media="(min-width: 465px)" srcset="images/medium-image.jpg">
       <img src="images/small-image.jpg" alt="A responsive image">
    </picture>
    ```

### HTML Comments

Comments are used to add notes to the HTML code that are not displayed in the browser.

-   **Tag**: `<!-- ... -->`
-   **Usage**: Helps in documenting the HTML source code.
-   **Example**:
    ```html
    <!-- This is a comment and will not be displayed -->
    <p>This is a visible paragraph.</p>
    ```

### HTML Entities

Some characters are reserved in HTML. To display them, you need to use character entities.

-   **Usage**: An entity starts with an ampersand (`&`) and ends with a semicolon (`;`).
-   **Common Entities**:
    -   `&lt;`: Less than (`<`)
    -   `&gt;`: Greater than (`>`)
    -   `&amp;`: Ampersand (`&`)
    -   `&quot;`: Double quote (`"`)
    -   `&copy;`: Copyright symbol (`©`)
    -   `&reg;`: Registered trademark symbol (`®`)
-   **Example**:
    ```html
    <p>The copyright symbol is &copy;. The less than sign is &lt;.</p>
    ```

### Void Elements

Void elements are elements in HTML that do not have any content. They don't have a closing tag.

-   **Common Void Elements**:
    -   `<br>`: Inserts a single line break.
    -   `<hr>`: Represents a thematic break between paragraph-level elements (e.g., a change of scene in a story, or a shift of topic with a section). It is typically displayed as a horizontal rule.
    -   `<img>`: Embeds an image.
    -   `<input>`: An input field.
    -   `<link>`: Links to an external resource (like a stylesheet).
    -   `<meta>`: Provides metadata about the HTML document.
-   **Example**:
    ```html
    <p>This is some text.<br>This text is on a new line.</p>
    <hr>
    <p>This is after the horizontal rule.</p>
    ```

This summary covers the fundamental HTML tags and concepts demonstrated in the project files. For more in-depth information, refer to the resources in the `README.md` file.