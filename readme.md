# HTML Introduction Notes

HTML (HyperText Markup Language) is the backbone of all web pages. It defines the structure and content that users see in their web browsers.

---

## 1. What is HTML?

* **HTML** stands for **HyperText Markup Language**.
* It is the **standard markup language** for documents designed to be displayed in a web browser.
* It describes the **structure** of a web page using a series of **elements**.
* HTML elements tell the browser how to display the content (e.g., as a heading, a paragraph, an image, or a link).

---

## 2. Basic HTML Components

### A. Tags and Elements

* An **HTML Element** is everything from the start tag to the end tag.
    * **Syntax:** `<tagname>Content goes here...</tagname>`
* An **HTML Tag** is just the opening or closing word (e.g., `<p>` is the start tag, `</p>` is the end tag).
* Most elements have both an opening and closing tag, but some are **self-closing** or **empty elements** (e.g., `<br>` for a line break, `<img>` for an image).

### B. Attributes

* **Attributes** provide **additional information** about elements.
* They are always specified in the **start tag**.
* Attributes always come in **name/value pairs**: `name="value"`.
* **Example:** The `href` attribute in a link tag: `<a href="https://www.example.com">Visit Example</a>`

---

## 3. The HTML Page Structure (The Skeleton)

Every fundamental HTML document uses this basic structure to ensure compatibility and correct rendering.



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Page Title Appears in Browser Tab</title>
</head>
<body>
    <h1>This is a visible Heading</h1>
    <p>This is a visible paragraph.</p>
</body>
</html>

```

## Key Structural HTML Tags

| Tag | Function | Note |
| :--- | :--- | :--- |
| `<!DOCTYPE html>` | Defines the document type to be **HTML5**. | Must be the very first line. |
| `<html>` | The **root element** of the page. | Everything else is nested inside this. |
| `<head>` | Contains **non-visible information (metadata)**. | Sets title, character set, links to stylesheets. |
| `<title>` | Sets the text that appears in the **browser tab**. | Essential for search engine optimization (SEO). |
| `<body>` | Contains all the **visible content** of the web page. | Headings, paragraphs, links, images, etc. |


##  HTML Documents and DOCTYPE

### 1. Structure of an HTML Document

All HTML documents follow a fundamental structure:

* **Document Type Declaration:** All documents **must** start with the document type declaration: `<!DOCTYPE html>`.
* **Root Element:** The HTML document itself begins with the opening tag `<html>` and ends with the closing tag `</html>`.
* **Visible Content:** The visible part of the HTML document (what the user sees) is contained between the `<body>` tag and the `</body>` tag.

### 2. The <!DOCTYPE> Declaration

The `<!DOCTYPE>` declaration is crucial for web browsers:

* **Purpose:** It represents the document type and helps browsers know which **HTML standard** to use when displaying the page. This ensures the web page renders **correctly** and consistently across different browsers.
* **Placement:** It must only appear **once**, right at the very **top** of the page (before any `<html>` tags).
* **Case Sensitivity:** The `<!DOCTYPE>` declaration is **not case sensitive** (e.g., `<!doctype html>` or `<!DOCTYPE HTML>` would work, but `<!DOCTYPE html>` is the standard convention).
* **The Declaration for HTML5 is:**

```html
<!DOCTYPE html>
```

##  HTML Headings

HTML headings are essential for defining the **structure and hierarchy** of content on a web page. 

### Definition and Usage

* HTML headings are defined using the tags `<h1>` through `<h6>`.
* These tags are used to title sections of content, much like titles and subtitles in a book or an essay.
* **Importance:** They are crucial for both users (who can quickly scan the page) and **Search Engines (SEO)**, as they index the structure and content of your page based on these headings.

### Heading Hierarchy

* `<h1>` defines the **most important** heading (the main title of the page). There should ideally only be **one** `<h1>` per page.
* `<h6>` defines the **least important** heading (the smallest subtitle).
* The hierarchy must be logical (e.g., don't skip from `<h1>` directly to `<h3>`).

### Example Code

```html
<h1>This is heading 1 (Most Important)</h1>
<h2>This is heading 2 (A major section)</h2>
<h3>This is heading 3 (A subsection of h2)</h3>
<h4>This is heading 4</h4>
<h5>This is heading 5</h5>
<h6>This is heading 6 (Least Important)</h6>