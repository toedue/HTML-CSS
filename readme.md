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

```

# HTML Comments

## What are HTML Comments?
- Comments in HTML are **not displayed** in the browser
- They are used to **document** your code, add reminders, or temporarily hide content
- Very useful for **debugging** and team collaboration

## Syntax
```html
<!-- Your comment goes here -->
```
- Starts with `<!--`
- Ends with `-->`
- Must include the exclamation mark `!` only in the opening tag
- Can span **multiple lines**

## Basic Examples

### Adding Notes & Reminders
```html
<!-- This is a comment -->
<p>This is a paragraph.</p>

<!-- Remember to update the footer in 2026 -->
```

### Hiding Content Temporarily
```html
<p>Visible paragraph</p>

<!-- 
<p>This paragraph is hidden</p>
<p>This one too!</p>
-->

<p>Another visible paragraph</p>
```

### Hiding a Larger Block
```html
<p>Visible content</p>

<!--
  <h2>Welcome Section</h2>
  <img src="banner.jpg" alt="Welcome banner">
  <p>This section is under construction</p>
-->

<p>More visible content</p>
```

### Hiding Inline Content (within a line)
```html
<p>My name is <!-- John Doe --> Jane Smith.</p>
<!-- Output: My name is  Jane Smith. -->
```

### Debugging with Comments
Comment out code line by line to find errors:
```html
<p>This works</p>
<!-- <p>This might be causing the bug</p> -->
<!-- <div class="problem">Test</div> -->
```

## Best Practices & Tips
- Use comments to explain **complex logic** or **why** you did something
- Add **section dividers** for better readability:
  ```html
  <!-- =================================== -->
  <!--           HEADER SECTION           -->
  <!-- =================================== -->
  ```
- Don’t overuse — too many comments can clutter code
- Comments are **ignored by browsers**, but visible in source code (View Page Source)



    
# HTML Paragraphs & Text Formatting

## The `<p>` Element – Paragraphs
- Defines a **paragraph**
- Automatically starts on a **new line**
- Browsers add **margin** before and after (white space)
- Block-level element

```html
<p>This is a paragraph.</p>
<p>This is another paragraph.</p>
```

### Important: Browser Ignores Extra Spaces & Lines
```html
<p>
  This paragraph      has many     spaces
  and
  
  multiple lines
  in the source code.
</p>
```
**Result:** All extra spaces and line breaks are collapsed into **one single space**.

## `<br>` – Line Break
- Forces a **new line** without creating a new paragraph
- **Empty tag** (no closing tag needed)
- Useful inside `<p>`, `<address>`, poems, etc.

```html
<p>This is<br>a paragraph<br>with line breaks.</p>
```
**Output:**
```
This is
a paragraph
with line breaks.
```

## `<hr>` – Horizontal Rule
- Creates a **thematic break** (visual separator)
- Displayed as a **horizontal line**
- **Empty tag**
- Often used to separate sections

```html
<h1>Main Title</h1>
<p>Some content...</p>
<hr>
<h2>Next Section</h2>
<p>More content...</p>
<hr>
```

## The Poem Problem (Without `<pre>`)
```html
<p>
  My Bonnie lies over the ocean.
  My Bonnie lies over the sea.
  My Bonnie lies over the ocean.
  Oh, bring back my Bonnie to me.
</p>
```
**Result:** Everything appears on **one line** (spaces collapsed)

## Solution: `<pre>` – Preformatted Text
- Preserves **both spaces and line breaks**
- Uses a **fixed-width (monospace) font** (usually Courier)
- Perfect for poems, ASCII art, code snippets

```html
<pre>
  My Bonnie lies over the ocean.

  My Bonnie lies over the sea.

  My Bonnie lies over the ocean.

  Oh, bring back my Bonnie to me.
</pre>
```

**Result:**
```
  My Bonnie lies over the ocean.

  My Bonnie lies over the sea.

  My Bonnie lies over the ocean.

  Oh, bring back my Bonnie to me.
```

## Summary Table

| Element   | Purpose                         | Starts New Line? | Preserves Spaces? | Empty Tag? |
|-----------|----------------------------------|------------------|-------------------|------------|
| `<p>`     | Paragraph                       | Yes              | No                | No         |
| `<br>`    | Line break                      | Yes              | No                | Yes        |
| `<hr>`    | Horizontal separator            | Yes              | -                 | Yes        |
| `<pre>`   | Preformatted text (code/poems)  | Yes              | Yes               | No         |

**Tip:** Use `<br>` for simple line breaks, `<pre>` when you need exact formatting!



# Lorem Ipsum – Placeholder Text

## What is Lorem Ipsum?
- **Lorem Ipsum** is a type of **dummy/placeholder text** used in designs, templates, and prototypes
- It is derived from sections of a Latin text by Cicero (De Finibus Bonorum et Malorum, 45 BC), but scrambled and altered
- Purpose: to fill space so viewers focus on **layout, typography, and design** instead of the actual content

## Why Use Lorem Ipsum?
- Prevents clients/readers from getting distracted by meaningful text
- Shows how the final content will look in terms of length and structure
- Standard in the industry for over 500 years (since the 1500s in print, now universal in web design)

## Standard Lorem Ipsum Text (Classic Block)
```text
Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
Ut enim ad minim veniam, quis nostrud exercitation ullamco 
laboris nisi ut aliquip ex ea commodo consequat. 

Duis aute irure dolor in reprehenderit in voluptate velit 
esse cillum dolore eu fugiat nulla pariatur. 
Excepteur sint occaecat cupidatat non proident, 
sunt in culpa qui officia deserunt mollit anim id est laborum.
```

## Shorter Versions (Commonly Used)

### One Paragraph
```text
Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
```

### Few Lines
```text
Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
```

## HTML Example with Lorem Ipsum
```html
<h1>My Awesome Website</h1>

<p>
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
  Curabitur venenatis mauris id lectus placerat, 
  quis volutpat nunc fringilla.
</p>

<hr>

<p>
  Sed ut perspiciatis unde omnis iste natus error sit 
  voluptatem accusantium doloremque laudantium.
</p>
```

# HTML Lists

## Overview
HTML provides **three types** of lists:
1. **Unordered lists** (bullet points)
2. **Ordered lists** (numbered)
3. **Description lists** (term + description)

## 1. Unordered List `<ul>`
- Items marked with **bullets** (• circles by default)

```html
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
  <li>Sugar</li>
</ul>
```

**Display:**
- Coffee
- Tea
- Milk
- Sugar

### Change Bullet Style (with CSS)
```html
<ul style="list-style-type: disc;">   <!-- default -->
<ul style="list-style-type: circle;">
<ul style="list-style-type: square;">
<ul style="list-style-type: none;">   <!-- no bullets -->
```

## 2. Ordered List `<ol>`
- Items marked with **numbers** (1, 2, 3...) by default

```html
<ol>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item</li>
</ol>
```

**Display:**
1. First item
2. Second item
3. Third item

### Change Numbering Type
```html
<ol type="1">   <!-- 1, 2, 3... (default) -->
<ol type="A">   <!-- A, B, C... -->
<ol type="a">   <!-- a, b, c... -->
<ol type="I">   <!-- I, II, III... (Roman uppercase) -->
<ol type="i">   <!-- i, ii, iii... (Roman lowercase) -->
```

### Start from a Specific Number
```html
<ol start="5">
  <li>Starts from 5</li>
  <li>6</li>
</ol>

<!-- Or using the value attribute (older method) -->
<ol>
  <li value="10">Tenth</li>
  <li>Eleventh</li>
</ol>
```

## 3. Description List (Definition List) `<dl>`
- Used for terms and their descriptions
- Perfect for glossaries, metadata, FAQs

```html
<dl>
  <dt>Coffee</dt>
  <dd>- black hot drink made from roasted beans</dd>
  
  <dt>Tea</dt>
  <dd>- aromatic beverage prepared by pouring hot water over leaves</dd>
  
  <dt>Milk</dt>
  <dd>- white liquid produced by mammals</dd>
</dl>
```

**Display:**
**Coffee**  
 - black hot drink made from roasted beans  

**Tea**  
 - aromatic beverage prepared by pouring hot water over leaves  

**Milk**  
 - white liquid produced by mammals

### Multiple Descriptions per Term
```html
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language</dd>
  <dd>The standard language for creating web pages</dd>
</dl>
```

## Nested Lists (Very Common!)
You can nest any list inside another:

```html
<ul>
  <li>Fruits
    <ul>
      <li>Apple</li>
      <li>Banana</li>
      <li>Orange</li>
    </ul>
  </li>
  <li>Vegetables
    <ol>
      <li>Carrot</li>
      <li>Broccoli</li>
    </ol>
  </li>
</ul>
```

## Summary Table

| List Type        | Tag     | Default Marker     | Best For                     |
|------------------|---------|--------------------|------------------------------|
| Unordered        | `<ul>`  | • Bullets          | Items where order doesn't matter |
| Ordered          | `<ol>`  | 1. Numbers         | Steps, rankings, sequences   |
| Description      | `<dl>`  | None (indented)    | Terms & definitions, glossaries |

**Pro Tip:** All list items (`<li>`) must be inside a parent list tag (`<ul>`, `<ol>`, or `<dl>`). Never use `<li>` alone!