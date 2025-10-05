# Instructional Framework for Beginners: HTML Style Guide

This document converts the HTML Style Guide lesson note into a beginner-friendly teaching package, adhering to a structured instructional framework. It covers guidelines for clean, consistent HTML code, including document structure, naming conventions, formatting, and character encoding. The package includes clear explanations, runnable examples, and guided exercises without complete solutions for practice tasks.

---

## Section 1 — Topical Explanations

Writing clean HTML is like keeping a tidy kitchen—it makes it easier for others (and yourself) to work with your code. The HTML Style Guide provides rules to ensure your code is readable, maintainable, and error-free. This section explains each guideline with step-by-step examples and troubleshooting tips.

### Always Declare Document Type
- **What it does**: The `<!DOCTYPE html>` declaration tells browsers the document is HTML5.
- **Purpose**: Ensures consistent rendering across browsers, like setting the rules for a game.

**Example Code**:
```html
<!DOCTYPE html> <!-- Declares HTML5 document -->
<html>
<head>
  <title>My Page</title>
</head>
<body>
  <p>Hello, world!</p>
</body>
</html>
```
- **Line-by-line explanation**:
  - `<!DOCTYPE html>`: Must be the first line; case-insensitive but typically uppercase.
  - `<html>`: Root element wrapping the page.
  - `<title>`: Sets the browser tab title.
  - `<body>`: Contains visible content.
- **Expected output**: A webpage with “My Page” in the tab and “Hello, world!” in the body.
- **Visual cue**: Browser renders the page correctly without quirks mode.
- **Common errors**:
  - Omitting `<!DOCTYPE>` triggers quirks mode, causing inconsistent styling.
  - **Fix**: Always include `<!DOCTYPE html>` at the start.
- **Validation check**: Save as `index.html`, open in a browser, and check for proper rendering.

### Use Lowercase Element and Attribute Names
- **What it does**: Uses lowercase for HTML tags (e.g., `<p>`) and attributes (e.g., `href`).
- **Purpose**: Ensures consistency and readability, like using a standard font in a document.

**Example Code**:
```html
<a href="https://example.com">Visit Example</a> <!-- Lowercase tag and attribute -->
```
- **Explanation**: Uses `href` instead of `HREF` for clarity.
- **Expected output**: A clickable link: “Visit Example”.
- **Common error**: Mixing cases (e.g., `<A HREF=...>`) looks messy and may confuse collaborators.
- **Validation check**: Confirm tags and attributes are lowercase in your code editor.

### Close All HTML Elements
- **What it does**: Ensures all elements have closing tags (e.g., `</p>`).
- **Purpose**: Prevents rendering issues and improves compatibility with XML/XHTML tools.

**Example Code**:
```html
<section>
  <p>This is a paragraph.</p> <!-- Closed properly -->
</section>
```
- **Explanation**: `<p>` is closed with `</p>`, unlike older HTML where it was optional.
- **Expected output**: A paragraph within a section, displayed correctly.
- **Common error**: Unclosed tags (e.g., `<p>Text`) can break layouts in some browsers.
- **Validation check**: Use an HTML validator (e.g., W3C Validator) to check for unclosed tags.

### Always Quote Attribute Values
- **What it does**: Encloses attribute values in double quotes (e.g., `class="example"`).
- **Purpose**: Improves readability and prevents errors with spaces in values.

**Example Code**:
```html
<table class="striped"> <!-- Quoted attribute -->
  <tr><td>Data</td></tr>
</table>
```
- **Explanation**: `class="striped"` uses quotes, unlike `class=striped`.
- **Expected output**: A table styled with the “striped” class.
- **Common error**: Unquoted values with spaces (e.g., `class=table striped`) break the HTML.
- **Validation check**: Check that attributes with spaces (e.g., `class="table striped"`) work.

### Specify `alt`, `width`, and `height` for Images
- **What it does**: Requires `alt` for accessibility and `width`/`height` to reserve space.
- **Purpose**: Ensures images are accessible and reduce flickering during loading.

**Example Code**:
```html
<img src="image.jpg" alt="A scenic mountain" width="128" height="128"> <!-- Complete attributes -->
```
- **Explanation**:
  - `alt`: Describes the image for screen readers.
  - `width`/`height`: Reserves space, preventing layout shifts.
- **Expected output**: Image displays without flickering, with fallback text if it fails to load.
- **Common error**: Missing `alt` reduces accessibility; omitting `width`/`height` causes flickering.
- **Validation check**: Disable images in the browser to confirm `alt` text appears.

### Spaces and Equal Signs
- **What it does**: Avoids spaces around equal signs in attributes (e.g., `href="styles.css"`).
- **Purpose**: Makes code compact and readable, like avoiding extra spaces in a sentence.

**Example Code**:
```html
<link rel="stylesheet" href="styles.css"> <!-- No spaces around = -->
```
- **Explanation**: `rel="stylesheet"` is clean, unlike `rel = "stylesheet"`.
- **Expected output**: Links to a stylesheet without errors.
- **Common error**: Extra spaces (e.g., `href = "styles.css"`) may confuse parsers.
- **Validation check**: Confirm attributes have no spaces around `=`.

### Avoid Long Code Lines
- **What it does**: Keeps code lines short to avoid horizontal scrolling in editors.
- **Purpose**: Improves readability, like keeping sentences short in a book.

**Example Code**:
```html
<p>This is a short paragraph that fits on one line.</p>
```
- **Explanation**: Avoids long lines like `<p style="font-size: 16px; color: blue; margin: 10px; padding: 5px;">`.
- **Expected output**: Clean, readable code in the editor.
- **Common error**: Long inline CSS or text causes scrolling.
- **Validation check**: View code in an editor to ensure no horizontal scrolling.

### Use Blank Lines and Indentation
- **What it does**: Adds blank lines between logical blocks and indents with two spaces.
- **Purpose**: Organizes code like paragraphs in an essay, improving readability.

**Example Code**:
```html
<body>
  <h1>Famous Cities</h1>

  <section>
    <h2>Tokyo</h2>
    <p>Tokyo is the capital of Japan.</p>
  </section>

  <section>
    <h2>Paris</h2>
    <p>Paris is the capital of France.</p>
  </section>
</body>
```
- **Explanation**:
  - Blank lines separate the `<h1>` and `<section>` blocks.
  - Two-space indentation organizes nested elements.
- **Expected output**: Cleanly formatted code in the editor; normal rendering in the browser.
- **Common error**: No indentation or random blank lines make code hard to follow.
- **Validation check**: Check code in an editor for consistent indentation and spacing.

### Never Skip the `<title>` Element
- **What it does**: Requires a `<title>` in the `<head>` for SEO and browser display.
- **Purpose**: Defines the page’s identity, like a book’s cover title.

**Example Code**:
```html
<head>
  <title>HTML Style Guide</title>
</head>
```
- **Explanation**: Descriptive title improves SEO and clarity.
- **Expected output**: “HTML Style Guide” in the browser tab.
- **Common error**: Missing `<title>` results in “Untitled Document” or poor SEO.
- **Validation check**: Confirm the tab displays the correct title.

### Include `<html>` and `<body>` Tags
- **What it does**: Uses `<html>` and `<body>` for proper document structure.
- **Purpose**: Ensures compatibility with older browsers and XML tools.

**Example Code**:
```html
<!DOCTYPE html>
<html>
<body>
  <p>Hello, world!</p>
</body>
</html>
```
- **Explanation**: `<html>` and `<body>` provide a standard structure.
- **Expected output**: A simple webpage with “Hello, world!”.
- **Common error**: Omitting `<body>` may cause errors in older browsers.
- **Validation check**: Test in an older browser (e.g., via emulator) to ensure rendering.

### Add the `lang` Attribute
- **What it does**: Specifies the page’s language in the `<html>` tag (e.g., `lang="en-us"`).
- **Purpose**: Helps search engines and screen readers, like labeling a book’s language.

**Example Code**:
```html
<html lang="en-us">
<head>
  <title>Page Title</title>
</head>
</html>
```
- **Explanation**: `lang="en-us"` indicates American English content.
- **Expected output**: No visible change, but improves accessibility and SEO.
- **Common error**: Missing `lang` reduces accessibility.
- **Validation check**: Use a screen reader to confirm language detection.

### Meta Data and Viewport
- **What it does**: Uses `<meta charset="UTF-8">` for encoding and `<meta name="viewport">` for responsiveness.
- **Purpose**: Ensures proper character display and mobile-friendly scaling.

**Example Code**:
```html
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
```
- **Explanation**:
  - `charset="UTF-8"`: Supports global characters.
  - `viewport`: Makes the page responsive on mobile devices.
- **Expected output**: Correct character rendering and mobile scaling.
- **Common error**: Missing viewport causes mobile display issues.
- **Validation check**: Test on a mobile device to confirm scaling.

### HTML Comments
- **What it does**: Uses `<!-- -->` for notes, with single-line or indented multi-line formats.
- **Purpose**: Documents code for clarity, like sticky notes in a textbook.

**Example Code**:
```html
<!-- Single-line comment -->
<section>
  <!--
    This section describes a city.
    Add more cities as needed.
  -->
  <p>Tokyo is the capital of Japan.</p>
</section>
```
- **Explanation**: Comments explain code without affecting rendering.
- **Expected output**: Comments are invisible in the browser.
- **Common error**: Unclosed comments (e.g., `<!-- Comment`) break the page.
- **Validation check**: Ensure comments don’t appear in the rendered page.

### Using Style Sheets and JavaScript
- **What it does**: Simplifies `<link>` and `<script>` tags by omitting `type` attributes.
- **Purpose**: Reduces clutter, as modern browsers assume CSS and JavaScript.

**Example Code**:
```html
<link rel="stylesheet" href="styles.css">
<script src="myscript.js"></script>
```
- **Explanation**: Omits `type="text/css"` and `type="text/javascript"`.
- **Expected output**: Styles and scripts load correctly.
- **Common error**: Incorrect file paths prevent loading.
- **Validation check**: Confirm styles/scripts apply in the browser.

### Use Lowercase File Names and Extensions
- **What it does**: Uses lowercase for file names (e.g., `index.html`, `styles.css`) and standard extensions (`.html`, `.css`, `.js`).
- **Purpose**: Avoids server case-sensitivity issues, like using consistent labels.

**Example Code** (file names):
- `index.html`, `styles.css`, `script.js`
- **Explanation**: Lowercase avoids errors on case-sensitive servers (e.g., Apache).
- **Expected output**: Files load correctly on any server.
- **Common error**: Mixed-case names (e.g., `Index.HTML`) fail on some servers.
- **Validation check**: Test on a case-sensitive server (e.g., via hosting).

### HTML Encoding (Character Sets)
- **What it does**: Uses `<meta charset="UTF-8">` to support global characters.
- **Purpose**: Ensures proper display of text, like using a universal alphabet.

**Example Code**:
```html
<meta charset="UTF-8">
<p>Special characters: Ā Ć ɖ ‰</p>
```
- **Explanation**: UTF-8 supports characters like `Ā` and `‰`, unlike ASCII or ISO-8859-1.
- **Expected output**: Special characters display correctly.
- **Common error**: Using `charset="ISO-8859-1"` may fail for non-Latin characters.
- **Validation check**: Include special characters and confirm they render.

---

## Section 2 — Class Exercise

**Theme**: Create a clean, styled webpage about a favorite city, following the HTML Style Guide.

**Objectives**:
- Apply style guide rules (lowercase tags/attributes, quoted values, indentation, etc.).
- Use `<title>`, `<meta charset>`, `<meta viewport>`, and `lang` attribute.
- Ensure accessibility with image attributes.

**Stepwise Instructions**:
1. Create an HTML file named `city_page.html`.
2. Add `<!DOCTYPE html>`, `<html lang="en-us">`, and a `<head>` with:
   - A `<title>` (e.g., “About Tokyo”).
   - `<meta charset="UTF-8">` and `<meta name="viewport">`.
3. In the `<body>`:
   - Add a `<section>` with a heading and paragraph about a city.
   - Include an `<img>` with `alt`, `width`, and `height`.
   - Add a `<!-- Comment -->` explaining the section.
4. Add a `<style>` section to style the `<section>` (e.g., border, padding) and text.
5. Use lowercase tags/attributes, quote values, and indent with two spaces.
6. Test on desktop and mobile to ensure readability and responsiveness.

**Hints**:
- Use a placeholder image (e.g., `https://via.placeholder.com/150`) if needed.
- Keep lines short (e.g., break long CSS rules into multiple lines).
- Add a blank line between the heading and paragraph.

**Checkpoints**:
- Are all tags and attributes lowercase?
- Are attribute values quoted?
- Does the image have `alt`, `width`, and `height`?
- Is the code indented with two spaces and free of long lines?
- Does the page scale correctly on mobile?

---

## Section 3 — Weekly Project

**Theme**: Build a responsive “Travel Guide” webpage with multiple city sections, following the HTML Style Guide.

**Milestones**:
1. **Setup**: Create a file named `travel_guide.html` with `<!DOCTYPE html>`, `<html lang="en-us">`, and a `<head>` including `<title>`, `<meta charset>`, `<meta viewport>`, and `<meta name="description">`.
2. **Content**: In the `<body>`:
   - Add a `<header>` with a page title (e.g., `<h1>Travel Guide</h1>`).
   - Add a `<nav>` with links to each city section (use `id` attributes).
   - Create two `<section>`s, each with a heading, paragraph, and `<img>` (with `alt`, `width`, `height`).
   - Add comments to explain each section.
   - Include a `<footer>` with contact or copyright info.
3. **Styling**: Use a `<style>` section to style sections (e.g., borders, centered content) and ensure responsiveness with a media query (e.g., stack sections on screens < 600px).
4. **Code Quality**: Follow style guide rules (lowercase, quoted attributes, indentation, no long lines).
5. **Testing**: Test on desktop and mobile for responsiveness, accessibility, and error-free rendering.

**Success Metrics**:
- Page loads without errors.
- Tags and attributes are lowercase, with quoted values and proper indentation.
- Images have `alt`, `width`, and `height` attributes.
- Layout is responsive and accessible.
- Comments clarify the code structure.

**Extension Ideas**:
- Add a `<link>` to an external CSS file instead of `<style>`.
- Include special characters (e.g., `é` or `€`) to test UTF-8 encoding.
- Research how the `lang` attribute affects screen readers.

**Research Prompts**:
- Why is UTF-8 preferred over ISO-8859-1 for modern webpages?
- How does proper indentation improve collaboration in coding projects?

---

## Completion Checklist
- **Learning Goals**:
  - Apply HTML Style Guide rules for clean, consistent code.
  - Use proper document structure (`<!DOCTYPE>`, `<html>`, `<body>`, `<head>`, `<title>`).
  - Ensure accessibility with `alt` attributes and `lang`.
  - Implement responsive design with `<meta viewport>`.
- **Runnable Example**:
```html
<!DOCTYPE html>
<html lang="en-us">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>About Tokyo</title>
  <style>
    section {
      border: 1px solid #ccc;
      padding: 15px;
      max-width: 600px;
      margin: 10px auto;
    }
    img {
      max-width: 100%;
      height: auto;
    }
  </style>
</head>
<body>
  <!-- City description -->
  <section>
    <h2>Tokyo</h2>
    <p>Tokyo is the capital of Japan.</p>
    <img src="https://via.placeholder.com/150" alt="Tokyo skyline" width="150" height="150">
  </section>
</body>
</html>
```
- **Checklist for Completion**:
  - [ ] `<!DOCTYPE html>` is the first line.
  - [ ] Tags and attributes are lowercase with quoted values.
  - [ ] All elements are closed (e.g., `</p>`).
  - [ ] Images have `alt`, `width`, and `height`.
  - [ ] Code is indented with two spaces and has blank lines between blocks.
  - [ ] `<meta charset>` and `<meta viewport>` are present.
  - [ ] No errors in the browser console (right-click, Inspect, Console).
- **Common Pitfalls**:
  - Missing `<!DOCTYPE>` or `<title>` affects rendering or SEO.
  - Unquoted attributes with spaces break the page.
  - Inconsistent indentation or long lines reduce readability.
  - Missing `alt` attributes harms accessibility.
- **One-line Summary**: The HTML Style Guide ensures clean, consistent, and accessible code with proper structure, lowercase naming, quoted attributes, and responsive design.