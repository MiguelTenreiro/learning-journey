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


# Meta Description and SEO

## What is SEO

- Stands for **Search Engine Optimization**
- A practice that optimises web pages to rank higher and appear more often in search results

---

## The meta description

A short description of the page, set inside the `<head>` using the `<meta>` element:

```html
<meta
  name="description"
  content="Discover expert tips and techniques for gardening in small spaces, choosing the right plants, and maintaining a thriving garden."
/>
```

| Attribute | Purpose |
|---|---|
| `name="description"` | Tells browsers, search engines, and web tools this is a page description |
| `content` | The actual description text |

---

## Best practices

- Keep descriptions **short and concise** — search engines truncate long ones
- Write for the **user**, not just the algorithm — it should clearly summarise the page
- Every page should have a **unique** description

---

## Where does it appear

The meta description is **not visible on the page itself**. It appears in **search engine results page (SERP) snippets**, just below the site link:

```
r/FreeCodeCamp
This is the official subreddit for the freeCodeCamp.org community. Learn to
code for free together with millions of other people...
```

```
freeCodeCamp — GitHub
Our full-stack web development and machine learning curriculum is completely free and
self-paced. We have thousands of interactive coding challenges...
```

---

## Does it directly affect ranking

- **No** — meta descriptions do not directly affect a site's position in search results
- **But** — a well-written description can increase **click-through rates**, which drives more traffic to your site

---

## Full example in context

```html
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta
    name="description"
    content="Learn HTML, CSS and JavaScript for free with thousands of interactive coding challenges."
  />
  <title>freeCodeCamp</title>
</head>
```

# Open Graph (OG) Tags and SEO

## What is the Open Graph protocol

- Enables you to **control how your content appears on social media** (Facebook, LinkedIn, etc.)
- Set through `<meta>` elements inside the `<head>` section
- Well-crafted OG tags lead to higher **click-through rates**, signalling to search engines that your content is relevant

---

## The 4 essential OG properties

### `og:title` — the title shown on social media
```html
<meta property="og:title" content="freeCodeCamp.org" />
```

---

### `og:type` — the type of content being shared
Common values: `website`, `article`, `video`, `music`

```html
<meta property="og:type" content="website" />
```

---

### `og:image` — the preview image shown in the share card
- Use **high quality** images with good dimensions and ratios
- Facebook recommends at least **1200×630px** for high resolution devices, minimum **600×315px**

```html
<meta
  property="og:image"
  content="https://cdn.freecodecamp.org/platform/universal/fcc_meta_1920X1080-indigo.png"
/>
```

---

### `og:url` — the canonical URL of the page
```html
<meta property="og:url" content="https://www.freecodecamp.org" />
```

---

## Other available OG properties

| Property | Purpose |
|---|---|
| `og:description` | Short description of the page |
| `og:audio` | URL to an audio file |
| `og:video` | URL to a video file |
| `og:locale` | Language and region (e.g. `en_US`) |

---

## Full example in context

```html
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>freeCodeCamp</title>

  <meta property="og:title" content="freeCodeCamp.org" />
  <meta property="og:type" content="website" />
  <meta property="og:url" content="https://www.freecodecamp.org" />
  <meta
    property="og:image"
    content="https://cdn.freecodecamp.org/platform/universal/fcc_meta_1920X1080-indigo.png"
  />
  <meta
    property="og:description"
    content="Learn to code for free with millions of other people."
  />
</head>
```

---

## How OG tags affect SEO

- Do **not** directly affect search engine ranking
- Improve the **visual appearance** of shared links in social media feeds
- Higher engagement and click-through rates **signal relevance** to search engines, indirectly boosting SEO



# HTML Audio and Video Elements

## Supported formats

| Element | Supported formats |
|---|---|
| `<audio>` | `mp3`, `wav`, `ogg` |
| `<video>` | `mp4`, `ogg`, `webm` |

---

## The `<audio>` element

### Basic usage
Without any attributes, nothing is visible on the page:

```html
<audio src="audio.mp3"></audio>
```

### With `controls` (recommended)
Displays the built-in playback controls (play, pause, volume):

```html
<audio src="audio.mp3" controls></audio>
```

> Note: Some browsers (e.g. Safari) may not display a volume control by default.

---

## Audio attributes

| Attribute | Type | Purpose |
|---|---|---|
| `src` | — | Location of the audio file |
| `controls` | boolean | Shows built-in playback controls |
| `loop` | boolean | Replays audio continuously |
| `muted` | boolean | Starts audio in a muted state |

### Full example

```html
<audio src="audio.mp3" controls loop muted></audio>
```

---

## Multiple source formats

Different browsers support different formats. Use `<source>` elements inside `<audio>` — the browser picks the first one it can play:

```html
<audio controls>
  <source src="audio.ogg" type="audio/ogg" />
  <source src="audio.wav" type="audio/wav" />
  <source src="audio.mp3" type="audio/mpeg" />
</audio>
```

---

## The `<video>` element

Supports all the same attributes as `<audio>`, plus two extras:

| Attribute | Type | Purpose |
|---|---|---|
| `src` | — | Location of the video file |
| `controls` | boolean | Shows built-in playback controls |
| `loop` | boolean | Replays video continuously |
| `muted` | boolean | Starts video muted |
| `autoplay` | boolean | Plays video automatically on load |
| `width` | — | Sets the width of the video player |
| `poster` | — | Image displayed while the video is loading (video only) |

### Full example

```html
<video
  src="video.mp4"
  controls
  loop
  muted
  autoplay
  poster="thumbnail.jpg"
  width="400"
></video>
```

---

## Multiple source formats for video

Same approach as audio — browser picks the first compatible format:

```html
<video controls width="400" poster="thumbnail.jpg">
  <source src="video.mp4" type="video/mp4" />
  <source src="video.webm" type="video/webm" />
  Your browser does not support the video tag.
</video>
```

> The fallback text (`Your browser does not support the video tag.`) is displayed only if the browser cannot play any of the provided formats.


# Optimizing Media Assets

## The 3 things to consider

| Factor | Goal |
|---|---|
| **Size** | Match image dimensions to how they are displayed |
| **Format** | Use modern, optimised file formats |
| **Compression** | Reduce file size with compression algorithms |

---

## 1. Size

- Always **scale images to the size they will be displayed** — no larger
- Serving a 1920×1080 image styled at 640×480 forces users to download unnecessary data
- Smaller resolution = smaller file size = faster load times

```
Display size:  640×480 px  ✅ serve at 640×480
Actual image: 1920×1080 px ⚠️ wasteful — users download 6× more data than needed
```

---

## 2. Format

| Format | Notes |
|---|---|
| `PNG` | Common but not ideal — large file sizes |
| `JPG` | Common but not ideal — lossy compression |
| `WEBP` | Modern, optimised — preferred over PNG/JPG |
| `AVIF` | Modern, highly optimised — best for most use cases |

> Unless you need to support older browsers, prefer **WEBP** or **AVIF**.

---

## 3. Compression

### Lossless compression
- Original data can be **perfectly reconstructed** after compression
- No quality loss
- Example format: `PNG`
- Example tool: `pngcrush`

```
PNG → pngcrush → smaller PNG, identical quality ✅
```

### Lossy compression
- Some image data is **permanently discarded** on each save or re-compression
- Results in degraded quality over time
- Example format: `JPG`

```
JPG → re-save → JPG with slightly lower quality ⚠️
JPG → re-save again → JPG with even lower quality ⚠️⚠️
```

---

## Quick checklist

- [ ] Image dimensions match the display size
- [ ] Using WEBP or AVIF instead of PNG/JPG where possible
- [ ] Compression applied to reduce file size
- [ ] Avoided re-saving lossy formats (JPG) multiple times



# Image Licenses

## Why licenses matter

- Images are **intellectual property** protected by copyright
- Copyright belongs to the creator (or publisher) by default
- Using an image without permission can have legal consequences

---

## The 3 ways to legally use a copyrighted image

1. Obtain **written permission** from the copyright holder
2. **Purchase a license** from the copyright holder
3. Use it under **fair use**

### Fair use
Use must be both **limited** and **transformative**:

```
✅ Commenting on or reviewing the image
✅ Creating a parody of the image
⚠️ Simply displaying it on your site does not qualify
```

---

## Types of image licenses

### All rights reserved (default)
- The creator holds **all copyright**
- Cannot be used without permission or purchase

### Permissive licenses
- Images are available for use, but **rules apply** — always read the license
- Examples: **Creative Commons**, **BSD**
- Restrictions may include:
  - Making your website open source
  - Not modifying the image

### Public domain
- **No copyright** — free to use without any restrictions
- Images released under **Creative Commons 0 (CC0)** are considered public domain

---

## License types — quick reference

| License type | Can use freely | Modifications allowed | Restrictions |
|---|---|---|---|
| All rights reserved | No | No | Permission or purchase required |
| Permissive (e.g. CC) | Yes | Depends on license | Read the license |
| Public domain / CC0 | Yes | Yes | None |

---

## Where to find free-to-use images

- **Pixabay** — free images, mostly CC0
- **Unsplash** — free high-quality images
- **Search engines** — filter results by license type

> Always verify the license of any image before using it on your website.


# SVGs — Scalable Vector Graphics

## Raster vs Vector images

| | Raster (PNG, JPG) | Vector (SVG) |
|---|---|---|
| **Based on** | Pixels | Paths and equations |
| **Scales well** | No — becomes pixelated | Yes — perfect at any size |
| **File editable as code** | No | Yes — stored in XML |
| **Colour changeable programmatically** | No | Yes |

---

## What is an SVG

- Stands for **Scalable Vector Graphic**
- Tracks data as **paths, points, lines, and curves** — not pixels
- Scales to **any size without quality loss**
- Stored in **XML** — can be used directly in HTML and edited with code

---

## SVG directly in HTML

```html
<svg width="100" height="100" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
  <circle cx="50" cy="50" r="45" stroke="black" stroke-width="4" fill="yellow" />
  <circle cx="35" cy="40" r="5" fill="black" />
  <circle cx="65" cy="40" r="5" fill="black" />
  <path d="M35 65 Q50 80 65 65" stroke="black" stroke-width="4" fill="transparent" />
</svg>
```

### Key SVG elements

| Element | Purpose |
|---|---|
| `<svg>` | Container for the whole drawing — sets up the drawing area |
| `<circle>` | Draws a circle — used for faces, eyes, dots, etc. |
| `<path>` | Draws lines and curves — used for complex shapes like smiles or icons |

### Common attributes

| Attribute | Purpose |
|---|---|
| `width` / `height` | Dimensions of the SVG canvas |
| `viewBox` | Defines the coordinate system for the drawing |
| `fill` | Fill colour of the shape |
| `stroke` | Border/outline colour |
| `stroke-width` | Thickness of the outline |
| `cx` / `cy` | Centre point of a circle |
| `r` | Radius of a circle |

---

## SVG icon examples

```html
<!-- Star -->
<svg width="50" height="50" viewBox="0 0 24 24" fill="gold" xmlns="http://www.w3.org/2000/svg">
  <path d="M12 2L14.9 8.6L22 9.3L17 14.1L18.3 21.2L12 17.8L5.7 21.2L7 14.1L2 9.3L9.1 8.6L12 2Z"/>
</svg>

<!-- Heart -->
<svg width="50" height="50" viewBox="0 0 24 24" fill="crimson" xmlns="http://www.w3.org/2000/svg">
  <path d="M12 21.35L10.55 20.03C5.4 15.36 2 12.28 2 8.5C2 6 4 4 6.5 4C8 4 9.5 4.8 10.5 6.09C11.5 4.8 13 4 14.5 4C17 4 19 6 19 8.5C19 12.28 15.6 15.36 10.45 20.04L12 21.35Z"/>
</svg>

<!-- Checkmark -->
<svg width="50" height="50" viewBox="0 0 24 24" fill="green" xmlns="http://www.w3.org/2000/svg">
  <path d="M20.29 5.71L9 17L3.71 11.71L5.12 10.29L9 14.17L18.88 4.29L20.29 5.71Z"/>
</svg>
```

> To change the colour of any SVG, update the `fill` attribute to any named colour: `red`, `blue`, `green`, etc.

---

## When to use SVGs

- **Icons** — custom bullet points, social media icons, UI icons (e.g. Font Awesome uses SVG)
- **Logos** — scale perfectly at any viewport size
- **Responsive layouts** — adapt to any screen size without quality loss

> Tip: open any `.svg` file in a text editor — you can edit the code directly to change colours, shapes, and sizes.


# Replaced Elements in HTML

## What is a replaced element

- An element whose **content is determined by an external resource**, not by CSS
- CSS can control **position and layout** of the element
- CSS **cannot modify the content** inside the element

---

## Common replaced elements

| Element | What it embeds |
|---|---|
| `<img>` | An external image file |
| `<iframe>` | An external website, video, or map |
| `<video>` | An external video file |
| `<embed>` | An external resource (e.g. PDF, Flash) |

---

## `<img>` — image element

CSS can position or filter the image, but cannot modify the image itself:

```html
<img src="example-img-url" alt="Descriptive text goes here" />
```

---

## `<iframe>` — inline frame element

Embeds an external site, video, or map. CSS can reposition the frame, but cannot style the content inside it.

> If the embedded site has an `<h1>`, your CSS cannot change its size, font, or colour.

### Embedding a YouTube video

```html
<iframe
  width="400"
  height="200"
  src="https://www.youtube.com/embed/VIDEO_ID"
  title="Video title"
  allowfullscreen
></iframe>
```

### Embedding a map

```html
<iframe
  title="Map of Greenwich, London"
  width="300"
  height="200"
  src="https://www.openstreetmap.org/export/embed.html?bbox=..."
></iframe>
```

---

## Conditionally replaced elements

Some elements behave as replaced elements only under **specific circumstances**:

```html
<!-- ✅ replaced element — embeds an image as a clickable input -->
<input type="image" src="example-img-url" alt="Descriptive text" />

<!-- ⚠️ not a replaced element — content is generated by the browser -->
<input type="text" />
<input type="email" />
```

---

## What CSS can and cannot do with replaced elements

| | CSS can | CSS cannot |
|---|---|---|
| `<img>` | Position, resize, apply filters | Modify the image itself |
| `<iframe>` | Position, resize | Style content inside the frame |
| `<video>` | Position, resize | Modify the video content |



# Embedding Videos and Content with `<iframe>`

## What is `<iframe>`

- Stands for **inline frame**
- An inline element used to **embed external HTML content** directly in a page
- Can embed: videos, maps, other web pages, or raw HTML

---

## Key attributes

| Attribute | Purpose |
|---|---|
| `src` | URL of the page or content to embed |
| `srcdoc` | Embed raw HTML directly (instead of a URL) |
| `width` | Width of the iframe in pixels |
| `height` | Height of the iframe in pixels |
| `title` | Describes the iframe content — important for accessibility |
| `allowfullscreen` | Boolean — allows the user to go fullscreen |
| `allow` | Defines an allowlist of features the iframe can use |
| `referrerpolicy` | Controls how much referrer info is sent with requests |

---

## Embedding a YouTube video

```html
<iframe
  width="400"
  height="400"
  src="https://www.youtube.com/embed/VIDEO_ID"
  title="Learn JavaScript - Full Course for Beginners (YouTube video)"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
  referrerpolicy="strict-origin-when-cross-origin"
  allowfullscreen
></iframe>
```

> Videos can come from any source — not just YouTube or Vimeo.

---

## The `allow` attribute (allowlist)

Defines what the embedded page is permitted to do. Items are separated by semicolons or spaces.

```html
allow="accelerometer; autoplay; clipboard-write; encrypted-media"
```

| Value | Permits |
|---|---|
| `autoplay` | Automatically play media |
| `clipboard-write` | Write items to the user's clipboard |
| `fullscreen` | Enter fullscreen mode |
| `accelerometer` | Access device motion sensors |

---

## Embedding a map

```html
<iframe
  width="425"
  height="350"
  src="https://www.openstreetmap.org/export/embed.html?bbox=..."
  title="Map of Lagos area, Nigeria"
  style="border: 1px solid black"
></iframe>

<br />
<small>
  <a href="https://www.openstreetmap.org/#map=11/6.4501/3.3210">View Larger Map</a>
</small>
```

---

## Embedding raw HTML with `srcdoc`

Use `srcdoc` instead of `src` to embed HTML directly:

```html
<iframe srcdoc="<p>Hello from inside the iframe!</p>" title="Embedded HTML"></iframe>
```

---

## Best practices

- Always include a `title` attribute — required for **accessibility**
- Use `allowfullscreen` for video embeds
- Keep the `allow` allowlist as **minimal as needed**
- Prefer `srcdoc` over `src` when embedding raw HTML


# The `target` Attribute in HTML

## What is the `target` attribute

- Used on `<a>` (anchor) elements
- Tells the browser **where to open the linked URL**
- Every value is preceded by an **underscore**

```html
<a href="https://freecodecamp.org" target="_blank">Visit freeCodeCamp</a>
```

---

## The 4 main values

| Value | Behaviour |
|---|---|
| `_self` | Opens in the **current tab/window** (default) |
| `_blank` | Opens in a **new tab** (or new window, depending on browser settings) |
| `_parent` | Opens in the **parent browsing context** (e.g. the page containing an iframe) |
| `_top` | Opens in the **top-most browsing context** — always the full browser tab/window |

---

## Examples

```html
<!-- default behaviour — opens in the same tab -->
<a href="/about" target="_self">About</a>

<!-- opens in a new tab -->
<a href="https://freecodecamp.org" target="_blank">Visit freeCodeCamp</a>

<!-- inside an iframe — opens in the parent page's tab -->
<a href="https://example.com" target="_parent">Open in parent</a>

<!-- inside nested iframes — always opens in the full browser tab -->
<a href="https://example.com" target="_top">Break out of all frames</a>
```

---

## `_parent` vs `_top`

Both are relevant when working with **embedded iframes**:

| Value | Opens in |
|---|---|
| `_parent` | The immediate parent of the current frame |
| `_top` | The outermost browser tab/window — ignores all nesting |

```
Page (tab)
└── iframe
    └── nested iframe
          └── <a target="_parent"> → opens in outer iframe
          └── <a target="_top">   → opens in the page tab
```

---

## Experimental: `_unfencedTop`

- Used for the experimental **FencedFrame API**
- Not yet relevant for general web development

---

## Best practice

Choosing the right `target` value is important for **controlling user navigation** — especially when your page contains embedded frames or links to external sites.


# Absolute vs Relative Paths

## What is a path

- A string that specifies the **location of a file or directory** in a file system
- Used to link to images, stylesheets, scripts, and other pages

---

## Absolute path

A **complete location** of a file, starting from the root directory down to the filename:

```html
<a href="/Users/user/Desktop/fCC/pages/about.html">About Page</a>
```

```
root → Users → user → Desktop → fCC → pages → about.html
```

---

## Absolute URL

A **complete web address** including protocol and domain name:

```html
<a href="https://design-style-guide.freecodecamp.org/img/fcc_secondary_small.svg">
  View fCC Logo
</a>
```

| Part | Example |
|---|---|
| Protocol | `https` |
| Domain | `design-style-guide.freecodecamp.org` |
| Filename | `fcc_secondary_small.svg` |

### How it looks in the browser address bar

```
file:///Users/user/Desktop/fCC/pages/about.html
         └── protocol  └── path           └── filename + extension
```

---

## Relative path

Specifies the location of a file **relative to the current file's directory**. No protocol or domain needed:

```html
<!-- about.html and contact.html are in the same folder -->
<a href="about.html">About Page</a>
```

### Common relative path patterns

```html
<!-- same folder -->
<a href="about.html">About</a>

<!-- subfolder -->
<a href="pages/about.html">About</a>

<!-- one folder up -->
<a href="../about.html">About</a>

<!-- from root of the site -->
<a href="/pages/about.html">About</a>
```

---

## Absolute path vs Absolute URL vs Relative path

| | Absolute path | Absolute URL | Relative path |
|---|---|---|---|
| **Includes protocol** | No (local) | Yes (`https`, `http`, `file`) | No |
| **Includes domain** | No | Yes | No |
| **Best used for** | Local machine resources | External websites | Internal links within the same site |

---

## When to use each

- **Absolute path** — referencing a resource from a fixed location or root directory
- **Absolute URL** — linking to a resource on an **external website**
- **Relative path** — linking to resources **within the same website**
- **Relative path** — keeping code **cleaner and easier to maintain**
- **Relative path** — **local testing** without an internet connection


# Path Syntax — Slashes, Single Dot, and Double Dot

## The 3 key syntaxes

| Syntax | Name | Meaning |
|---|---|---|
| `/` or `\` | Path separator | Separates folder and file names in a path |
| `.` | Single dot | The **current** directory |
| `..` | Double dot | The **parent** directory (one level up) |

> The slash used depends on the OS — `/` on Mac/Linux, `\` on Windows.

---

## The slash `/` — path separator

Tells the computer where one folder or file name ends and the next begins:

```
naomis-files/         → a directory called "naomis-files"
naomis/files/         → a directory called "files" inside "naomis"
```

---

## Single dot `.` — current directory

Points to the folder the current file is in. Commonly used to make clear a path is **relative**:

```html
<script src="./script.js"></script>
<img src="./logo.png" />
```

---

## Double dot `..` — parent directory

Moves **one level up** in the directory tree. Used to access files outside the current folder:

```html
<link rel="stylesheet" href="../styles.css" />
```

---

## Practical example

Given this file structure:

```
my-app/
├─ public/
│  ├─ favicon.ico
│  └─ index.html   ← you are here
└─ src/
   ├─ index.css
   └─ index.js
```

| Goal | Path | Explanation |
|---|---|---|
| Load `favicon.ico` (same folder) | `./favicon.ico` | `.` = current folder (`public/`) |
| Load `index.css` (different folder) | `../src/index.css` | `..` = go up to `my-app/`, then into `src/` |

```html
<!-- favicon — same directory -->
<link rel="icon" href="./favicon.ico" />

<!-- stylesheet — parent directory, then into src/ -->
<link rel="stylesheet" href="../src/index.css" />
```

---

## Quick reference

```
./file.txt         → file in the current folder
../file.txt        → file one level up
../../file.txt     → file two levels up
../other/file.txt  → up one level, then into "other" folder
```



# Link States in HTML & CSS

## What are link states

- Links can be in **5 different states** depending on user interaction
- Each state can be styled differently with CSS using **pseudo-classes**
- They give users visual feedback about links they have or haven't visited

---

## The 5 link states

| State | Pseudo-class | When it applies | Default browser style |
|---|---|---|---|
| Default | `:link` | Link not yet visited or interacted with | Blue |
| Visited | `:visited` | User has already visited the linked page | Purple |
| Hover | `:hover` | Cursor is hovering over the link | — |
| Focus | `:focus` | Link is focused (e.g. via `Tab` key) | — |
| Active | `:active` | Link is being clicked | — |

---

## CSS examples for each state

```css
/* not yet visited */
a:link {
  color: blue;
}

/* already visited */
a:visited {
  color: brown;
}

/* cursor hovering over the link */
a:hover {
  color: red;
}

/* focused via keyboard (Tab key) */
a:focus {
  color: green;
}

/* being clicked */
a:active {
  color: black;
}
```

---

## ⚠️ Required order in CSS

Link states must be written in this exact order to work correctly:

```
1. :link
2. :visited
3. :hover
4. :focus
5. :active
```

> Mnemonic: **L**o**V**e **H**ates **F**ear and **A**nger — **L**ink, **V**isited, **H**over, **F**ocus, **A**ctive

---

## Why link states matter

- `:visited` — helps users know which pages they have already read
- `:hover` — confirms the element is clickable before the user commits to clicking
- `:focus` — essential for **keyboard navigation** and accessibility
- `:active` — gives immediate feedback that a click has been registered


# Basic HTML Review

## HTML Basics

### What is HTML
- Represents the **content and structure** of a web page

### Elements
- Building blocks of an HTML document — headings, paragraphs, links, images, etc.
- Most elements have an **opening** and **closing** tag

```html
<elementName>Content goes here</elementName>
```

### Void elements
- No closing tag, no content — start tag only
- Both forms are acceptable:

```html
<img>
<img />
```

### Attributes
- Values placed inside the opening tag to provide extra information or behaviour

```html
<element attribute="value"></element>
```

- **Boolean attributes** — presence = true, absence = false (e.g. `disabled`, `readonly`, `required`)

### Comments

```html
<!-- This is an HTML comment -->
```

---

## Common HTML Elements

| Element | Purpose |
|---|---|
| `<h1>`–`<h6>` | Headings — `h1` is most important, `h6` least |
| `<p>` | Paragraph |
| `<img src="" alt="">` | Image — `src` required, `alt` recommended |
| `<body>` | Represents the visible content of the page |
| `<section>` | Divides content into thematic sections (semantic) |
| `<div>` | Generic container — no semantic meaning |
| `<a href="">` | Anchor/link — `href` sets the destination |
| `<ul>` / `<ol>` | Unordered / ordered list |
| `<li>` | List item (used inside `ul` or `ol`) |
| `<em>` | Emphasis |
| `<strong>` | Strong importance / urgency |
| `<figure>` | Groups images or diagrams |
| `<figcaption>` | Caption for content inside `<figure>` |
| `<main>` | Main content of the page |
| `<footer>` | Bottom of the page — copyright, links |

```html
<!-- lists -->
<ul><li>Item</li></ul>
<ol><li>Item</li></ol>

<!-- figure -->
<figure>
  <img src="cats.jpg" alt="Two cats sleeping." />
  <figcaption>Cats hate other cats.</figcaption>
</figure>

<!-- footer -->
<footer>
  <p>No Copyright - <a href="https://www.freecodecamp.org">freeCodeCamp.org</a></p>
</footer>
```

---

## IDs and Classes

| | `id` | `class` |
|---|---|---|
| Unique per page | Yes | No |
| Spaces allowed | No (use `-` or `_`) | Yes (each word = separate class) |
| CSS selector | `#id-name` | `.class-name` |
| Best for | Targeting one specific element | Styling groups of elements |

```html
<h1 id="title">Movie Review Page</h1>
<div id="red-box"></div>
<div class="box red-box"></div>
<div class="box blue-box"></div>
```

---

## HTML Entities

Used to display reserved or special characters as plain text:

| Symbol | Named | Decimal | Hex |
|---|---|---|---|
| `<` | `&lt;` | `&#60;` | `&#x3C;` |
| `>` | `&gt;` | `&#62;` | `&#x3E;` |
| `&` | `&amp;` | `&#38;` | `&#x26;` |
| `©` | `&copy;` | `&#169;` | `&#xA9;` |
| `€` | `&euro;` | `&#8364;` | `&#x20AC;` |

```html
<p>This is an &lt;img /&gt; element</p>
```

---

## Linking Resources

### `<link>` — external stylesheets, fonts, icons

```html
<link rel="stylesheet" href="./styles.css" />
<link rel="icon" href="favicon.ico" />
```

### `<script>` — external JavaScript (best practice)

```html
<!-- inline (avoid in real projects) -->
<script>alert("Hello");</script>

<!-- external file (recommended) -->
<script src="./script.js"></script>
```

> Place `<script>` at the **end of `<body>`** so HTML loads before JavaScript runs.

---

## HTML Boilerplate

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Page Title</title>
    <link rel="stylesheet" href="./styles.css" />
  </head>
  <body>
    <!-- content goes here -->
    <script src="./script.js"></script>
  </body>
</html>
```

| Part | Purpose |
|---|---|
| `<!DOCTYPE html>` | Declares HTML5 |
| `<html lang="en">` | Root element — sets page language |
| `<head>` | Behind-the-scenes metadata |
| `<meta charset="UTF-8">` | Character encoding — supports all languages and symbols |
| `<meta name="viewport">` | Responsive layout on mobile |
| `<title>` | Text shown in the browser tab |
| `<body>` | All visible page content |

---

## SEO and Social Sharing

### Meta description
```html
<meta name="description" content="Short description of the page." />
```

### Open Graph tags

```html
<meta property="og:title" content="freeCodeCamp.org" />
<meta property="og:type" content="website" />
<meta property="og:url" content="https://www.freecodecamp.org" />
<meta property="og:image" content="https://example.com/image.png" />
```

| Property | Purpose |
|---|---|
| `og:title` | Title shown in social media previews |
| `og:type` | Content type (`website`, `article`, `video`) |
| `og:url` | Canonical URL for the post |
| `og:image` | Preview image (recommended: 1200×630px min) |

---

## Media

### `<audio>`

```html
<audio src="audio.mp3" controls loop muted></audio>

<!-- multiple formats for browser compatibility -->
<audio controls>
  <source src="audio.ogg" type="audio/ogg" />
  <source src="audio.wav" type="audio/wav" />
  <source src="audio.mp3" type="audio/mpeg" />
</audio>
```

### `<video>`

```html
<video src="video.mp4" controls loop muted poster="thumbnail.jpg" width="400"></video>
```

### Audio/Video attributes

| Attribute | Type | Purpose |
|---|---|---|
| `controls` | boolean | Shows playback controls |
| `loop` | boolean | Replays continuously |
| `muted` | boolean | Starts muted |
| `autoplay` | boolean | Plays automatically |
| `poster` | — | Image shown while video loads (video only) |

### `<iframe>` — embed external content

```html
<iframe
  src="https://www.youtube.com/embed/VIDEO_ID"
  width="560"
  height="315"
  title="Video title"
  allowfullscreen
></iframe>
```

### Media optimisation

| Factor | Recommendation |
|---|---|
| Size | Match image dimensions to display size |
| Format | Prefer `WEBP` or `AVIF` over `PNG`/`JPG` |
| Compression | Lossless (PNG) = no quality loss / Lossy (JPG) = permanent data loss |

### SVGs

- **Scalable Vector Graphic** — paths and equations, not pixels
- Scales to any size without quality loss
- Stored in XML — editable directly in HTML

```html
<svg width="100" height="100" viewBox="0 0 100 100">
  <circle cx="50" cy="50" r="45" fill="yellow" />
</svg>
```

---

## Paths

| Syntax | Meaning |
|---|---|
| `/` | Path separator |
| `./` | Current directory |
| `../` | Parent directory (one level up) |

| Type | Includes protocol/domain | Use when |
|---|---|---|
| Absolute path | No | Referencing from root on local machine |
| Absolute URL | Yes | Linking to external websites |
| Relative path | No | Linking within the same site |

```html
<img src="./photo.jpg" />           <!-- same folder -->
<link href="../src/styles.css" />   <!-- one level up -->
<a href="https://example.com">      <!-- external site -->
```

---

## `target` Attribute

| Value | Opens in |
|---|---|
| `_self` | Same tab (default) |
| `_blank` | New tab |
| `_parent` | Parent browsing context |
| `_top` | Top-most browsing context (escapes all frames) |

```html
<a href="https://freecodecamp.org" target="_blank">Open in new tab</a>
```

---

## Link States

Must be written in this order in CSS:

```css
a:link    { color: blue; }     /* not yet visited */
a:visited { color: purple; }   /* already visited */
a:hover   { color: red; }      /* cursor over link */
a:focus   { color: green; }    /* focused via Tab key */
a:active  { color: black; }    /* being clicked */
```

> Mnemonic: **L**o**V**e **H**ates **F**ear and **A**nger


# Why Semantic HTML Matters

## What is semantics in HTML

- Semantics = the **meaning** of elements in a language
- Each HTML element conveys **special information** about its content
- Think of an HTML document like a text document — headings, paragraphs, bold text all have meaning

```html
<!-- <p> semantically means "a paragraph of text" -->
<p>
  Let me tell you about my fantastic holiday in Paris.
  I saw the impressive Eiffel Tower up close!
</p>
```

> The `<div>` element is one of the very few HTML elements with **no semantic meaning**.

---

## Why semantic HTML matters

### 1. Accessibility
- Ensures the best experience for users with **assistive technology** like screen readers
- Screen readers rely on semantic meaning to describe content correctly

### 2. SEO
- Proper semantic elements can **improve search engine rankings**
- Search engines better understand the structure and relevance of your content

### 3. Developer experience
- Easier to read and navigate your own code
- Instead of sifting through generic `<div>` elements, you can go straight to `<nav>`, `<header>`, `<footer>`, etc.

---

## Semantic vs non-semantic

```html
<!-- ⚠️ avoid — no meaning, hard to read -->
<div>
  <div>My Website</div>
  <div>Welcome to my page</div>
</div>

<!-- ✅ correct — clear meaning at a glance -->
<header>
  <h1>My Website</h1>
  <nav>...</nav>
</header>
<main>
  <p>Welcome to my page</p>
</main>
```

---

## Key takeaway

Using the **right element for the right content** improves:
- Accessibility for all users
- Visibility on search engines
- Readability and maintainability of your code


# Structural Hierarchy in HTML

## What is structural hierarchy

- The correct, logical ordering of **heading elements** in an HTML document
- Think of it like a text document — headings, subheadings, and body text follow a clear order

---

## Heading levels

| Element | Role | Notes |
|---|---|---|
| `<h1>` | Top-level heading | Typically only **one per page** — comes before all content |
| `<h2>` | Subheading | Always after `<h1>` — multiple allowed, used to separate sections |
| `<h3>` | Sub-subheading | Always after `<h2>` — never skip directly from `<h1>` |
| `<h4>`–`<h6>` | Deeper levels | Follow the same rule — never skip levels |

---

## Correct vs incorrect hierarchy

```html
<!-- ✅ correct — logical order, multiple h2s allowed -->
<section>
  <h1>freeCodeCamp</h1>
  <h2>Learn Front-End Development</h2>
  <h2>Learn Back-End Development</h2>
</section>

<!-- ⚠️ incorrect — h3 appears before h2 -->
<section>
  <h1>freeCodeCamp</h1>
  <h3>Introduction to HTML</h3>
  <h2>Learn Front-End Development</h2>
</section>
```

---

## Don't use headings for styling

```html
<!-- ⚠️ avoid — using h1 just to get large text -->
<article>
  <p>Here is some <h1>Large Text</h1></p>
</article>

<!-- ✅ correct — use the right element, style with CSS -->
<article>
  <p class="large-text">Here is some large text</p>
</article>
```

> Choose the heading level that fits the **document structure**, not the visual style you want.

---

## Why hierarchy matters

### Accessibility
- Screen readers rely on heading structure to **navigate and announce content**
- An `<h3>` after an `<h1>` (skipping `<h2>`) may make users think they missed content

### SEO
- Search engines parse heading structure to **rank and categorise content**
- Malformed structure can hurt your position in search results

### Valid HTML
- Incorrect structure may produce **technically invalid HTML**
- Browsers will try to guess your intent — and may get it wrong

---

## Quick rules

- One `<h1>` per page
- Never skip heading levels (e.g. `h1` → `h3`)
- Multiple headings at the same level are fine within sections
- Use CSS for font size — not heading level


# Presentational vs Semantic HTML

## The core difference

| | Presentational HTML | Semantic HTML |
|---|---|---|
| **Focus** | Appearance and style | Meaning and structure |
| **Status** | Deprecated — avoid | Recommended modern practice |
| **Styling** | Done in HTML | Done in CSS |
| **Accessibility** | Poor | Good |
| **Maintainability** | Hard | Easy |

---

## Deprecated presentational elements (avoid these)

### `<font>` — sets font size and colour
```html
<!-- ⚠️ deprecated — don't use -->
<font size="5" color="blue">This text is blue and large.</font>
```
- `size` range: `1` (smallest) to `7` (largest), default is `3`
- Use CSS `color` and `font-size` instead

---

### `<center>` — horizontally centres content
```html
<!-- ⚠️ deprecated — don't use -->
<center>
  This text is centered.
  <p>HTML is awesome.</p>
</center>
```
- Use CSS `text-align: center` instead

---

### `<big>` — makes text one level larger
```html
<!-- ⚠️ deprecated — don't use -->
<p>Normal text. <big>This text is larger.</big></p>
```
- Use CSS `font-size` instead

---

## Semantic HTML elements (use these)

Describe the **purpose** of the content — easy to read, understand, and maintain:

| Element | Purpose |
|---|---|
| `<header>` | Header of the document or section |
| `<nav>` | Section containing navigation links |
| `<main>` | Main content of the page |
| `<section>` | Groups related content |
| `<article>` | Self-contained piece of content |
| `<figure>` | Illustrations, diagrams, images |
| `<footer>` | Bottom of the document or section |

```html
<!-- ✅ semantic — clear structure and purpose -->
<header>
  <nav>
    <a href="#">Home</a>
    <a href="#">About</a>
    <a href="#">Products</a>
    <a href="#">Contact</a>
  </nav>
</header>
```

---

## Why semantic HTML is recommended

- **Accessibility** — screen readers use semantic elements to describe page content
- **SEO** — search engines better understand and rank pages with clear structure
- **Maintainability** — developers can instantly understand the purpose of each section
- **Separation of concerns** — structure in HTML, styling in CSS


# `<em>` vs `<i>` — Emphasis vs Idiomatic Text

## The core difference

| | `<i>` (idiomatic text) | `<em>` (emphasis) |
|---|---|---|
| **Original purpose** | Display text in italics (presentational) | Semantic emphasis |
| **Modern use** | Text that is *different* from surrounding content | Text that is *important* compared to surrounding content |
| **Conveys importance** | No | Yes |
| **Affects meaning** | No | Yes — changes how the sentence is understood |
| **Screen readers** | Treated as visually different | Announced with added stress |

---

## `<i>` — idiomatic text

Used for text that is somehow **different** from the surrounding text, but not necessarily important:

- Foreign or idiomatic phrases
- Technical terms
- Alternative voice or mood
- Thoughts

```html
<!-- foreign language phrase -->
<p>There is a certain <i lang="fr">je ne sais quoi</i> in the air.</p>

<!-- technical term -->
<p>The process is known as <i>photosynthesis</i>.</p>
```

> The `lang` attribute specifies the language of the content inside `<i>`.

---

## `<em>` — emphasis

Used when a word or phrase requires **special emphasis** that changes the meaning of the sentence. Usually limited to a few words:

```html
<p>Never give up on <em>your</em> dreams.</p>
```

> Stressing *your* changes the meaning — it's about your dreams specifically, not someone else's.

---

## When to use neither — use CSS instead

If the text has **no special purpose or meaning** and you just want it to look italic, use CSS:

```html
<!-- ⚠️ avoid — using <i> or <em> for pure styling -->
<p><i>This is just styled text with no special meaning.</i></p>

<!-- ✅ correct — use CSS for presentational italics -->
<p class="stylised">This is just styled text with no special meaning.</p>
```

```css
.stylised {
  font-style: italic;
}
```

---

## Quick decision guide

```
Is the text a foreign phrase, technical term, or alternative voice?
  → use <i>

Does the text need emphasis that changes the meaning of the sentence?
  → use <em>

Do you just want italic styling with no semantic purpose?
  → use CSS font-style: italic
```




# `<strong>` vs `<b>` — Strong Importance vs Bring Attention To

## The core difference

| | `<b>` (bring attention to) | `<strong>` (strong importance) |
|---|---|---|
| **Purpose** | Draw attention to text | Convey importance or urgency |
| **Semantic meaning** | No — purely attention | Yes — signals criticality |
| **Default style** | Bold | Bold |
| **Screen readers** | No special announcement | Announced with added importance |

> Both look the same visually — the difference is in **meaning**, not appearance.

---

## `<b>` — bring attention to

Used to highlight text that should stand out, but **without implying it is critical**:

- Keywords in summaries
- Product names in reviews
- Key terms in prose

```html
<p>
  We tested the <b>SuperSound 3000</b> for audio quality,
  the <b>QuickCharge Pro</b> for fast charging, and the
  <b>EcoClean Vacuum</b> for cleaning.
</p>
```

---

## `<strong>` — strong importance

Used for text that is **crucial, urgent, or serious** — where the meaning would suffer without emphasis:

```html
<p>
  <strong>Warning:</strong> This product may cause allergic reactions.
</p>
```

---

## When to use neither — use CSS instead

If you just want bold text with no semantic purpose, use CSS:

```html
<!-- ⚠️ avoid — using <b> or <strong> for pure styling -->
<p><b>This is just visually bold text.</b></p>

<!-- ✅ correct — use CSS for presentational bold -->
<p class="highlight">This is just visually bold text.</p>
```

```css
.highlight {
  font-weight: bold;
}
```

---

## Quick decision guide

```
Is the text a keyword, product name, or term worth noticing?
  → use <b>

Is the text a warning, critical instruction, or urgent information?
  → use <strong>

Do you just want bold styling with no semantic purpose?
  → use CSS font-weight: bold
```



# Description Lists in HTML

## What is a description list

- Used to present **key-value pairs** — a term/label and its related information
- Perfect for glossaries, dictionaries, FAQs, recipes, product specs, and metadata
- Any situation where one piece of information **labels** another

---

## The 3 elements

| Element | Role |
|---|---|
| `<dl>` | **Description list** — container for the entire list |
| `<dt>` | **Description term** — the label or key |
| `<dd>` | **Description details** — the value, definition, or related info |

---

## Basic syntax

```html
<dl>
  <dt>Term</dt>
  <dd>Details or definition for the term</dd>
</dl>
```

> By default, `<dd>` is indented to the right to visually separate it from `<dt>`.

---

## Example — glossary

```html
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language</dd>

  <dt>CSS</dt>
  <dd>Cascading Style Sheets</dd>

  <dt>JS</dt>
  <dd>JavaScript</dd>
</dl>
```

---

## Example — recipe ingredients

```html
<dl>
  <dt>Flour</dt>
  <dd>2 cups</dd>

  <dt>Sugar</dt>
  <dd>1/2 cup</dd>

  <dt>Vegetable Oil</dt>
  <dd>2 tablespoons</dd>
</dl>
```

---

## When to use description lists

Use a `<dl>` whenever you have content in **key-value pair format**:

| Use case | Key (`<dt>`) | Value (`<dd>`) |
|---|---|---|
| Glossary / dictionary | Term | Definition |
| Recipe | Ingredient | Amount |
| Product specs | Spec name | Spec value |
| FAQ | Question | Answer |
| Contact info | Label (e.g. Phone) | Value |
| Metadata | Property name | Property value |

---

## Quick rule

```
Do you have two related pieces of information where one labels the other?
  → use a description list <dl>
```


# Block and Inline Quotes in HTML

## Two types of quotes

| | `<blockquote>` | `<q>` |
|---|---|---|
| **Use for** | Extended quotations from another source | Short inline quotations within a paragraph |
| **Display** | Indented block — visually separate from content | Inline — part of the surrounding text |
| **Quotation marks** | Must be written manually if needed | Added automatically by most browsers |
| **`cite` attribute** | Yes | Yes |

---

## `<blockquote>` — block quotation

For **long, extended quotes** from another source:

```html
<blockquote cite="https://www.example.com/source">
  "Can you imagine what it would be like to be a successful developer?"
</blockquote>
```

### Multiple paragraphs in one block quote

```html
<blockquote cite="https://www.example.com/source">
  <p>Build your projects. Show them to your friends.</p>
  <p>Build your network. Help the people you meet along the way.</p>
  <p>It is not too late. Life is long.</p>
</blockquote>
```

> Wrapping paragraphs inside one `<blockquote>` keeps them as part of the same quotation.

---

## The `cite` attribute vs the `<cite>` element

These are two different things:

| | `cite` attribute | `<cite>` element |
|---|---|---|
| **Type** | HTML attribute | HTML element |
| **Used on** | `<blockquote>`, `<q>` | Standalone — wraps the title of a work |
| **Visible to user** | No — works behind the scenes | Yes — displayed on the page |
| **Purpose** | Gives screen readers and search engines source info | Marks up the title of a book, article, film, song, etc. |

### Attributing a source visually with `<cite>`

```html
<div>
  <blockquote cite="https://www.example.com/source">
    Can you imagine what it would be like to be a successful developer?
  </blockquote>
  <p>—Quincy Larson, <cite>How to Learn to Code and Get a Developer Job.</cite></p>
</div>
```

---

## `<q>` — inline quotation

For **short quotes** that sit within a larger paragraph:

```html
<p>
  As Quincy Larson said,
  <q cite="https://www.example.com/source">Momentum is everything.</q>
</p>
```

> Most modern browsers automatically add quotation marks around `<q>` content.

---

## Quick decision guide

```
Is the quote long and from an external source?
  → use <blockquote>

Is the quote short and part of an existing paragraph?
  → use <q>

Do you want to visually credit the source or title of a work?
  → use <cite> element

Do you want to provide source info to screen readers and search engines only?
  → use the cite attribute
```


# Abbreviations in HTML

## Types of abbreviations

| Type | Definition | Pronounced | Example |
|---|---|---|---|
| **Acronym** | Letters form a pronounceable word | As a word | `GUI` → Graphical User Interface |
| **Initialism** | Letters spell out individually | Letter by letter | `HTML` → HyperText Markup Language |

> Both are types of abbreviations — the distinction is in how they are spoken.

---

## The `<abbr>` element

Used to mark up abbreviations, acronyms, and initialisms in HTML:

```html
<p><abbr>HTML</abbr> is the foundation of the web.</p>
```

> Without any attributes, `<abbr>` provides context behind the scenes but looks like normal text.

---

## The `title` attribute

Optional — provides the full expanded form as a **tooltip** on hover:

```html
<p>
  <abbr title="HyperText Markup Language">HTML</abbr> is the foundation of the web.
</p>
```

- Value must be a **human-readable** description of the abbreviation
- Most browsers display a **dotted underline** or **small caps** when `title` is present
- Hovering over the element shows the full form as a tooltip

---

## More examples

```html
<p>
  The <abbr title="Graphical User Interface">GUI</abbr> makes software easier to use.
</p>

<p>
  She has a <abbr title="Doctor of Philosophy">PhD</abbr> in computer science.
</p>

<p>
  We use <abbr title="Cascading Style Sheets">CSS</abbr> to style web pages.
</p>
```

---

## When to use `<abbr>`

- When the abbreviation might be **unclear** to the reader
- When it needs **additional context** to be understood
- When it appears **for the first time** — always explain the full meaning on first use

> You don't need to wrap every abbreviation — use your judgement to keep text clear without cluttering it.


# Displaying Addresses in HTML

## The `<address>` element

- A **semantic element** for representing contact information
- Use instead of a generic `<div>` for contact sections
- Versatile — works for business pages, author pages, personal sites, and more

---

## Full example

```html
<address>
  <h2>Company Name</h2>
  <p>
    1234 Elm Street<br />
    Springfield, IL 62701<br />
    United States
  </p>
  <p>Phone: <a href="tel:+15555555555">+1 (555) 555-5555</a></p>
  <p>Email: <a href="mailto:contact@company.com">contact@company.com</a></p>
</address>
```

---

## Key elements used inside `<address>`

### `<br />` — line break
Used to separate lines within a physical address without creating a new paragraph:

```html
<p>
  1234 Elm Street<br />
  Springfield, IL 62701<br />
  United States
</p>
```

### `tel:` link — clickable phone number
Creates a link that initiates a phone call on supported devices:

```html
<a href="tel:+15555555555">+1 (555) 555-5555</a>
```

### `mailto:` link — clickable email address
Opens the user's default email client with a new message:

```html
<a href="mailto:contact@company.com">contact@company.com</a>
```

> ⚠️ `mailto:` links are often associated with spam — use with caution.

---

## Why use `<address>` over `<div>`

| | `<div>` | `<address>` |
|---|---|---|
| **Semantic meaning** | None | Clearly marks contact information |
| **Accessibility** | Screen readers treat it as generic content | Screen readers identify it as contact info |
| **SEO** | No signal | Helps search engines understand the content |



# Displaying Times and Dates in HTML

## The `<time>` element

- Used to represent a **specific moment in time**
- The `datetime` attribute translates it into a **machine-readable format**
- Helps with search engine results and browser processing of date/time info

---

## The `datetime` attribute

The value must be one of:

| Format | Example |
|---|---|
| Valid year | `2024` |
| Valid month | `2024-06` |
| Valid date | `2024-06-15` |
| Valid time | `20:00` |
| Date + time (ISO 8601) | `2024-06-15T15:00` |
| Duration | `PT2H30M` (2 hours 30 min) |

---

## Examples

### Time only

```html
<p>The reservations are for <time datetime="20:00">20:00</time>.</p>
```

### Date + time (ISO 8601)

```html
<p>The graduation will be on <time datetime="2024-06-15T15:00">June 15</time>.</p>
```

### ISO 8601 format breakdown

```
2024  -  06  -  15  T  15:00
 │        │      │  │    │
year   month   day  │   time (15:00 = 3 PM)
                    │
             separator between date and time
```

---

## Why use `<time>`

- Helps **search engines** understand event dates and publication times
- Allows **browsers** to process date/time info more effectively
- Improves **accessibility** for screen readers

---

## When to use `<time>`

- Events and appointments
- Publication dates
- Schedules and reservations

```html
<!-- event -->
<p>The concert starts at <time datetime="2024-09-21T19:30">7:30 PM on September 21</time>.</p>

<!-- publication date -->
<p>Published on <time datetime="2024-01-10">January 10, 2024</time>.</p>
```

# Superscript and Subscript in HTML

## The two elements

| Element | Name | Position | Use for |
|---|---|---|---|
| `<sup>` | Superscript | **Above** the normal text line | Exponents, abbreviations, ordinal numbers |
| `<sub>` | Subscript | **Below** the normal text line | Chemical formulas, footnotes, variable subscripts |

---

## `<sup>` — superscript

Text displayed **raised** above the baseline, in smaller size:

### Exponents

```html
<p>2<sup>2</sup> (2 squared) is 4.</p>
<p>The speed of light is approximately 3 × 10<sup>8</sup> m/s.</p>
```

### Superior lettering (abbreviations)

```html
<p>Monseigneur is often written as <strong>M<sup>gr</sup></strong>.</p>
```

### Ordinal numbers

```html
<p>She finished in 1<sup>st</sup> place.</p>
<p>It's on the 2<sup>nd</sup> floor.</p>
```

---

## `<sub>` — subscript

Text displayed **lowered** below the baseline, in smaller size:

### Chemical formulas

```html
<p>CO<sub>2</sub></p>               <!-- Carbon dioxide -->
<p>H<sub>2</sub>O</p>              <!-- Water -->
<p>H<sub>2</sub>SO<sub>4</sub></p> <!-- Sulphuric acid -->
```

### Footnotes

```html
<p>This claim is disputed.<sub>1</sub></p>
```

### Variable subscripts (maths)

```html
<p>The variable x<sub>1</sub> represents the first value.</p>
```

---

## Important rule

Both elements should only be used for **typographical reasons** — when the raised or lowered text is part of the meaning (maths, chemistry, abbreviations).

```
Do you need raised/lowered text for semantic reasons (exponents, formulas)?
  → use <sup> or <sub>

Do you just want visually raised/lowered text for styling?
  → use CSS vertical-align and font-size
```



# Representing Code in HTML

## The two elements

| Element | Purpose | Displays |
|---|---|---|
| `<code>` | Short inline code snippets | Monospaced font, inline |
| `<pre>` | Preformatted text block | Preserves whitespace and indentation exactly as written |

---

## `<code>` — inline code

For **short, single-line** code snippets within text:

```html
<p>
  To set the text color to blue in CSS, use the following code:
  <code>color: blue;</code>
</p>
```

- Browser applies **monospaced font** by default
- Communicates to the browser that the content is a code snippet

---

## `<pre>` + `<code>` — multi-line code blocks

For **longer, multi-line** code snippets:

```html
<pre>
  <code>
    body {
      color: red;
    }
  </code>
</pre>
```

> ⚠️ `<pre>` preserves **all whitespace and indentation** exactly as written in the HTML — be mindful of spacing.

---

## More examples

### Inline — referencing an HTML element

```html
<p>Use the <code>&lt;img&gt;</code> element to add images to your page.</p>
```

### Block — JavaScript function

```html
<pre>
  <code>
    function greet(name) {
      return "Hello, " + name;
    }
  </code>
</pre>
```

---

## Quick decision guide

```
Is it a short snippet within a sentence?
  → use <code>

Is it multiple lines that need preserved formatting?
  → use <pre> wrapping <code>
```



# The `<u>`, `<s>`, and `<ruby>` Elements

## Quick overview

| Element | Name | Purpose |
|---|---|---|
| `<u>` | Unarticulated annotation | Marks text with non-textual annotation (e.g. spelling errors) |
| `<s>` | Strikethrough | Marks text that is no longer accurate or relevant |
| `<ruby>` | Ruby | Shows small annotation text above/below main text (e.g. pronunciation) |

---

## `<u>` — unarticulated annotation

Used for inline text that has **non-textual annotation** applied — most commonly spelling errors:

```html
<p>
  You can use this element to highlight
  <u>inccccort</u> <u>spling</u> <u>issses</u>.
</p>
```

- Default style: **black underline** beneath the text
- In HTML4 it was used for visual underlining — in **HTML5 it is semantic only**

> To underline text for styling purposes only, use CSS `text-decoration: underline` instead.

---

## `<s>` — strikethrough

Used when text is **no longer accurate or relevant**:

```html
<p><s>Tomorrow's hike will be meeting at noon.</s></p>
<p>Due to unforeseen weather conditions, the hike has been canceled.</p>
```

- Default style: **horizontal line through** the text
- Should **not** be used to show document edits or tracked changes

> For document changes use `<del>` (deleted text) and `<ins>` (inserted text) instead.

---

## `<ruby>` — ruby annotation

Shows **small annotation text** above or below the main text. Most commonly used for pronunciation of East Asian characters:

```html
<ruby>
  明日
  <rp>(</rp>
  <rt>Ashita</rt>
  <rp>)</rp>
</ruby>
```

### Elements used with `<ruby>`

| Element | Name | Purpose |
|---|---|---|
| `<rt>` | Ruby text | The annotation text — pronunciation or translation |
| `<rp>` | Ruby fallback parenthesis | Shown as fallback in browsers that don't support ruby |

---

## Key rules

```
Need to flag a spelling error or non-textual annotation?
  → use <u>

Need to show text that is no longer accurate or relevant?
  → use <s>

Need to show document edits (additions/deletions)?
  → use <ins> and <del> instead of <s>

Need to add pronunciation or translation above East Asian characters?
  → use <ruby> with <rt> and <rp>

Just want visual underlining or strikethrough for styling?
  → use CSS text-decoration
```

# Semantic HTML Review

## Why semantic HTML matters

- **Accessibility** — screen readers use semantic meaning to describe content
- **SEO** — search engines better understand and rank your content
- **Maintainability** — code is easier to read and navigate
- Use **CSS** for visual styling — not presentational HTML elements

---

## Structural hierarchy

- `<h1>` is the highest level, `<h6>` the lowest
- Never skip heading levels (e.g. `h1` → `h3`)
- Only one `<h1>` per page

---

## Semantic vs presentational

| Type | Examples | Status |
|---|---|---|
| Presentational | `<center>`, `<big>`, `<font>` | Deprecated — avoid |
| Semantic | `<header>`, `<nav>`, `<figure>` | Recommended |

---

## Semantic layout elements

### `<header>` — document or section header
```html
<header>
  <h1>CatPhotoApp</h1>
  <p>Welcome to our cat gallery.</p>
</header>
```

### `<main>` — main page content
```html
<main>
  <section>
    <h2>Cat Photos</h2>
  </section>
</main>
```

### `<section>` — thematic content group
```html
<section>
  <h2>About Me</h2>
  <p>Hi, I am Jane Doe.</p>
</section>
```

### `<nav>` — navigation links
```html
<nav>
  <ul>
    <li><a href="#photos">Photos</a></li>
    <li><a href="#videos">Videos</a></li>
  </ul>
</nav>
```

### `<figure>` + `<figcaption>` — image with caption
```html
<figure>
  <img src="cats.jpg" alt="Two tabby kittens sleeping." />
  <figcaption>Cats <strong>hate</strong> other cats.</figcaption>
</figure>
```

---

## Text-level semantic elements

### Emphasis and importance

| Element | Name | Purpose | Default style |
|---|---|---|---|
| `<em>` | Emphasis | Stress emphasis that changes meaning | Italic |
| `<i>` | Idiomatic text | Foreign terms, technical terms, alternative voice | Italic |
| `<strong>` | Strong importance | Urgent or critical information | Bold |
| `<b>` | Bring attention to | Keywords, product names — no added importance | Bold |

```html
<p>Never give up on <em>your</em> dreams.</p>
<p>There is a certain <i lang="fr">je ne sais quoi</i> in the air.</p>
<p><strong>Warning:</strong> This product may cause allergic reactions.</p>
<p>We tested the <b>SuperSound 3000</b> and the <b>QuickCharge Pro</b>.</p>
```

---

### Lists

#### Description list — key-value pairs
```html
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language</dd>
  <dt>CSS</dt>
  <dd>Cascading Style Sheets</dd>
</dl>
```

---

### Quotations

| Element | Use for |
|---|---|
| `<blockquote cite="">` | Extended quotes from another source |
| `<q cite="">` | Short inline quotes |
| `<cite>` | Title of a referenced work — visible to user |

```html
<!-- block quote with visible attribution -->
<blockquote cite="https://www.example.com">
  "Can you imagine what it would be like to be a successful developer?"
</blockquote>
<p>—Quincy Larson, <cite>How to Learn to Code and Get a Developer Job.</cite></p>

<!-- inline quote -->
<p>As Quincy Larson said, <q cite="https://www.example.com">Momentum is everything.</q></p>
```

---

### Abbreviations
```html
<p><abbr title="HyperText Markup Language">HTML</abbr> is the foundation of the web.</p>
```

---

### Contact address
```html
<address>
  <p>1234 Elm Street<br />Springfield, IL</p>
  <p><a href="mailto:contact@company.com">contact@company.com</a></p>
</address>
```

---

### Date and time
```html
<p>The reservations are for <time datetime="20:00">20:00</time>.</p>
<p>The event is on <time datetime="2024-06-15T15:00">June 15 at 3 PM</time>.</p>
```

> ISO 8601 format: `YYYY-MM-DDThh:mm:ss` — `T` separates date from time.

---

### Superscript and subscript

```html
<p>2<sup>2</sup> is 4.</p>          <!-- exponent -->
<p>She came 1<sup>st</sup>.</p>     <!-- ordinal -->
<p>CO<sub>2</sub></p>               <!-- chemical formula -->
```

---

### Code

```html
<!-- inline -->
<p>Use <code>color: blue;</code> to set the text colour.</p>

<!-- multi-line block -->
<pre>
  <code>
    body {
      color: red;
    }
  </code>
</pre>
```

---

### Annotation elements

| Element | Purpose | Default style |
|---|---|---|
| `<u>` | Non-textual annotation (e.g. spelling errors) | Underline |
| `<s>` | No longer accurate or relevant | Strikethrough |
| `<ruby>` | Pronunciation/meaning for East Asian text | Annotation above |

```html
<p>Fix the <u>spling</u> errors.</p>
<p><s>The hike is at noon.</s> The hike has been canceled.</p>
<ruby>明日 <rp>(</rp><rt>Ashita</rt><rp>)</rp></ruby>
```

---

### Internal links

Link to another section on the same page using `href="#id"`:

```html
<a href="#about-section">Go to About Section</a>

<section id="about-section">
  <h2>About</h2>
  <p>This is the about section.</p>
</section>
```

> Common uses: skip links, table of contents, long pages with multiple sections.


# Forms, Labels, and Inputs in HTML

## The `<form>` element

Container for all form inputs. The `action` attribute specifies where the data is sent on submission:

```html
<form action="url-goes-here">
  <!-- inputs go here -->
</form>
```

---

## The `<input>` element

- Void element — **no closing tag**
- The `type` attribute defines what kind of data is expected

```html
<input type="text" />
```

### Common `type` values

| Type | Purpose |
|---|---|
| `text` | Plain text input |
| `email` | Email address — includes basic format validation |
| `password` | Hidden text input |
| `checkbox` | Checkbox |
| `radio` | Radio button |
| `number` | Numeric input |
| `submit` | Submit button |

---

## The `<label>` element

Associates a text description with an input. Clicking the label focuses the input.

### Implicit association — nest `<input>` inside `<label>`

```html
<form action="">
  <label>
    Full Name:
    <input type="text" />
  </label>
</form>
```

### Explicit association — use `for` and `id`

The `for` value on `<label>` must match the `id` value on `<input>`:

```html
<form action="">
  <label for="email">Email Address:</label>
  <input type="email" id="email" />
</form>
```

---

## The `placeholder` attribute

Shows hint text inside the input before the user types. Disappears on focus:

```html
<form action="">
  <label for="email">Email Address:</label>
  <input type="email" id="email" placeholder="example@email.com" />
</form>
```

> Keep placeholder text short and representative of the expected format.

---

## Putting it all together

```html
<form action="/submit">
  <label>
    Full Name:
    <input type="text" placeholder="Jane Doe" />
  </label>

  <label for="email">Email Address:</label>
  <input type="email" id="email" placeholder="jane@example.com" />
</form>
```

---

## Implicit vs explicit association

| | Implicit | Explicit |
|---|---|---|
| **How** | Nest `<input>` inside `<label>` | Match `for` on label with `id` on input |
| **Extra attributes needed** | No | Yes — `for` and `id` |
| **When to use** | Simple, compact forms | When label and input are not nested |

# Button Types in HTML

## The `<button>` element

Used to perform an action when activated — submitting a form, showing a modal, toggling a menu, etc.:

```html
<button>Start Game</button>
```

---

## The `type` attribute

Controls the button's behaviour when clicked:

| Value | Behaviour |
|---|---|
| `button` | Does nothing by default — behaviour added via JavaScript |
| `submit` | Submits the form data to the server |
| `reset` | Clears all input data in the form |

---

## `type="button"` — general purpose

Does nothing on its own — use JavaScript to add interactivity:

```html
<button type="button">Show Alert</button>
```

---

## `type="submit"` — form submission

Sends the form data to the server when clicked:

```html
<form action="">
  <label for="email">Email address:</label>
  <input type="email" id="email" name="email" />
  <button type="submit">Submit form</button>
</form>
```

---

## `type="reset"` — clear form

Clears all user input in the form when clicked:

```html
<form action="">
  <label for="email">Email address:</label>
  <input type="email" id="email" name="email" />
  <button type="reset">Reset form</button>
  <button type="submit">Submit form</button>
</form>
```

> ⚠️ Reset buttons are generally not recommended — users can accidentally clear their data. Multiple buttons can also clutter the UI.

---

## Using `<input>` as a button

The `<input>` element can also create buttons using `type="button"`, `type="submit"`, or `type="reset"`. The button label is set with the `value` attribute:

```html
<input type="button" value="Start Game" />
<input type="submit" value="Submit form" />
<input type="reset" value="Reset form" />
```

---

## `<button>` vs `<input>` for buttons

| | `<input type="button">` | `<button>` |
|---|---|---|
| **Void element** | Yes — no closing tag, no children | No — has opening and closing tags |
| **Can contain children** | No — text only via `value` attribute | Yes — text, images, icons |
| **Flexibility** | Limited | More flexible |

```html
<!-- input — text only -->
<input type="button" value="Start Game" />

<!-- button — can contain icons and text -->
<button type="button">
  <img src="icon.svg" alt="" /> Start Game
</button>
```

> Prefer `<button>` over `<input>` for buttons — it is more flexible and easier to style.



# Client-Side Form Validation in HTML

## Key concepts

| Term | Definition |
|---|---|
| **Client-side** | Everything that happens on the user's device — layout, design, interactive features |
| **Server-side** | Everything that happens on the server — processing data, handling requests |
| **Client-side validation** | Checks user input before it is sent to the server |

> ⚠️ Client-side validation is not enough on its own — malicious users can bypass it. Always add server-side validation too.

---

## The `required` attribute

Prevents form submission if the field is empty:

```html
<form action="">
  <label for="email">Email Address (Required):</label>
  <input required type="email" name="email" id="email" />
  <button type="submit">Submit Form</button>
</form>
```

> Each browser displays its own style of alert message when validation fails.

---

## Built-in email validation

The `type="email"` input automatically checks for basic email format (e.g. requires `@`):

```html
<input required type="email" name="email" id="email" />
```

- Typing `abc` and submitting → browser alerts that `@` is missing
- Basic format only — additional validation must be added manually

---

## `minlength` and `maxlength` attributes

Set minimum and maximum character length for the input:

```html
<form action="">
  <label for="email">Email Address (Required):</label>
  <input
    required
    type="email"
    name="email"
    id="email"
    minlength="4"
    maxlength="64"
  />
  <button type="submit">Submit Form</button>
</form>
```

| Attribute | Purpose |
|---|---|
| `minlength` | Minimum number of characters required |
| `maxlength` | Maximum number of characters allowed |

> Submitting `b@m` (3 characters) with `minlength="4"` triggers an alert — too short.

---

## Common validation attributes — quick reference

| Attribute | Works on | Purpose |
|---|---|---|
| `required` | All inputs | Field must not be empty |
| `type="email"` | `<input>` | Enforces basic email format |
| `minlength` | Text-based inputs | Minimum character count |
| `maxlength` | Text-based inputs | Maximum character count |
| `min` | Number, date inputs | Minimum value |
| `max` | Number, date inputs | Maximum value |
| `pattern` | Text-based inputs | Custom regex validation |




# Form States in HTML

## The 4 main form states

| State | How it's triggered | Can be focused | User can edit |
|---|---|---|---|
| `default` | Page loads | Yes | Yes |
| `focused` | Click or `Tab` key | Yes | Yes |
| `disabled` | `disabled` attribute | No | No |
| `readonly` | `readonly` attribute | Yes | No |

---

## Default state

The input as it appears when first rendered on the page — blank and interactive:

```html
<input type="email" name="email" id="email" />
```

---

## Focused state

Active when the user clicks the input or selects it with the `Tab` key. Most browsers show a **blue highlighted border** by default:

```html
<input type="email" name="email" id="email" />
```

> Additional focus styles can be added with CSS.

---

## Disabled state

The input **cannot be focused or activated** by the user:

```html
<input disabled type="email" name="email" id="email" />
```

- User cannot click or tab into it
- Visually appears greyed out in most browsers
- Additional styles can be set with CSS

---

## Readonly state

The input **can be focused but not edited**. Use the `value` attribute to set the displayed value:

```html
<input
  readonly
  type="email"
  name="email"
  id="email"
  value="example@email.com"
/>
```

- User can see and copy the value
- User cannot change it

---

## `disabled` vs `readonly`

| | `disabled` | `readonly` |
|---|---|---|
| Can be focused | No | Yes |
| Can be edited | No | No |
| Value submitted with form | No | Yes |
| Visual indication | Greyed out | Normal appearance |

---

## Why form states matter

- Give users **clear feedback** about what they can and cannot interact with
- Help **prevent errors** by guiding users through the form
- Improve the overall **user experience** and accessibility



# HTML Tables

## What tables are for

- Displaying **tabular data** — structured information in rows and columns
- Examples: statistics, schedules, pricing, comparisons

> ⚠️ Do not use tables for page layout — use CSS Flexbox or Grid instead.

---

## Table element hierarchy

```
<table>
├── <thead>   — table header section
│   └── <tr>  — table row
│       └── <th>  — header cell
├── <tbody>   — table body section
│   └── <tr>  — table row
│       ├── <th>  — row header cell
│       └── <td>  — data cell
└── <tfoot>   — table footer section
    └── <tr>  — table row
        └── <th>  — footer cell
```

---

## Element reference

| Element | Name | Purpose |
|---|---|---|
| `<table>` | Table | Container for the entire table |
| `<thead>` | Table head | Groups the header rows |
| `<tbody>` | Table body | Groups the main data rows |
| `<tfoot>` | Table foot | Groups the footer rows (meta info, totals) |
| `<tr>` | Table row | A single row — used inside thead, tbody, tfoot |
| `<th>` | Table header | A header cell — labels a row or column |
| `<td>` | Table data | A data cell — contains the actual data |

---

## Minimal table example

```html
<table>
  <thead>
    <tr>
      <th>Title of this table</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>First Row</th>
      <td>First Data Cell</td>
    </tr>
    <tr>
      <th>Second Row</th>
      <td>Second Data Cell</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th>Footer — publication date, author credits, or other meta info.</th>
    </tr>
  </tfoot>
</table>
```

---

## Real-world example — Bureau of Labor Statistics

```html
<table id="quickfacts">
  <thead>
    <tr>
      <th colspan="2">Quick Facts: Software Developers</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2023 Median Pay</th>
      <td>$130,160 per year<br />$62.58 per hour</td>
    </tr>
    <tr>
      <th>Typical Entry-Level Education</th>
      <td>Bachelor's degree</td>
    </tr>
    <tr>
      <th>Job Outlook, 2022-32</th>
      <td>25% (Much faster than average)</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th>Source: U.S. Bureau of Labor Statistics</th>
    </tr>
  </tfoot>
</table>
```

> `colspan="2"` spans a cell across 2 columns.

---

## Tables — do and don't

| ✅ Use tables for | ⚠️ Do not use tables for |
|---|---|
| Statistical data | Page layout |
| Schedules and timetables | Positioning non-data elements |
| Pricing or comparison grids | Navigation menus |
| Structured key-value data | General content arrangement |

> For layout, use **CSS Flexbox** or **CSS Grid** instead.


# HTML Validators

## Why validation matters

- HTML is **forgiving** — browsers try to render code even with errors
- A missing closing tag may still render, but can cause **unexpected behaviour**

### Example of a silent error

```html
<!-- missing closing </h2> tag -->
<h2>Subheading 3
<p>This paragraph renders as an h2 — not the intended result.</p>
```

> The browser's parsing algorithm fills in the gap, but not always the way you intended.

---

## What is an HTML validator

- A tool that checks your HTML against **official HTML specifications**
- Identifies **errors and warnings** in your code
- Ensures your pages are **correctly structured** and compliant with web standards

---

## Who benefits from validation

- **You** — catch bugs before they cause visual or functional issues
- **Teammates** — easier to review and understand clean, valid code
- **Open-source contributors** — consistent, standards-compliant codebase

---

## Recommended validators

### W3C Markup Validation Service
The most widely accepted HTML validator:

```
https://validator.w3.org
```

1. Visit the site
2. Click **Validate by Direct Input**
3. Paste your HTML code
4. Click **Check**
5. Review the list of errors and warnings

---

### JSON Formatter HTML Validator

```
https://jsonformatter.org
```

1. Paste your HTML into the editor
2. Click **Validate**
3. Review any errors shown

---

## Common errors validators catch

- Missing closing tags
- Incorrect nesting of elements
- Deprecated elements or attributes
- Missing required attributes (e.g. `alt` on `<img>`)
- Incorrect document structure (e.g. elements outside `<body>`)

---

## Quick habit

> Always run your HTML through a validator before considering a project complete — it takes seconds and can save hours of debugging.




# DOM Inspector and DevTools for Debugging

## Key concepts

| Term | Definition |
|---|---|
| **Bug** | An issue that causes a program to not work as expected |
| **Debugging** | The process of finding and fixing bugs |
| **DOM** | Document Object Model — a tree-like structure representing all elements on a page |
| **DOM Inspector** | Tool to inspect and explore the HTML structure of a page |
| **DevTools** | Browser tools to inspect and debug HTML, CSS, and JavaScript |

---

## How to open DevTools

| Method | Shortcut |
|---|---|
| Right-click on the page | Select **Inspect** |
| PC keyboard | `Ctrl` + `Shift` + `I` |
| Mac keyboard | `Cmd` + `Option` + `I` |

---

## Key DevTools tabs

| Tab | Purpose |
|---|---|
| **Elements** | Shows the full HTML structure of the page (DOM inspector) |
| **Console** | Shows errors, warnings, and logs occurring on the page |

---

## Example — debugging a broken link

```html
<!-- bug: typo in the URL — /larn instead of /learn -->
<a href="https://www.freecodecamp.org/larn/">freeCodeCamp curriculum</a>
```

### Debugging steps

1. Click the link → lands on a **404 page** (page not found)
2. Open DevTools → go to the **Console** tab
3. Look for the **404 error message** — it shows `/larn` as the failing URL
4. Go to the **Elements** tab → inspect the `href` attribute
5. Spot the typo: `/larn` → fix to `/learn`

```html
<!-- fixed -->
<a href="https://www.freecodecamp.org/learn/">freeCodeCamp curriculum</a>
```

---

## What a 404 error means

- The server **cannot find the requested page**
- Common causes: typo in the URL, moved or deleted page, incorrect path

---

## Quick debugging habit

```
Something not working as expected?
  1. Open DevTools (Ctrl/Cmd + Shift + I)
  2. Check the Console tab for errors
  3. Check the Elements tab for incorrect HTML
  4. Fix the issue and verify in the preview
```



# HTML Tables and Forms Review

## Form elements and attributes

### `<form>`
```html
<form method="POST" action="url-goes-here">
  <!-- inputs go here -->
</form>
```

| Attribute | Purpose |
|---|---|
| `action` | URL where form data is sent on submission |
| `method` | HTTP method — `GET` or `POST` |

---

### `<input>` — input field

| Attribute | Purpose |
|---|---|
| `type` | Type of input — `text`, `email`, `number`, `radio`, `checkbox`, etc. |
| `placeholder` | Hint text shown before the user types |
| `value` | Pre-set value — also sets button text for `type="button"` |
| `name` | Key used when form data is submitted — groups radio buttons |
| `size` | Number of visible characters in the field |
| `min` / `max` | Minimum/maximum value for number inputs |
| `minlength` / `maxlength` | Minimum/maximum character count |
| `required` | Field must be filled before submission |
| `disabled` | Field cannot be interacted with |
| `readonly` | Field is visible and focusable but not editable |

```html
<!-- text input -->
<input type="text" id="name" name="name" placeholder="e.g. Quincy Larson"
  size="20" minlength="5" maxlength="30" required />

<!-- number input -->
<input type="number" id="quantity" name="quantity" min="2" max="10" disabled />

<!-- button via input -->
<input type="button" value="Show Alert" />
```

---

### `<label>` — input label

| Association | How |
|---|---|
| Implicit | Nest `<input>` inside `<label>` |
| Explicit | Match `for` on `<label>` with `id` on `<input>` |

```html
<!-- implicit -->
<label>
  Full Name:
  <input type="text" />
</label>

<!-- explicit -->
<label for="email">Email Address:</label>
<input type="email" id="email" />
```

---

### `<button>` — clickable button

```html
<button type="button">Show Form</button>   <!-- no default action -->
<button type="submit">Submit Form</button> <!-- submits the form -->
<button type="reset">Reset Form</button>   <!-- clears all inputs -->
```

---

### `<fieldset>` and `<legend>` — grouping inputs

```html
<!-- radio group -->
<fieldset>
  <legend>Was this your first time at our hotel?</legend>
  <label for="yes-option">Yes</label>
  <input id="yes-option" type="radio" name="hotel-stay" value="yes" />
  <label for="no-option">No</label>
  <input id="no-option" type="radio" name="hotel-stay" value="no" />
</fieldset>

<!-- checkbox group -->
<fieldset>
  <legend>Why did you choose to stay at our hotel?</legend>
  <label for="location">Location</label>
  <input type="checkbox" id="location" name="location" value="location" />
  <label for="price">Price</label>
  <input type="checkbox" id="price" name="price" value="price" />
</fieldset>
```

| Element | Purpose |
|---|---|
| `<fieldset>` | Groups related inputs together |
| `<legend>` | Caption describing the group |

---

## Form states

| State | Triggered by | Can focus | Can edit |
|---|---|---|---|
| Default | Page load | Yes | Yes |
| Focused | Click or `Tab` key | Yes | Yes |
| Disabled | `disabled` attribute | No | No |
| Readonly | `readonly` attribute | Yes | No |

---

## Table elements and attributes

### Element reference

| Element | Purpose |
|---|---|
| `<table>` | Container for the entire table |
| `<caption>` | Title shown above the table |
| `<thead>` | Groups header rows |
| `<tbody>` | Groups body/data rows |
| `<tfoot>` | Groups footer rows |
| `<tr>` | A single table row |
| `<th>` | Header cell — labels a row or column |
| `<td>` | Data cell — contains the actual data |

### `colspan` attribute
Spans a cell across multiple columns:

```html
<td colspan="2">Average Grade</td>
```

### Full table example

```html
<table>
  <caption>Exam Grades</caption>
  <thead>
    <tr>
      <th>Last Name</th>
      <th>First Name</th>
      <th>Grade</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Davis</td>
      <td>Alex</td>
      <td>54</td>
    </tr>
    <tr>
      <td>Doe</td>
      <td>Samantha</td>
      <td>92</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td colspan="2">Average Grade</td>
      <td>78</td>
    </tr>
  </tfoot>
</table>
```

---

## HTML tools

| Tool | Purpose |
|---|---|
| **HTML validator** | Checks HTML syntax against official standards — catches errors and warnings |
| **DOM inspector** | Inspect and explore the HTML structure of a live page |
| **DevTools** | Full browser toolkit — debug HTML, CSS, JavaScript, network requests, and more |

### Opening DevTools

| Method | Shortcut |
|---|---|
| Right-click page | Select **Inspect** |
| PC | `Ctrl` + `Shift` + `I` |
| Mac | `Cmd` + `Option` + `I` |

### Key DevTools tabs

| Tab | Purpose |
|---|---|
| **Elements** | View and edit the HTML/CSS of the page |
| **Console** | See errors, warnings, and logs |



# What Is Accessibility?

## Definition

Creating products and services that **everyone can use** — including people with disabilities.

In web development: making websites that everyone can **understand and interact with**.

---

## Disabilities that can affect online experience

- **Visual** — blindness, low vision, colour blindness
- **Auditory** — deafness
- **Motor** — difficulty using keyboards, mice, or touchscreens
- **Cognitive** — attention disorders, memory issues
- **Communication** — difficulty speaking or understanding spoken language
- **Neurological** — sensitivity to flashing lights

---

## WCAG — Web Content Accessibility Guidelines

Developed by the **World Wide Web Consortium (W3C)** — an international set of standards for accessible web content.

Built on four core principles: **POUR**

| Letter | Principle | What it means | Example |
|---|---|---|---|
| **P** | Perceivable | Users can perceive all information | Provide `alt` text for images |
| **O** | Operable | Users can interact with the interface | All functionality works with keyboard, not just mouse |
| **U** | Understandable | Users can understand the content | Use simple language, avoid complex sentences |
| **R** | Robust | Works across browsers and assistive technologies | Use semantic HTML |

> If your content fails **any one** of these principles, not everyone will be able to use your website.

---

## How to check your accessibility

Visit the W3C Quick Reference for a full list of criteria and techniques:

```
https://www.w3.org/WAI/WCAG21/quickref/
```

---

## How semantic HTML helps accessibility

- Screen readers rely on semantic elements to **describe and navigate** content
- Semantic HTML ensures compatibility with a **wide range of browsers and assistive technologies**
- Supports the **Robust** principle of WCAG

---

## Why accessibility matters

- Promotes **equality** — ensures everyone can access and engage with your content
- Creates a **better user experience** for all users
- Is an **essential** part of professional web development


# Screen Readers

## What is a screen reader

- Assistive technology programs that help **blind and visually impaired** people use computers and mobile devices
- Also used by people with **dyslexia** and **cognitive disabilities**

---

## What screen readers do

> Common misconception: screen readers are just text-to-speech devices — they are much more.

| Feature | Description |
|---|---|
| **Text-to-speech** | Reads on-screen text aloud |
| **Braille output** | Renders text to a braille display instead of speech |
| **Navigation aids** | Helps users move through page structure (headings, links, landmarks) |
| **Web browsing assistance** | Interprets HTML structure to describe page content |

---

## Why screen readers matter

- Enable access to **education, work, and social media**
- Ensure **digital inclusion** for people who would otherwise be excluded
- Allow full participation in society

---

## Screen readers by platform

| Platform | Built-in screen reader | How to enable | Other options |
|---|---|---|---|
| **macOS** | VoiceOver | `Cmd` + `F5` | — |
| **iOS** | VoiceOver | Settings → Accessibility | — |
| **Windows** | Narrator | `Win` + `Ctrl` + `Enter` | NVDA (free, open-source), JAWS (paid) |
| **Linux** | Orca (desktop) | — | Speakup (terminal) |
| **Android** | TalkBack | Settings → Special Function → Accessibility → TalkBack | Ella, Select to Speak |

---

## The developer's responsibility

- Many developers do **not design with screen reader accessibility in mind** — a major challenge for users
- Every developer should learn how to make their web software **accessible for all users**
- Good accessibility demonstrates **empathy and a commitment to inclusivity**

---

## How to support screen readers in HTML

- Use **semantic HTML** — screen readers rely on element meaning to navigate content
- Always include `alt` text on images
- Use proper **heading hierarchy** (`h1` → `h2` → `h3`)
- Associate `<label>` with every `<input>`
- Ensure all functionality works with **keyboard navigation**




# Large Text and Braille Keyboards

## Who uses them

People with **visual disabilities** — from low vision to complete blindness.

---

## Large Text Keyboards (Large Print Keyboards)

Designed for users with **low vision** who can still see but struggle with standard key sizes:

| Feature | Purpose |
|---|---|
| Larger letters, numbers, and symbols | Easier to see individual keys |
| Enhanced contrast | Improves visibility (e.g. yellow keys with black text) |
| Backlit keys | Adjustable brightness for different lighting conditions |

### Common examples

- **Yellow keys with black bold text** — high contrast for low vision users
- **Black keys with white text + backlit** — adjustable for different environments

---

## Braille Keyboards

Designed for users with **more severe visual disabilities**, including people who are blind.

### What is Braille

- A **tactile reading and writing system**
- Uses **raised dots** arranged in specific patterns to represent letters, numbers, and punctuation
- Read by feeling the patterns with fingertips

### How braille keyboards work

- Keys have **raised dot patterns** representing letters, numbers, and symbols
- Users identify keys by **touch** rather than sight
- Provides a completely **tactile experience**

---

## Combined keyboards

Some keyboards combine **both approaches** — large print fonts and braille dot patterns:

- Useful for people with visual disabilities who are **also learning braille**
- Serves a wider range of visual impairment levels

---

## Summary

| Keyboard type | Best for | Key feature |
|---|---|---|
| Large print | Low vision | Larger text, high contrast, backlit |
| Braille | Blind / severe visual impairment | Raised dot patterns on keys |
| Combined | Both / braille learners | Large text + braille dots |

---

## Why this matters for developers

- Accessible websites must work well with **alternative input methods**
- Ensure your UI is navigable by **keyboard alone** — not just mouse
- Clear, readable text and good colour contrast supports users of large print keyboards


# Alternative Pointing Devices

## What are they

Input devices that serve as alternatives to the traditional mouse — essential for improving **computer accessibility** for people with disabilities, forelimb impairments, and limited mobility.

---

## Trackball

A **stationary pointing device** with a large movable ball in a socket. The user moves the ball with their fingers, thumb, or palm to control the cursor — the device itself stays in place.

| Feature | Benefit |
|---|---|
| No surface movement required | Ideal for users with **mobility issues** |
| High precision control | Good for detailed work |
| Small footprint | Ideal for **limited desk space** |

> Some traditional mice have a trackball on the top or side — a good starting point for gradually switching.

---

## Joystick

A **lever-based pointing device** that pivots up, down, left, and right — primarily designed for games and industrial applications (machinery, cranes, flight simulators).

| Feature | Benefit |
|---|---|
| Large, deliberate movements | Beneficial for users with **tremors or unsteady hands** |
| Reduces repetitive motion | Ideal for users with **arthritis or carpal tunnel syndrome** |
| Precise directional control | Great for flight simulators, driving games, industrial machinery |

---

## Touchpad

A **flat, touch-sensitive surface** built into laptops and some keyboards. Users slide fingers across the surface to control the cursor.

| Feature | Benefit |
|---|---|
| Forelimb stays almost stationary | Ideal for users with **low arm or hand movement** |
| No arm movement needed | Suitable for **arthritis and joint pain** |
| Multi-touch gesture support | Pinch-to-zoom, two-finger scroll, tap-to-click, three-finger swipe |
| Built-in click buttons | Emulates right-click and left-click of a traditional mouse |

---

## Comparison

| Device | Movement style | Best for |
|---|---|---|
| **Trackball** | Finger/thumb rolls the ball | Mobility issues, limited desk space, high precision |
| **Joystick** | Lever pushed in a direction | Tremors, arthritis, directional control applications |
| **Touchpad** | Finger slides across surface | Low arm mobility, arthritis, general laptop use |

---

## Why this matters for developers

- Ensure all interactive elements are **reachable and usable without a mouse**
- Support **keyboard navigation** as a baseline
- Avoid interactions that require precise mouse movements — these can be difficult for alternative device users
- Test your UI with different input methods where possible



# Screen Magnifiers

## What are they

Tools that **enlarge text, graphics, and other elements** on a screen to help people with **low vision and visual impairments** access digital content.

- Most allow enlargement of **200% or more**
- Offer **customisable zoom percentages** and other settings
- Users navigate the magnified view with a **pointing device or keyboard**

---

## What screen magnifiers help with

| Use case | How magnifiers help |
|---|---|
| **Reading text** | Enlarges small fonts in documents, emails, and articles |
| **Web browsing** | Makes buttons, links, and interactive elements easier to locate and click |
| **Filling out forms** | Improves visibility of fields and labels |
| **General online activity** | Enables full participation without eye strain |

---

## Developer considerations for magnifier users

- Use **scalable fonts** so the page can be resized without breaking the layout
- Implement **responsive design** so the UI adapts to different screen sizes
- Use **high-contrast colour schemes** and allow customisable colours
- Keep the **navbar non-sticky and minimal** so it doesn't block content when magnified
- Use **real HTML text** instead of images of text
- Place **feedback and error messages directly next to** the element that triggered them

---

## Built-in magnifiers by platform

| Platform | Magnifier | How to enable |
|---|---|---|
| **macOS** | Zoom | Settings → Accessibility → Zoom → toggle keyboard shortcuts |
| **iOS** | Zoom | Settings → Accessibility → Zoom |
| **Android** | Magnification | Settings → Special Function → Accessibility → Magnification |
| **Windows** | Magnifier | Settings → Ease of Access → Magnifier |
| **Linux** | Zoom or Magnifier | Varies by distribution |

---

## Third-party screen magnifiers

| Tool | Platform |
|---|---|
| ZoomText | Windows |
| ClaroView | macOS, Windows |
| iZoom | Windows |
| Zoomify | macOS |
| LunarPlus | Windows |
| Loupe | macOS |

---

## Why this matters for developers

Screen magnifiers are widely used — designing with scalability, contrast, and responsive layout in mind ensures your content is accessible to users who depend on them.


# Voice Recognition Software

## What is it

Software that lets users **control computers and devices using their voice** instead of traditional input devices like keyboards and mice.

### What you can do with it

- Write emails and documents
- Browse the web
- Control smart home devices
- Issue commands to the operating system

---

## Who uses it

### People with disabilities

| Group | Condition |
|---|---|
| Visual impairments | Low vision, blindness |
| Mobility impairments | Limited use of hands/arms, arthritis, carpal tunnel syndrome |
| Injury recovery | Hand or arm injuries |
| Cognitive disorders | Memory issues, attention deficit disorders |
| Elderly users | Find voice commands easier than physical input |

### Other users (no disability)

- Law enforcement
- Gamers
- Drivers
- Busy professionals

---

## Why voice recognition matters for accessibility

- **Eliminates the need for physical interaction** with a device
- Gives people with disabilities **significant independence and control** over their environment
- Enables full participation in digital life — work, communication, browsing

---

## Voice recognition software by platform

| Platform | Built-in tool |
|---|---|
| **macOS / iOS** | Voice Control |
| **Android** | Voice Access |
| **Windows** | Windows Speech Recognition (called Voice Access in recent versions) |

### Third-party options

| Tool | Platform |
|---|---|
| **Dragon by Nuance** | Windows — one of the most popular professional tools |

---

## Why this matters for developers

- Ensure your web content is **navigable and operable by voice commands**
- Use **semantic HTML** and proper labels so voice tools can identify and interact with elements correctly
- Avoid interactions that require precise clicking — voice users often navigate by **element names and labels**


# Accessibility Auditing Tools

## What are they

Applications that **automatically detect accessibility issues** in websites, web apps, and mobile apps — helping developers meet accessibility standards.

> ⚠️ Automated tools typically find only about **one third** of all possible accessibility issues. Manual testing — preferably by people with disabilities — is always required.

---

## Google Lighthouse

A popular web metrics checker built into **Chrome DevTools** or available online.

### What it checks
- Accessibility
- SEO
- Best practices
- Performance

### How to use (DevTools version)
1. Open DevTools — press `F12`
2. Switch to the **Lighthouse** tab
3. Select the metrics to check
4. Choose the target device
5. Click **Analyse page load**
6. Review the accessibility score and list of issues

### Web version
```
https://pagespeed.web.dev
```
> More reliable metrics, but does **not support local websites**.

---

## WAVE

A reliable accessibility checker available as a **Chrome extension** or **web tool**.

### How to use
1. Enter the URL of your website
2. A comprehensive report is generated automatically

### What it reports
- Accessibility features implemented
- ARIA usage
- Colour contrast issues

---

## IBM Equal Accessibility Checker

A robust tool for scanning websites and generating **detailed accessibility reports**.

Available as a **Chrome extension** or **Firefox add-on**.

### How to use (Chrome extension)
1. Download from the Chrome Web Store
2. Open DevTools — press `F12`
3. Go to the **Accessibility Checker** tab in the Elements panel
4. Click **Scan**
5. Review the generated report
6. Export as spreadsheet or HTML via **Export XLS**

---

## Tool comparison

| Tool | Available as | Supports local sites | Export report |
|---|---|---|---|
| Google Lighthouse | DevTools tab, web | Yes (DevTools only) | No |
| WAVE | Chrome extension, web | No | No |
| IBM Equal Accessibility Checker | Chrome extension, Firefox add-on | Yes | Yes (XLS, HTML) |

---

## Key reminder

> A **perfect score** from any automated tool does **not** mean your content is fully accessible. Always complement automated testing with **manual testing by real users**, including people with disabilities.



# Heading Structure and Accessibility

## Why heading structure matters

- Creates a **visual hierarchy** for all users to navigate and understand a page
- Allows **screen reader users** to list all headings and jump directly to sections they need
- Reduces **cognitive load** for users with partial sight or cognitive disabilities
- Helps everyone find information quickly
- Well-formed headings can also improve **SEO**

---

## How screen readers use headings

Screen readers can **list all headings on a page** — users jump directly to the section they need without reading through all content. This makes correct heading order critical.

```html
<h1>I am an h1 heading</h1>
<h2>I am an h2 heading</h2>
<h3>I am an h3 heading</h3>
<h4>I am an h4 heading</h4>
<h5>I am an h5 heading</h5>
<h6>I am an h6 heading</h6>
```

---

## Best practices

- Use headings in a **logical hierarchy** — `h1` → `h2` → `h3`, and so on
- **Never skip levels** — don't jump from `h1` to `h3` or `h2` to `h4`
- Use **clear and descriptive text** that summarises the content that follows
- **Never use a heading in isolation** — content must follow every heading
- Use **actual heading elements** — don't style regular text to look like a heading
- Each page should have **one `h1`** representing the main topic or title

---

## Correct structure example

```html
<!-- page title -->
<h1>What is HTML</h1>

<!-- first section -->
<section>
  <h2>Introduction to HTML</h2>
  <p>HTML stands for HyperText Markup Language. It is the standard language for creating web pages.</p>
</section>

<!-- second section -->
<section>
  <h2>History of HTML</h2>
  <p>HTML began to take shape in the early 90s.</p>

  <h3>Origins</h3>
  <p>HTML was created by Tim Berners-Lee in 1991.</p>
</section>
```

---

## Common mistakes to avoid

| ❌ Incorrect | ✅ Correct |
|---|---|
| Skipping from `h1` to `h3` | Always use `h2` between `h1` and `h3` |
| Multiple `h1` elements on one page | One `h1` per page only |
| Vague heading text like "Section 1" | Descriptive text like "History of HTML" |
| Using bold/large text instead of headings | Use actual `<h2>`, `<h3>` elements |
| Heading with no content below it | Always follow a heading with content |



