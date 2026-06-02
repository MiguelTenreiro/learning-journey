# Responsive Web Design


# What Role Does HTML Play on the Web?

## What is HTML

- Stands for **Hypertext Markup Language**
- A markup language for creating web pages
- Represents the content and structure of a webpage through **elements**

---

## HTML Elements

- Most elements have an **opening tag** and a **closing tag** (also called start and end tags)
- Content (text or other elements) goes between the two tags
- Tag names are **case-insensitive**, but lowercase is the accepted convention

```html
<h1>Main heading element</h1>
<p>I am a paragraph element.</p>
```

### Opening vs Closing tags

- Both use angle brackets `< >`
- Closing tag has a forward slash `/` after the opening bracket

```html
<p>   <!-- opening tag -->
</p>  <!-- closing tag -->
```

---

## Void Elements

- Some elements **have no closing tag** and **cannot have content**
- Only have a start tag

```html
<img>    <!-- valid -->
<img />  <!-- also valid — the / has no effect per the HTML spec -->
```

> In real-world development you'll see both forms — be familiar with both.

---

## Attributes

- Special values placed inside a tag to adjust the element's behaviour

### `src` — image source
Specifies the location of the image to display.

```html
<img src="https://example.com/photo.jpg" />
```

### `alt` — alternative text
Short descriptive text for the image. Shows when the image fails to load.

```html
<img src="cats.jpg" alt="Two tabby kittens sleeping on a couch." />
```


# HTML Attributes

## What is an attribute

- Values placed inside the opening tag of an HTML element
- Provide extra information or define the element's behaviour
- Syntax: `attribute="value"` — name, `=` sign, and value in quotes

```html

```

---

## Common Attributes

### `href` — hyperlink destination
Required on `<a>` tags. Defines where the link points to.

```html
Go to Google
About page
Send email
```

---

### `target` — where to open the link
Used with `<a>`. `_blank` opens in a new tab; `_self` (default) opens in the same tab.

```html
New tab
Same tab
```

---

### `src` — source file
Required on `<img>`. Specifies the path or URL of the image to display.

```html



```

---

### `alt` — alternative text
Describes the image for screen readers and when the image fails to load.
Not required, but essential for accessibility.

```html


 
```

---

### `type` — input type
Defines what kind of input the user sees and interacts with.

```html
      
  
  
     
```

---

## Boolean Attributes (no value needed)

### `checked` — pre-selected checkbox
If present, the checkbox is checked by default.

```html
  
          
```

---

### `disabled` — non-interactive element
Prevents the user from clicking or typing in the element.

```html

Submit
```

---

### `readonly` — visible but not editable
User can see and copy the value, but cannot change it.

```html

```

---

### `required` — mandatory field
Form cannot be submitted if this field is empty.

```html


```

---

## Key Concept: Accessibility

- Making the web usable for everyone, including people with disabilities
- Covers screen readers, keyboard navigation, and assistive technology
- The `alt` attribute is the most direct example — it describes images to those who cannot see them


# The `link` Element in HTML

## What is the `link` element

- Used to link to **external resources** like stylesheets and site icons
- Always placed inside the `<head>` element
- It is a **void element** — no closing tag

---

## Basic syntax

```html
<link rel="stylesheet" href="./styles.css" />
```

### Key attributes

| Attribute | Purpose |
|---|---|
| `rel` | Defines the **relationship** between the resource and the HTML document |
| `href` | Specifies the **location/URL** of the external resource |

> `./` means "look in the current folder" for the file.

---

## Linking to an external CSS file

Best practice is to keep HTML and CSS in **separate files** and link them with `<link>`.

```html
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>My Page</title>
  <link rel="stylesheet" href="./styles.css" />
</head>
```

---

## Linking to Google Fonts

Google Fonts are **free and open source** custom fonts. Google provides the HTML code to embed them.

```html
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link
  href="https://fonts.googleapis.com/css2?family=Playwrite+CU:wght@100..400&display=swap"
  rel="stylesheet"
/>
```

> `rel="preconnect"` tells the browser to establish an early connection to that domain, speeding up load times.

---

## Linking to a favicon

A **favicon** (short for *favorite icon*) is the small icon shown in the browser tab next to the page title. Used by most websites to display their brand icon.

```html
<link rel="icon" href="favicon.ico" />
```

---

## Common `rel` values — summary

| Value | Use case |
|---|---|
| `stylesheet` | Link to an external CSS file |
| `preconnect` | Early connection to an external domain (performance) |
| `icon` | Link to a favicon |



# HTML Boilerplate

## What is a boilerplate

- A **ready-made template** with the basic structure every HTML document needs
- Acts as the foundation for any web project
- Ensures pages are structured correctly and work across different browsers
- Saves time and helps avoid common mistakes

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>

  <header>
    <h1>Hello, World!</h1>
  </header>

  <main>
    <p>Start your content here.</p>
  </main>

  <footer>
    <p>&copy; 2026 Your Name</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
```

---

## Breaking down the boilerplate

### `<!DOCTYPE html>`
Tells the browser which version of HTML is being used.

```html
<!DOCTYPE html>
```

---

### `<html lang="en">`
Wraps all page content. The `lang` attribute specifies the language of the page.

```html
<html lang="en">
  <!-- all other elements go here -->
</html>
```

---

### `<head>` — behind-the-scenes information
Contains metadata and links to external resources. Not visible to the user.

```html
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Document Title</title>
  <link rel="stylesheet" href="./styles.css" />
</head>
```

| Element | Purpose |
|---|---|
| `<meta charset="UTF-8">` | Sets character encoding — ensures special characters display correctly |
| `<meta name="viewport" ...>` | Controls layout on mobile devices |
| `<title>` | Text shown in the browser tab |
| `<link>` | Links to external stylesheets, fonts, icons |

---

### `<body>` — visible content
Everything the user sees goes here: headings, paragraphs, images, etc.

```html
<body>
  <h1>I am a main title</h1>
  <p>Example paragraph text</p>
</body>
```

---

## Why use a boilerplate

- Ensures correct structure across different browsers
- Follows best practices from the start
- Solid starting point for any project
- Can be **customised** over time with your preferred elements and `meta` tags


# UTF-8 Character Encoding

## What is UTF-8

- Stands for **UCS Transformation Format 8**
- A standardized character encoding widely used on the web
- Supports **every character in the Unicode character set** — all writing systems, languages, and technical symbols

---

## Key concepts

| Term | Definition |
|---|---|
| **Character encoding** | The method computers use to store characters as data |
| **Byte** | A unit of data consisting of 8 bits (binary digits) |
| **Unicode** | A universal standard that assigns a unique code to every character |

---

## How to set UTF-8 in HTML

Place this `<meta>` tag inside the `<head>` element:

```html
<meta charset="UTF-8" />
```

> Include this in **every new HTML project** you create.

---

## Full example

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>UTF-8 Example</title>
  </head>
  <body>
    <p>Café</p> <!-- é displays correctly because of UTF-8 -->
  </body>
</html>
```

---

## Why it matters

- Without UTF-8, special characters like `é`, `ñ`, `ü` or `中` may display incorrectly
- Ensures your page renders text correctly for **all languages and symbols**
- It is considered **best practice** to always declare it


# `div` Elements — What They Are and When to Use Them

## What is a `div`

- A **container element** used to group other HTML elements
- Has **no semantic meaning** — it is a generic wrapper
- Mainly used to group elements that will **share CSS styles**

```html
<div>
  <p>Example paragraph element.</p>
</div>
```

---

## When to use `div`

- When you need to group elements purely for **styling or layout purposes**
- When no other semantic element fits the content

> Avoid overusing `div` — if another element is more appropriate, use that instead.

---

## Semantic elements vs `div`

**Semantics** = the meaning of elements in HTML. Semantic elements tell the browser (and assistive technology) what kind of content they contain.

| Element | Semantic meaning | Use when... |
|---|---|---|
| `<div>` | None — generic container | Grouping for CSS/layout only |
| `<section>` | A thematic section of content | Dividing content into distinct sections |

---

## Example — prefer `<section>` over `<div>` for content sections

```html
<!-- ✅ correct — use section for thematic content blocks -->
<section>
  <h2>Mammals</h2>
  <p>Mammals are warm-blooded animals with fur or hair.</p>
  <ul>
    <li>Lion</li>
    <li>Elephant</li>
    <li>Dolphin</li>
  </ul>
</section>

<!-- ⚠️ avoid — div has no semantic meaning -->
<div>
  <h2>Mammals</h2>
  <p>Mammals are warm-blooded animals with fur or hair.</p>
</div>
```

---

## Why semantics matter

- Browsers understand the **purpose** of semantic elements
- Improves **accessibility** for screen readers and assistive technology
- Works correctly across desktops, mobiles, and other devices
- Makes your HTML more **readable and maintainable**


# IDs and Classes in HTML

## The `id` attribute

- Adds a **unique identifier** to an HTML element
- Used to target a specific element in CSS or JavaScript
- Must be **unique** — never use the same `id` more than once on a page

```html
<h1 id="title">Movie Review Page</h1>
```

### Rules for `id` values

- No spaces — use underscores `_` or dashes `-` instead
- Only letters, digits, underscores, and dashes allowed

```html
<!-- ✅ correct -->
<h1 id="main-heading">Main heading</h1>

<!-- ⚠️ avoid — space breaks the id -->
<h1 id="main heading">Main heading</h1>
```

### Referencing an `id` in CSS

Use the `#` symbol followed by the `id` name:

```css
#title {
  color: red;
}
```

---

## The `class` attribute

- Applies a **reusable label** to one or more elements
- Does **not** need to be unique — multiple elements can share the same class
- Multiple classes can be applied to one element, separated by spaces

```html
<!-- single class -->
<div class="box"></div>

<!-- multiple classes -->
<div class="box red-box"></div>
```

### Referencing a `class` in CSS

Use the `.` symbol followed by the class name:

```css
.box {
  width: 100px;
  height: 100px;
}

.red-box {
  background-color: red;
}

.blue-box {
  background-color: blue;
}
```

### Applying multiple classes to multiple elements

```html
<div class="box red-box"></div>
<div class="box blue-box"></div>
<div class="box red-box"></div>
<div class="box blue-box"></div>
```

---

## `id` vs `class` — when to use each

| | `id` | `class` |
|---|---|---|
| **Uniqueness** | Must be unique per page | Can be reused across many elements |
| **Spaces allowed** | No | Yes (each word = a separate class) |
| **CSS selector** | `#id-name` | `.class-name` |
| **Best used for** | Targeting one specific element | Applying styles to groups of elements |


# HTML Entities (Character References)

## What is an HTML entity

- A set of characters used to **represent reserved or special characters** in HTML
- Needed when the HTML parser would otherwise misread a character as code
- Example: `<` is normally the start of a tag — an entity lets you display it as text

```html
<!-- ⚠️ avoid — parser reads <img /> as an actual element -->
<p>This is an <img /> element</p>

<!-- ✅ correct — displays literally as: This is an <img /> element -->
<p>This is an &lt;img /&gt; element</p>
```

---

## The 3 types of character references

### 1. Named character reference
Starts with `&` and ends with `;`

```html
&lt;   <!-- < less-than -->
&gt;   <!-- > greater-than -->
&amp;  <!-- & ampersand -->
```

---

### 2. Decimal numeric reference
Starts with `&#` followed by decimal digits and ends with `;`

```html
&#60;   <!-- < less-than -->
&#169;  <!-- © copyright -->
&#174;  <!-- ® registered trademark -->
```

---

### 3. Hexadecimal numeric reference
Starts with `&#x` followed by hex digits and ends with `;`

```html
&#x3C;    <!-- < less-than -->
&#x20AC;  <!-- € euro -->
&#x03A9;  <!-- Ω Greek capital omega -->
```

---

## Common entities — quick reference

| Symbol | Named | Decimal | Hexadecimal |
|---|---|---|---|
| `<` | `&lt;` | `&#60;` | `&#x3C;` |
| `>` | `&gt;` | `&#62;` | `&#x3E;` |
| `&` | `&amp;` | `&#38;` | `&#x26;` |
| `©` | `&copy;` | `&#169;` | `&#xA9;` |
| `®` | `&reg;` | `&#174;` | `&#xAE;` |
| `€` | `&euro;` | `&#8364;` | `&#x20AC;` |
| `Ω` | `&Omega;` | `&#937;` | `&#x03A9;` |

---

## Why entities matter

- Prevent the HTML parser from **misreading text as code**
- Allow you to display **reserved characters** like `<`, `>`, and `&` as plain text
- Enable **special symbols** (currency, copyright, math) without relying on keyboard input


# The `script` Element in HTML

## What is the `script` element

- Used to **embed or link executable code** in an HTML document
- Most commonly used to run **JavaScript**
- JavaScript adds interactivity to web pages — games, image sliders, form validation, etc.

---

## Writing JavaScript inline

JavaScript can be written directly inside `<script>` tags:

```html
<body>
  <script>
    alert("Welcome to freeCodeCamp");
  </script>
</body>
```

> While this works, it is **not recommended** for real projects — see below.

---

## Linking to an external JavaScript file (best practice)

Use the `src` attribute to point to an external `.js` file:

```html
<script src="path-to-javascript-file.js"></script>
```

| Attribute | Purpose |
|---|---|
| `src` | Specifies the location (source) of the external JavaScript file |

---

## Why separate HTML and JavaScript

This follows the **separation of concerns** design principle — splitting a program into distinct sections, each addressing one responsibility.

| File | Responsibility |
|---|---|
| `.html` | Content and structure |
| `.css` | Styling and design |
| `.js` | Interactivity and behaviour |

> Keeping JavaScript in its own file makes your code **easier to read, maintain, and debug**.

---

## Full example

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My Page</title>
    <link rel="stylesheet" href="./styles.css" />
  </head>
  <body>
    <h1>Hello, world</h1>

    <!-- script goes at the end of body -->
    <script src="./script.js"></script>
  </body>
</html>
```

> Placing `<script>` at the **end of `<body>`** ensures the HTML content loads before the JavaScript runs.