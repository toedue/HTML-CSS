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

Tags:

- `<dl>` = list container
- `<dt>` = term/name
- `<dd>` = description (indented automatically)

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


# HTML Images – Complete Markdown Notes

## The `<img>` Tag – Basic Syntax
```html
<img src="path/to/image.jpg" alt="Description of image">
```
- **Empty tag** → no closing tag needed
- **Two REQUIRED attributes**:
  - `src` → path/URL to the image
  - `alt` → alternate text (for accessibility & fallback)

### Examples
```html
<img src="pic_trulli.jpg" alt="Italian Trulli house">
<img src="images/logo.png" alt="Company logo">
<img src="https://example.com/photo.jpg" alt="External image">
```

## Essential Attributes

| Attribute   | Purpose                                    | Example                              |
|-------------|--------------------------------------------|--------------------------------------|
| `src`       | Image location (relative or absolute URL)  | `src="img/photo.jpg"`                |
| `alt`       | Alternate text (screen readers, fallback)  | `alt="Sunset over mountains"`        |
| `width`     | Width in pixels (or %)                     | `width="500"` or `width="100%"`      |
| `height`    | Height in pixels (or %)                    | `height="300"`                       |
| `style`     | Inline CSS (recommended for size)          | `style="width:500px;height:auto;"`   |
| `loading`   | Lazy loading (improves performance)        | `loading="lazy"`                     |

### Best Practice: Always set width & height
```html
<img src="photo.jpg" alt="Beach" width="800" height="600">
<!-- OR with CSS (preferred) -->
<img src="photo.jpg" alt="Beach" style="width:800px;height:auto;">
```
Prevents layout shift while image loads

## Image Paths

| Type                  | Syntax                                    | Example                                   |
|-----------------------|-------------------------------------------|-------------------------------------------|
| Same folder           | `src="image.jpg"`                         |                                           |
| Subfolder             | `src="images/image.jpg"`                  |                                           |
| Parent folder         | `src="../image.jpg"`                      |                                           |
| Root-relative         | `src="/images/image.jpg"`                 | (starts from domain root)                 |
| External URL          | Full https:// link                        | `src="https://example.com/pic.jpg"`       |

## Animated Images
HTML fully supports animated GIFs, APNG, and WebP:
```html
<img src="dancing-cat.gif" alt="Dancing cat animation">
```

## Image as a Link
```html
<a href="https://example.com">
  <img src="button.png" alt="Click here">
</a>
```

## Floating Images with CSS
```html
<img src="smiley.png" alt="Smiley" style="float:right; margin:0 0 10px 10px;">
<p>Text will wrap around the image...</p>
```
Use `float: left` or `float: right`

## Common Image Formats (Browser-Supported)

| Format | Extension         | Best For                       | Notes                     |
|--------|-------------------|--------------------------------|---------------------------|
| JPEG   | .jpg, .jpeg       | Photos                         | Good compression          |
| PNG    | .png              | Logos, icons, transparency     | Lossless + alpha channel  |
| GIF    | .gif              | Simple animations, small icons | Limited to 256 colors     |
| WebP   | .webp             | Best quality/size ratio        | Modern, supported widely  |
| AVIF   | .avif             | Even smaller than WebP         | Newest, excellent quality |
| SVG    | .svg              | Icons, logos (vector)          | Scalable, editable        |

**Pro Tip:**  
For responsive images, combine with CSS:
```css
img {
  max-width: 100%;
  height: auto;
  display: block;
}
```


# HTML Links 

## The `<a>` Tag – Hyperlinks
```html
<a href="https://example.com">Visible link text</a>
```
- **Most important attribute:** `href` → destination URL
- Link text (or image/element) is what users click
- Can wrap **any** element: text, images, buttons, divs, etc.

### Default Browser Styles
- Unvisited link → **blue + underlined**
- Visited link → **purple + underlined**
- Active link → **red + underlined**  
(Override with CSS anytime!)

## Target Attribute – Where to Open the Link

| Value       | Behavior                                    | Use Case                              |
|-------------|---------------------------------------------|---------------------------------------|
| `_self`     | Same tab/window (default)                   | Normal navigation                     |
| `_blank`    | New tab/window                              | External sites, downloads             |
| `_parent`   | Parent frame (for frames/iframes)           | Legacy frames                         |
| `_top`      | Full window (breaks out of all frames)      | Legacy frames                         |

### Example: Open in new tab (most common)
```html
<a href="https://google.com" target="_blank">Google (new tab)</a>
```
**Pro tip:** Add `rel="noopener"` for security/performance:
```html
<a href="https://google.com" target="_blank" rel="noopener">Google</a>
```

## Absolute vs Relative URLs

| Type           | Example                                    | When to Use                              |
|----------------|--------------------------------------------|------------------------------------------|
| Absolute       | `https://example.com/page.html`            | External websites                        |
| Root-relative  | `/images/photo.jpg`                        | Same site, starts from domain root       |
| Relative       | `contact.html` or `../about/team.html`    | Same site, relative to current page      |

### Examples
```html
<!-- Absolute -->
<a href="https://w3schools.com">W3Schools</a>

<!-- Root-relative (good for large sites) -->
<a href="/html/tutorial.html">HTML Tutorial</a>

<!-- Relative (same folder) -->
<a href="about.html">About</a>

<!-- Relative (parent folder) -->
<a href="../index.html">Home</a>
```

## Image as a Link
```html
<a href="https://example.com">
  <img src="button.png" alt="Go to Example">
</a>
```

## Link to Email
```html
<a href="mailto:hello@example.com">Send Email</a>
```
Add subject and body:
```html
<a href="mailto:hello@example.com?subject=Hi%20There&body=Hello%20world!">
  Send pre-filled email
</a>
```

## Link to Phone Number (Mobile)
```html
<a href="tel:+1234567890">Call: +1 (234) 567-890</a>
```

## Button as a Link (with JavaScript)
```html
<button onclick="location.href='https://example.com'">
  Go to Example
</button>
```

## Title Attribute – Tooltip on Hover
```html
<a href="https://example.com" title="Visit Example.com - Best site ever!">
  Example.com
</a>
```

## Best Practices Summary

| Do                                      | Don't                                  |
|-----------------------------------------|----------------------------------------|
| Always use descriptive link text        | Avoid “click here”                     |
| Use `target="_blank"` + `rel="noopener"`| Open new tabs without warning          |
| Add `alt` to images used as links      | Leave broken or missing `href`         |
| Use relative URLs for internal links    | Hardcode full URLs for same-site pages |

## Bonus: Common Link Variations

```html
<!-- Download file -->
<a href="resume.pdf" download>Download Resume</a>

<!-- Smooth scroll to section -->
<a href="#contact">Go to Contact</a>
<div id="contact">...</div>

<!-- Open WhatsApp -->
<a href="https://wa.me/1234567890">Chat on WhatsApp</a>
```


# HTML Forms 

## The `<form>` Element
- Container for all form controls
- Collects user input and sends it to a server

```html
<form action="/submit-form.php" method="post">
  <!-- form controls go here -->
</form>
```

### Important Attributes
| Attribute  | Purpose                                    | Example                          |
|------------|--------------------------------------------|----------------------------------|
| `action`   | URL where form data is sent                | `action="/login.php"`            |
| `method`   | HTTP method: `get` (default) or `post`     | `method="post"` (recommended)    |
| `name`     | Name of the form (for JS/DOM)              | `name="signupForm"`              |
| `novalidate` | Disable browser validation               | `novalidate`                     |

## The `<input>` Element – Most Common Form Control

### Basic Syntax
```html
<input type="text" name="username" id="username">
```

### Required Attributes for Submission
- `name` → **MUST have** (this is how data is sent to server)
- Without `name`, the input value is **not submitted**

### Common Input Types

| Type              | Description                              | Example Use                     |
|-------------------|------------------------------------------|---------------------------------|
| `text`            | Single-line text                         | Name, email                     |
| `password`        | Masked text input                        | Login password                  |
| `radio`           | Select **one** option                    | Gender, yes/no                  |
| `checkbox`        | Select **zero or more** options          | Hobbies, terms agreement        |
| `submit`          | Submit button                            | Send form                       |
| `button`          | Clickable button (no auto-submit)        | Custom JS actions               |
| `email`           | Validates email format                   | Contact forms                   |
| `number`          | Numeric input                            | Age, quantity                   |
| `date`            | Date picker                              | Birthday                        |
| `file`            | File upload                              | Upload photo                    |
| `hidden`          | Hidden field (send data silently)        | User ID, CSRF token             |

## Text Fields Example
```html
<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname"><br><br>

  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname">
</form>
```

## The `<label>` Element – Accessibility Best Practice
- Clickable label toggles control
- Screen readers announce it properly

```html
<label for="email">Email address:</label>
<input type="email" id="email" name="email">

<!-- Or wrap the input (implicit binding) -->
<label>
  <input type="checkbox" name="newsletter"> Subscribe to newsletter
</label>
```

**Always** match `for` attribute with input `id`

## Radio Buttons (Choose One)
```html
<p>Choose your favorite language:</p>
<input type="radio" id="html" name="fav_language" value="HTML">
<label for="html">HTML</label><br>

<input type="radio" id="css" name="fav_language" value="CSS">
<label for="css">CSS</label><br>

<input type="radio" id="js" name="fav_language" value="JavaScript">
<label for="javascript">JavaScript</label>
```
**Key:** All radios in a group must have the **same `name`**

## Checkboxes (Choose Many)
```html
<input type="checkbox" id="bike" name="vehicle" value="Bike">
<label for="bike">I have a bike</label><br>

<input type="checkbox" id="car" name="vehicle" value="Car">
<label for="car">I have a car</label>
```

## Submit Button
```html
<form action="/submit.php" method="post">
  <input type="text" name="username" placeholder="Enter username">
  <input type="submit" value="Send Form">
</form>
```
- `value` = text shown on button
- Clicks → sends data to `action` URL

## Complete Working Example
```html
<!DOCTYPE html>
<html>
<body>
  <h2>User Registration</h2>

  <form action="/register.php" method="post">
    <label for="fname">First Name:</label><br>
    <input type="text" id="fname" name="fname" required><br><br>

    <label for="lname">Last Name:</label><br>
    <input type="text" id="lname" name="lname" required><br><br>

    <p>Gender:</p>
    <input type="radio" id="male" name="gender" value="male">
    <label for="male">Male</label><br>

    <input type="radio" id="female" name="gender" value="female">
    <label for="female">Female</label><br><br>

    <input type="checkbox" id="terms" name="terms" required>
    <label for="terms">I accept the terms and conditions</label><br><br>

    <input type="submit" value="Register Now">
  </form>
</body>
</html>
```

## Key Rules Summary

| Rule                                  | Why It Matters                          |
|---------------------------------------|-----------------------------------------|
| Every submitted input needs `name`    | Otherwise value is ignored              |
| Radio buttons in group → same `name`  | Allows only one selection               |
| Use `<label for="id">`                | Accessibility + better UX               |
| Use `method="post"` for sensitive data| Hides data from URL                     |
| Always test your form!                | Broken forms = lost users               |

**Pro Tip:** In real projects, you’ll style forms with CSS and validate with JavaScript/HTML5 attributes (`required`, `pattern`, etc.). But this is the pure HTML foundation you need! 🚀


# HTML Boilerplate

## 1. What is Boilerplate?

* **Definition:** "Boilerplate" refers to sections of code that are **repeatedly used** in various places with little or no alteration. It is the basic, necessary structure required to start any new project of a certain type.
* **Purpose:** It ensures that every new document starts with the **correct foundational structure** that all modern browsers expect.

## 2. The Standard HTML5 Boilerplate

The HTML5 boilerplate is the minimal structure required for a valid, functional HTML page. It includes tags that define the document type, the page structure, and necessary metadata.



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Page Title Here</title>
</head>
<body>
    </body>
</html>
```

# Most Commonly Used HTML Tags

These tags form the foundation of almost every web page and are the most frequently used elements for structuring and displaying content.

---

## 1. Structural Tags (The Skeleton)

| Tag | Name | Purpose | Example Use |
| :--- | :--- | :--- | :--- |
| `<!DOCTYPE html>` | DOCTYPE | Defines the document type to be HTML5. | Must be the first line. |
| `<html>` | HTML Root | The container for all other HTML elements. | `<html lang="en">...</html>` |
| `<head>` | Head | Contains metadata and links to resources (not visible on the page). | `<head><title>Title</title></head>` |
| `<body>` | Body | Contains all the visible page content. | `<body><h1>Hi</h1></body>` |
| `<div>` | Division | A generic **block-level** container, often used to group elements for styling with CSS. | `<div>...</div>` |
| `<span>` | Span | A generic **inline** container, often used to apply styles to small parts of text. | `<p>This is a <span>word</span></p>` |

---

## 2. Text and Heading Tags

| Tag | Name | Purpose | Example Use |
| :--- | :--- | :--- | :--- |
| `<h1>` to `<h6>` | Headings | Define the hierarchy of content, where `<h1>` is the most important. | `<h2>Section Title</h2>` |
| `<p>` | Paragraph | Defines a block of text. | `<p>This is text content.</p>` |
| `<br>` | Break | Inserts a single line break (an empty element). | `Line 1<br>Line 2` |
| `<hr>` | Horizontal Rule | Draws a thematic break (a horizontal line) across the page. | `<hr>` |
| `<b>` or `<strong>` | Bold/Strong | **`<strong>`** gives semantic importance; **`<b>`** is just for visual boldness. | `<strong>Important!</strong>` |
| `<i>` or `<em>` | Italic/Emphasis | **`<em>`** gives semantic emphasis; **`<i>`** is for text in an alternate voice (e.g., technical terms). | `<em>Emphasis</em>` |

---

## 3. Link and Media Tags

| Tag | Name | Purpose | Example Use |
| :--- | :--- | :--- | :--- |
| `<a>` | Anchor/Link | Creates a hyperlink to another page or a section on the current page. Requires the `href` attribute. | `<a href="page.html">Link</a>` |
| `<img>` | Image | Embeds an image. Requires `src` (source) and `alt` (alternative text) attributes. | `<img src="pic.jpg" alt="A Photo">` |
| `<ul>` | Unordered List | Creates a bulleted list. | `<ul><li>Item</li></ul>` |
| `<ol>` | Ordered List | Creates a numbered list. | `<ol><li>Item</li></ol>` |
| `<li>` | List Item | Defines an item within an ordered or unordered list. | `<li>List Item</li>` |


# The HTML <meta> Tag

The `<meta>` tag provides **metadata** (data about data) about the HTML document. Metadata is essential because it is **not displayed** on the page itself, but is used by browsers, search engines, and other web services.

---

## 1. Syntax and Placement

* The `<meta>` tag is a **self-closing** (empty) tag.
* It must always be placed **inside the `<head>` element** of the HTML document.
* Metadata is typically defined by the use of **attributes**.

### Example Placement

```html
<head>
    <meta charset="UTF-8"> 
    <meta name="description" content="Free web tutorials">
    <title>W3Schools</title>
</head>

```

# 

HTML Formatting Tags

HTML formatting elements were traditionally used to give text a specific look (like bold or italic). Today, many tags also carry **semantic meaning**, telling the browser and assistive technologies *why* the text is styled that way.

---

## 1. Semantic Formatting (Recommended)

These tags define the content's meaning or importance. Browsers typically display them with a certain style, but that style can be changed with CSS.

| Tag | Display Style | Semantic Meaning | Usage |
| :--- | :--- | :--- | :--- |
| `<strong>` | **Bold** | **Important text.** Indicates content of strong importance, seriousness, or urgency. | `<p>Safety measures are <strong>critical</strong>.</p>` |
| `<em>` | *Italic* | **Emphasized text.** Indicates stress or emphasis, changing the meaning of the sentence. | `<p>I *must* leave now.</p>` |
| `<mark>` | Highlighted | **Marked/Highlighted text.** Indicates text relevant in a particular context (like search results). | `<p>Search for <mark>HTML tags</mark>.</p>` |
| `<del>` | <del>Strikethrough</del> | **Deleted text.** Indicates text that has been deleted from a document. | `<p>Old price: <del>$20</del></p>` |
| `<ins>` | Underlined | **Inserted text.** Indicates text that has been inserted into a document. | `<p>New price: <ins>$15</ins></p>` |

---

## 2. Basic Formatting (Presentational)

These tags are primarily used for their visual appearance, though some still have secondary semantic roles. **It is generally better to use CSS for visual styling and semantic tags where possible.**

| Tag | Display Style | Purpose | Usage |
| :--- | :--- | :--- | :--- |
| `<b>` | **Bold** | **Bold text.** Used to draw attention to text without conveying extra importance. | `<b>Company Name</b>` |
| `<i>` | *Italic* | **Italic text.** Used for technical terms, phrases from another language, or thoughts (alternate voice). | `<i>Cascading Style Sheets</i>` |
| `<small>` | Smaller | **Smaller text.** Used to make the text size slightly smaller than the surrounding text (often for copyright or legal disclaimers). | `<small>© 2024</small>` |
| `<u>` | <u>Underlined</u> | **Underlined text.** Used for annotations or misspelled words, though generally discouraged as it can be confused with links. | `<u>Misspelled</u>` |

---

## 3. Special Text Formatting

| Tag | Display Style | Purpose | Example Use |
| :--- | :--- | :--- | :--- |
| `<sub>` | Subscript | **Subscripted text.** Used for chemical formulas or mathematical variables. | `H<sub>2</sub>O` |
| `<sup>` | Superscript | **Superscripted text.** Used for exponents or footnotes. | `E = mc<sup>2</sup>` |

# HTML Tags Categorized by Function

This summary breaks down the most commonly used HTML tags based on their primary purpose in a web document.

---

## 1. Structural Tags (Layout & Organization)

These tags are used to define the overall structure of the document and group related content together.

| Tag | Function | Level | Note |
| :--- | :--- | :--- | :--- |
| `<html>` | Root Element | N/A | Wraps all content on the page. |
| `<head>` | Metadata Container | N/A | Contains non-visible information (title, links, scripts). |
| `<body>` | Visible Content | N/A | Contains all content displayed to the user. |
| `<div>` | Division | Block | A generic container for flow content; often used for layout. |
| `<span>` | Span | Inline | A generic inline container; often used for styling small phrases. |
| `<header>` | Semantic | Block | Introductory content, often containing navigation or logos. |
| `<footer>` | Semantic | Block | Concluding content, often containing copyright or contact info. |
| `<main>` | Semantic | Block | Defines the dominant content of the document. |
| `<section>` | Semantic | Block | A thematic grouping of content, typically with a heading. |
| `<article>` | Semantic | Block | Self-contained, distributable content (e.g., a blog post). |
| `<nav>` | Semantic | Block | Contains navigation links. |

---

## 2. Formatting & Text Tags (Semantics)

These tags define the appearance and semantic meaning of text within a document.

| Tag | Function | Semantic Meaning | Example |
| :--- | :--- | :--- | :--- |
| `<h1>` to `<h6>` | Headings | Title hierarchy (H1 is most important). | `<h1>Page Title</h1>` |
| `<p>` | Paragraph | Defines a block of text. | `<p>Text content.</p>` |
| `<strong>` | Strong Importance | Indicates content of strong importance. | `<strong>Danger!</strong>` |
| `<em>` | Emphasis | Indicates content that should be stressed or emphasized. | `<em>Crucial</em> detail.` |
| `<b>` | Bold | Visually bold text without extra importance. | `<b>Bold text</b>` |
| `<i>` | Italic | Text in an alternate voice or mood (e.g., technical terms). | `<i>Technical Term</i>` |
| `<br>` | Break | Inserts a single line break. | `Line 1<br>Line 2` |
| `<hr>` | Horizontal Rule | Thematic break (a visual line). | `<hr>` |

---

## 3. Meta Tags (Document Data)

These tags provide necessary data about the HTML document itself.

| Tag | Attribute | Purpose | Note |
| :--- | :--- | :--- | :--- |
| `<meta>` | `charset` | Specifies the character encoding (usually `UTF-8`). | Essential for correct display of characters. |
| `<meta>` | `name="viewport"` | Sets page width to device width. | **Crucial for responsive design.** |
| `<title>` | N/A | Defines the title shown in the browser tab. | Essential for SEO and user experience. |
| `<link>` | `rel="stylesheet"` | Links an external style sheet (CSS) to the document. | Must be in `<head>`. |
| `<link>` | `rel="icon"` | Links a favicon (site icon) to the document. | Must be in `<head>`. |

---

## 4. Form Tags (User Input)

These tags are used to collect data from the user and send it to a server.

| Tag | Function | Example Attribute | Note |
| :--- | :--- | :--- | :--- |
| `<form>` | Container | `action="/submit"` | Defines the form and where data is sent. |
| `<input>` | Input Field | `type="text"`, `type="submit"` | The most versatile tag for data entry. |
| `<label>` | Label | `for="username"` | Provides an accessible label for an input field. |
| `<button>` | Button | `type="submit"` | A clickable button for user interaction. |
| `<textarea>` | Text Area | `rows="5"` | Defines a multi-line text input control. |
| `<select>` | Select List | N/A | Creates a drop-down list. |
| `<option>` | Option | `value="val"` | Defines an item in a `<select>` list. |

---

## 5. List Tags (Grouping)

These tags are used to create structured lists of items.

| Tag | Function | Type | Note |
| :--- | :--- | :--- | :--- |
| `<ul>` | Unordered List | Bulleted | Items are marked with bullets. |
| `<ol>` | Ordered List | Numbered/Lettered | Items are marked with numbers or letters. |
| `<li>` | List Item | Item | Defines an item in both `<ul>` and `<ol>`. |
| `<dl>` | Description List | N/A | Defines a list of terms and their descriptions. |
| `<dt>` | Term | N/A | Defines a term (name) in a description list. |
| `<dd>` | Description | N/A | Defines the description of a term. |

---

## 6. Scripting Tags

These tags are used to incorporate client-side dynamic behavior into the HTML page.

| Tag | Function | Example Attribute | Note |
| :--- | :--- | :--- | :--- |
| `<script>` | Client-side Scripting | `src="file.js"` | Used to embed or reference executable code (JavaScript). |
| `<noscript>` | Alternate Content | N/A | Content to be displayed if the user's browser does not support scripts. |

---

## 7. Embedded Content Tags (Media)

These tags are used to embed external content, images, and media directly into the document.

| Tag | Function | Example Attribute | Note |
| :--- | :--- | :--- | :--- |
| `<img>` | Image | `src="path.jpg"`, `alt="text"` | Embeds an image. **Self-closing.** |
| `<a>` | Anchor | `href="url"`, `target="_blank"` | Creates a hyperlink. Not technically *embedded*, but key for media/navigation. |
| `<video>` | Video | `controls` | Embeds a video file and its playback controls. |
| `<audio>` | Audio | `autoplay` | Embeds an audio file and its playback controls. |
| `<source>` | Media Source | `src="path.mp4"` | Specifies multiple media resources for `<video>` or `<audio>`. |
| `<iframe>` | Inline Frame | `src="url"` | Embeds another HTML document within the current one. |