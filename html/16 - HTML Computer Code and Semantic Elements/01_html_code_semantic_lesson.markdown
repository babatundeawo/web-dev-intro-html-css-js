# Instructional Framework for Beginners: HTML Computer Code and Semantic Elements

This document converts the lesson note on HTML computer code elements (`<code>`, `<kbd>`, `<samp>`, `<var>`, `<pre>`) and semantic elements (`<section>`, `<article>`, `<header>`, `<footer>`, `<nav>`, `<aside>`, `<figure>`, `<figcaption>`) into a beginner-friendly teaching package. It follows a structured instructional framework, providing clear explanations, runnable examples, and guided exercises without complete solutions for practice tasks.

---

## Section 1 — Topical Explanations

HTML computer code and semantic elements are like tools in a toolbox: each has a specific purpose to make your webpage clear to users, browsers, and assistive technologies (like screen readers). Computer code elements format code-related text, while semantic elements give structure and meaning to content. This section explains each element with step-by-step examples and troubleshooting tips.

### HTML Computer Code Elements

#### The `<code>` Element
- **What it does**: Displays a piece of computer code in the browser’s default monospace font (e.g., Courier or Consolas).
- **Purpose**: Makes code snippets stand out, like highlighting a recipe’s ingredients in a cookbook.
- **Key note**: Does not preserve whitespace or line breaks unless wrapped in `<pre>`.

**Example Code** (expanded with comments):
```html
<code>
x = 5; <!-- Variable assignment -->
y = 6; <!-- Another variable assignment -->
z = x + y; <!-- Adds x and y, stores in z -->
</code>
```
- **Line-by-line explanation**:
  - `<code>`: Wraps the code snippet, rendering it in monospace font.
  - Each line represents a JavaScript statement, but it’s displayed as plain text in HTML.
- **Expected output**: `x = 5; y = 6; z = x + y;` in a single line, in monospace font.
- **Visual cue**: Text appears in a font like Courier, distinct from surrounding text.
- **Common errors**:
  - Whitespace/line breaks ignored, making code hard to read.
  - **Fix**: Use `<pre>` to preserve formatting (see below).
- **Validation check**: View in a browser to confirm the monospace font.

**With `<pre>` for Formatting**:
```html
<pre> <!-- Preserves whitespace and line breaks -->
<code>
x = 5; <!-- Variable assignment -->
y = 6; <!-- Another variable -->
z = x + y; <!-- Adds x and y -->
</code>
</pre>
```
- **Explanation**: `<pre>` ensures each line appears as written, with spaces and line breaks preserved.
- **Expected output**:
  ```
  x = 5;
  y = 6;
  z = x + y;
  ```
- **Visual cue**: Code appears formatted as written, in monospace font.
- **Validation check**: Confirm line breaks are preserved in the browser.

#### The `<kbd>` Element
- **What it does**: Represents keyboard input, displayed in the browser’s monospace font.
- **Purpose**: Shows users specific keys to press, like labeling buttons on a remote control.

**Example Code** (expanded):
```html
<p>Save the document by pressing <kbd>Ctrl + S</kbd></p> <!-- Shows keyboard shortcut -->
```
- **Explanation**: `<kbd>` highlights “Ctrl + S” as a keyboard command.
- **Expected output**: “Save the document by pressing `Ctrl + S`” (monospace font for `Ctrl + S`).
- **Visual cue**: The shortcut stands out in a monospace font.
- **Common error**: Nesting `<kbd>` inside other formatting tags (e.g., `<b>`) may override the monospace style.
- **Validation check**: Check that “Ctrl + S” appears in monospace font.

#### The `<samp>` Element
- **What it does**: Displays sample output from a program, in monospace font.
- **Purpose**: Mimics computer or terminal output, like a printed receipt from a machine.

**Example Code** (expanded):
```html
<p>Message from my computer:</p>
<p><samp>File not found.<br>Press F1 to continue</samp></p> <!-- Simulates program output -->
```
- **Line-by-line explanation**:
  - `<samp>`: Wraps the output text.
  - `<br>`: Adds a line break for readability.
- **Expected output**:
  ```
  Message from my computer:
  File not found.
  Press F1 to continue
  ```
- **Visual cue**: Output text is in monospace font, distinct from regular text.
- **Common error**: Forgetting `<br>` for multi-line output can make it appear as one line.
- **Validation check**: Confirm the text is monospace and formatted as expected.

#### The `<var>` Element
- **What it does**: Defines a variable (e.g., in programming or math), typically displayed in italics.
- **Purpose**: Highlights variables to distinguish them from regular text, like underlining key terms in a textbook.

**Example Code** (expanded):
```html
<p>The area of a triangle is: 1/2 x <var>b</var> x <var>h</var>, where <var>b</var> is the base, and <var>h</var> is the vertical height.</p>
```
- **Explanation**:
  - `<var>`: Marks `b` and `h` as variables, usually italicized.
- **Expected output**: “The area of a triangle is: 1/2 x *b* x *h*, where *b* is the base, and *h* is the vertical height.” (italics for `b` and `h`).
- **Visual cue**: Variables appear in italics.
- **Common error**: Browser styles may not italicize `<var>`; use CSS (`var { font-style: italic; }`) to enforce it.
- **Validation check**: Confirm variables are italicized or styled distinctly.

#### The `<pre>` Element
- **What it does**: Displays preformatted text, preserving whitespace and line breaks, in monospace font.
- **Purpose**: Ideal for code blocks or text requiring exact formatting, like a poem with specific spacing.

**Example Code** (covered above with `<code>`):
- **Key use**: Often wraps `<code>` to maintain code formatting.
- **Common error**: Using `<pre>` without `<code>` for code snippets may not convey “code” context to screen readers.
- **Validation check**: Ensure text inside `<pre>` retains its exact spacing and line breaks.

### HTML Semantic Elements

Semantic elements are like labeled folders in a filing cabinet—they give content clear meaning, making it easier for browsers, developers, and assistive technologies to understand the structure.

#### The `<section>` Element
- **What it does**: Groups related content, typically with a heading, like chapters in a book.
- **Purpose**: Organizes content thematically for clarity and accessibility.

**Example Code** (expanded):
```html
<section> <!-- Groups content about WWF -->
  <h1>WWF</h1>
  <p>The World Wide Fund for Nature (WWF) is...</p>
</section>
<section> <!-- Groups content about WWF's logo -->
  <h1>WWF's Panda symbol</h1>
  <p>The Panda has become the symbol of WWF...</p>
</section>
```
- **Explanation**: Each `<section>` groups related content with a heading.
- **Expected output**: Two distinct sections with headings and paragraphs.
- **Visual cue**: Content appears as normal text unless styled with CSS.
- **Common error**: Overusing `<section>` instead of `<div>` for non-thematic grouping.
- **Validation check**: Ensure each section has a heading for semantic clarity.

#### The `<article>` Element
- **What it does**: Defines independent, self-contained content, like a blog post or news article.
- **Purpose**: Marks content that could stand alone if extracted, like a magazine article.

**Example Code** (with CSS, expanded):
```html
<head>
  <style>
    .all-browsers { margin: 0; padding: 5px; background-color: lightgray; }
    .all-browsers > h1, .browser { margin: 10px; padding: 5px; }
    .browser { background: white; }
    .browser > h2, p { margin: 4px; font-size: 90%; }
  </style>
</head>
<body>
  <article class="all-browsers"> <!-- Container for related articles -->
    <h1>Most Popular Browsers</h1>
    <article class="browser"> <!-- Individual browser article -->
      <h2>Google Chrome</h2>
      <p>Google Chrome is a web browser developed by Google...</p>
    </article>
    <article class="browser">
      <h2>Mozilla Firefox</h2>
      <p>Mozilla Firefox is an open-source web browser...</p>
    </article>
  </article>
</body>
```
- **Line-by-line explanation**:
  - `<style>`: Styles the outer `<article>` with a gray background and inner `<article>`s with white backgrounds.
  - Outer `<article>`: Groups related browser articles.
  - Inner `<article>`s: Each describes a specific browser, independent and self-contained.
- **Expected output**: A gray container with a heading and white boxes for each browser’s details.
- **Visual cue**: Styled boxes make the articles visually distinct.
- **Common error**: Nesting `<article>` unnecessarily; use `<section>` for thematic grouping within an article.
- **Validation check**: Confirm each `<article>` could stand alone if extracted.

#### The `<header>` Element
- **What it does**: Defines introductory content or navigation, like the title page of a book.
- **Purpose**: Provides context or navigation for a section or article.

**Example Code**:
```html
<article>
  <header> <!-- Introductory content for the article -->
    <h1>What Does WWF Do?</h1>
    <p>WWF's mission:</p>
  </header>
  <p>WWF's mission is to stop the degradation...</p>
</article>
```
- **Explanation**: `<header>` groups the heading and introductory text.
- **Expected output**: Heading and introductory text appear above the main content.
- **Common error**: Placing `<header>` inside `<footer>` or another `<header>` (not allowed).
- **Validation check**: Ensure `<header>` is within `<article>` or `<section>` and contains introductory content.

#### The `<footer>` Element
- **What it does**: Defines footer content, like contact info or copyright, for a document or section.
- **Purpose**: Provides supplementary information, like the back cover of a book.

**Example Code**:
```html
<footer> <!-- Footer for the page -->
  <p>Author: Hege Refsnes</p>
  <p><a href="mailto:hege@example.com">hege@example.com</a></p>
</footer>
```
- **Explanation**: Contains authorship and contact details.
- **Expected output**: Text and a clickable email link at the page’s bottom.
- **Common error**: Including main content in `<footer>`; it’s for supplementary info only.
- **Validation check**: Confirm footer content is relevant (e.g., contact or copyright).

#### The `<nav>` Element
- **What it does**: Defines a block of navigation links.
- **Purpose**: Marks major navigation areas for accessibility and clarity, like a table of contents.

**Example Code**:
```html
<nav> <!-- Navigation menu -->
  <a href="/html/">HTML</a> |
  <a href="/css/">CSS</a> |
  <a href="/js/">JavaScript</a>
</nav>
```
- **Explanation**: Links to key sections, separated by pipes (`|`).
- **Expected output**: Clickable links in a row.
- **Common error**: Including non-navigation links in `<nav>` reduces semantic clarity.
- **Validation check**: Ensure only major navigation links are inside `<nav>`.

#### The `<aside>` Element
- **What it does**: Defines content indirectly related to the main content, like a sidebar.
- **Purpose**: Provides supplementary info, like a “Did You Know?” box in a textbook.

**Example Code** (with CSS):
```html
<head>
  <style>
    aside {
      width: 30%;
      padding-left: 15px;
      margin-left: 15px;
      float: right;
      font-style: italic;
      background-color: lightgray;
    }
  </style>
</head>
<body>
  <p>My family and I visited The Epcot center...</p>
  <aside> <!-- Sidebar content -->
    <p>The Epcot center is a theme park...</p>
  </aside>
</body>
```
- **Explanation**: `<aside>` floats right as a sidebar with a gray background.
- **Expected output**: Main text on the left, sidebar on the right.
- **Visual cue**: Sidebar is italicized and gray.
- **Common error**: Using `<aside>` for unrelated content; it should be indirectly related.
- **Validation check**: Confirm the aside content complements the main content.

#### The `<figure>` and `<figcaption>` Elements
- **What they do**: `<figure>` groups self-contained content (e.g., images, code); `<figcaption>` adds a caption.
- **Purpose**: Provides context for visuals or code, like a labeled diagram.

**Example Code**:
```html
<figure> <!-- Groups image and caption -->
  <img src="pic_trulli.jpg" alt="Trulli"> <!-- Image -->
  <figcaption>Fig1. - Trulli, Puglia, Italy.</figcaption> <!-- Caption -->
</figure>
```
- **Explanation**: `<figure>` wraps an image and its caption for semantic clarity.
- **Expected output**: Image with a caption below it.
- **Common error**: Missing `alt` attribute on `<img>` reduces accessibility.
- **Validation check**: Ensure the caption describes the figure and the `alt` attribute is present.

---

## Section 2 — Class Exercise

**Theme**: Create a webpage showcasing a simple code snippet with an explanation.

**Objectives**:
- Practice using `<code>`, `<pre>`, `<kbd>`, `<samp>`, and `<var>` to display a code-related example.
- Use `<section>` and `<header>` to structure the content.
- Ensure the page is clear and accessible.

**Stepwise Instructions**:
1. Create an HTML file named `code_example.html`.
2. In the `<head>`, add a `<title>` (e.g., “Code Snippet Demo”) and `<meta charset="UTF-8">`.
3. In the `<body>`:
   - Add a `<section>` with a `<header>` containing an `<h1>` (e.g., “Simple Addition Program”).
   - Use `<pre>` and `<code>` to display a code snippet (e.g., a Python snippet: `a = 10; b = 20; sum = a + b;`).
   - Use `<samp>` to show the output (e.g., `Sum is 30`).
   - Use `<kbd>` to show a keyboard shortcut (e.g., “Run with Ctrl + R”).
   - Use `<var>` to explain variables (e.g., `<var>a</var> is the first number”).
4. Add basic CSS in a `<style>` section to style the `<section>` (e.g., border, padding).
5. Test the page to ensure the code and output are formatted correctly.

**Hints**:
- Use `<pre>` to keep the code’s line breaks.
- Style `<samp>` with a different background to mimic a terminal.
- Ensure the `<header>` clearly introduces the section.

**Checkpoints**:
- Does the code appear in monospace font with line breaks?
- Is the output in `<samp>` distinct from other text?
- Does the `<section>` have a clear heading?
- Is the page readable on a mobile device?

---

## Section 3 — Weekly Project

**Theme**: Build a responsive “Programming Tutorial” webpage with computer code and semantic elements.

**Milestones**:
1. **Setup**: Create an HTML file with a `<head>` including `<title>`, `<meta charset>`, `<meta viewport>`, and `<meta description>`.
2. **Content**: Use `<header>` for a page title, `<nav>` for links to tutorial sections, and two `<section>`s:
   - One with a `<pre>` and `<code>` block showing a code snippet, `<samp>` for output, and `<var>` for variable explanations.
   - Another with a `<figure>` containing an image (e.g., a screenshot) and `<figcaption>`.
3. **Styling**: Use a `<style>` section to style the `<section>`s (e.g., borders, background colors) and ensure responsiveness with a media query (e.g., stack sections vertically on screens < 600px).
4. **Footer**: Add a `<footer>` with contact info or a copyright notice.
5. **Testing**: Test on desktop and mobile to verify responsiveness and accessibility.

**Success Metrics**:
- Page loads without errors.
- Code and output are clearly formatted and distinguishable.
- Semantic elements are used correctly (e.g., `<nav>` for navigation only).
- Layout adjusts for mobile devices.
- Image has an `alt` attribute for accessibility.

**Extension Ideas**:
- Add a `<kbd>` element to show a shortcut for running the code.
- Include an `<aside>` with a tip or fun fact about the programming language.
- Research how screen readers interpret `<code>` vs. `<pre>`.

**Research Prompts**:
- How do semantic elements improve accessibility for screen readers?
- What are the benefits of using `<figure>` and `<figcaption>` over plain `<img>` tags?

---

## Completion Checklist
- **Learning Goals**:
  - Understand how to use `<code>`, `<kbd>`, `<samp>`, `<var>`, and `<pre>` for code-related content.
  - Learn to structure content with semantic elements (`<section>`, `<article>`, `<header>`, `<footer>`, `<nav>`, `<aside>`, `<figure>`, `<figcaption>`).
  - Apply basic CSS for visual clarity and responsiveness.
- **Runnable Example**:
```html
<!DOCTYPE html>
<html>
<head>
  <title>Code Demo</title>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    section { border: 1px solid gray; padding: 10px; margin: 10px; }
    pre { background-color: #f4f4f4; padding: 10px; }
    samp { background-color: #e0e0e0; display: block; padding: 5px; }
    @media screen and (max-width: 600px) { section { margin: 5px; } }
  </style>
</head>
<body>
  <section>
    <header>
      <h1>Simple Addition</h1>
    </header>
    <pre><code>a = 10;
b = 20;
sum = a + b;</code></pre>
    <p>Output: <samp>Sum is 30</samp></p>
    <p>Press <kbd>Ctrl + R</kbd> to run.</p>
    <p>Here, <var>a</var> and <var>b</var> are variables.</p>
  </section>
</body>
</html>
```
- **Checklist for Completion**:
  - [ ] Code in `<pre><code>` appears with line breaks in monospace font.
  - [ ] `<samp>` output is distinct (e.g., different background).
  - [ ] `<kbd>` and `<var>` are styled appropriately (monospace and italic, respectively).
  - [ ] Semantic elements (`<section>`, `<header>`) are used correctly.
  - [ ] Page is responsive on mobile devices.
  - [ ] No errors in the browser console (right-click, Inspect, Console).
- **Common Pitfalls**:
  - Forgetting `<pre>` around `<code>` causes formatting loss.
  - Using non-semantic elements (e.g., `<div>`) instead of `<section>` or `<article>`.
  - Missing `alt` attributes on images in `<figure>`.
  - Incorrect CSS syntax breaking styles.
- **One-line Summary**: HTML computer code elements (`<code>`, `<kbd>`, `<samp>`, `<var>`, `<pre>`) and semantic elements (`<section>`, `<article>`, etc.) add clarity and structure to code-related and meaningful content.