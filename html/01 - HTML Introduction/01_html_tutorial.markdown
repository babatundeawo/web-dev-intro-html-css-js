# HTML Tutorial for Beginners

Below is a beginner-friendly teaching package based on the provided HTML tutorial, following the instructional framework for comprehensive, accessible, and practical learning.

---

## Section 1 — Topical Explanations

This section explains the key concepts from the HTML tutorial, using plain language, everyday metaphors, and step-by-step breakdowns of code examples. Each concept is paired with commented code, expected outputs, visual cues, common errors, and validation checks to ensure beginners can follow along confidently.

### Concept 1: What is HTML?

HTML (Hyper Text Markup Language) is like the blueprint of a house—it tells the web browser how to structure and display content on a webpage. It uses **elements** (like building blocks) to label content, such as headings, paragraphs, or links.

- **Key Points**:
  - HTML is the standard language for creating webpages.
  - It consists of elements that describe content (e.g., "this is a heading").
  - Browsers read HTML to show text, images, and links correctly.
- **Metaphor**: Think of HTML as a recipe card. The tags (like `<h1>` or `<p>`) are instructions telling the chef (browser) how to prepare and present the dish (webpage).

### Concept 2: Structure of an HTML Document

An HTML document is like a nested set of boxes, with each box containing specific content. The main parts are:

- `<!DOCTYPE html>`: Declares the document as HTML5.
- `<html>`: The root box that holds everything.
- `<head>`: Contains metadata (like the page title shown in the browser tab).
- `<body>`: Holds visible content like headings and paragraphs.

**Example Code Breakdown**:

Let’s analyze the provided example line-by-line:

```html
<!DOCTYPE html> <!-- Declares this is an HTML5 document; tells browsers how to read it -->
<html> <!-- Root element; everything else nests inside -->
<head> <!-- Contains metadata, not visible on the page -->
    <title>Page Title</title> <!-- Sets the title shown in the browser tab -->
</head>
<body> <!-- Contains all visible content -->
    <h1>This is a Heading</h1> <!-- A large heading -->
    <p>This is a paragraph.</p> <!-- A block of text -->
</body>
</html> <!-- Closes the root element -->
```

- **Purpose**: Creates a simple webpage with a heading and paragraph.
- **Inputs**: None (static HTML).
- **Outputs**: A webpage with "Page Title" in the browser tab, a large heading "This is a Heading," and a paragraph "This is a paragraph."
- **Side Effects**: None (just displays content).
- **Expected Output in Browser**:
  - Browser tab shows: "Page Title"
  - Page displays:
    ```
    This is a Heading
    This is a paragraph.
    ```
- **Visual Cues**: The heading is larger and bolder than the paragraph. Text appears in the browser’s default font and style.
- **Common Errors**:
  - Missing `<!DOCTYPE html>`: Browser may misinterpret the page (e.g., quirky rendering).
    - **Fix**: Always include `<!DOCTYPE html>` at the top.
  - Forgetting closing tags (e.g., `</p>`): Text may overlap or display incorrectly.
    - **Fix**: Double-check that every opening tag has a matching closing tag.
- **Validation Check**: Save the file as `index.html`, open it in a browser, and confirm the title appears in the tab and the content displays as expected.

### Concept 3: HTML Elements

HTML elements are like labeled containers. Each has a **start tag** (e.g., `<p>`), **content**, and an **end tag** (e.g., `</p>`). Some elements, like `<br>` (line break), are **empty elements** with no content or end tag.

- **Example**:

```html
<p>This is a paragraph.</p> <!-- Start tag, content, end tag -->
<br> <!-- Empty element; adds a line break -->
```

- **Metaphor**: Elements are like sticky notes. The tag names (e.g., `p`, `h1`) are the note’s label, and the content is what you write on it. Empty elements like `<br>` are blank sticky notes that just mark a spot.

### Concept 4: HTML Attributes

Attributes are like extra instructions on a sticky note, providing more details about an element. They are written in the start tag as `name="value"`.

- **Example (Link with `href` Attribute)**:

```html
<a href="https://www.w3schools.com">This is a link</a>
```

- **Line-by-Line**:
  - `<a>`: Defines a hyperlink.
  - `href="https://www.w3schools.com"`: Specifies the destination URL.
  - `This is a link`: The clickable text displayed.
  - `</a>`: Closes the element.
- **Purpose**: Creates a clickable link to W3Schools.
- **Output**: Displays "This is a link" (underlined, usually blue) that navigates to W3Schools when clicked.
- **Common Errors**:
  - Missing quotes around the `href` value (e.g., `href=https://www.w3schools.com`): May break the link.
    - **Fix**: Always use quotes (`"` or `'`) around attribute values.
  - Incorrect URL: Leads to a "404 Not Found" error.
    - **Fix**: Verify the URL is correct.
- **Validation Check**: Click the link in the browser to ensure it navigates to the correct page.

- **Example (Image with Attributes)**:

```html
<img src="w3schools.jpg" alt="W3Schools.com" width="104" height="142">
```

- **Line-by-Line**:
  - `<img>`: Defines an image.
  - `src="w3schools.jpg"`: Path to the image file.
  - `alt="W3Schools.com"`: Text shown if the image fails to load (also used by screen readers).
  - `width="104" height="142"`: Sets image size in pixels.
- **Purpose**: Displays an image with specified size and alternative text.
- **Output**: Shows the image if `w3schools.jpg` exists; otherwise, displays "W3Schools.com" (alt text).
- **Common Errors**:
  - Wrong `src` path (e.g., `img_typo.jpg`): Image doesn’t load, shows alt text or a broken icon.
    - **Fix**: Check the file name and path.
  - Missing `alt` attribute: Inaccessible for screen readers.
    - **Fix**: Always include a descriptive `alt` attribute.
- **Validation Check**: Load the page and verify the image appears. If not, check the console (right-click > Inspect > Console) for errors.

### Concept 5: Creating and Viewing an HTML Page

To create a webpage:

1. Write HTML in a text editor (e.g., Notepad or TextEdit).
2. Save with a `.html` or `.htm` extension (e.g., `index.html`).
3. Open in a browser to view.

- **Step-by-Step Example**:

```html
<!DOCTYPE html>
<html>
<body>
    <h1>My First Heading</h1>
    <p>My first paragraph.</p>
</body>
</html>
```

- **Steps**:
  1. Open Notepad/TextEdit.
  2. Copy the code above.
  3. Save as `index.html` with UTF-8 encoding.
  4. Double-click the file to open in a browser.
- **Output**: Displays a heading and paragraph.
- **Common Errors**:
  - Saving as `.txt` instead of `.html`: Browser won’t render it as a webpage.
    - **Fix**: Ensure the file extension is `.html`.
  - Incorrect file path when linking images or other resources.
    - **Fix**: Use relative paths (e.g., `src="images/photo.jpg"`) and verify file locations.
- **Validation Check**: Open the file in a browser and confirm the content displays correctly.

### Concept 6: HTML History and Standards

HTML has evolved since 1989, with HTML5 as the latest standard (2014). This tutorial uses HTML5, which is modern and widely supported.

- **Key Takeaway**: Use `<!DOCTYPE html>` to ensure browsers interpret your code as HTML5.
- **Validation Check**: Always start your HTML files with `<!DOCTYPE html>` to avoid rendering issues.

---

## Section 2 — Class Exercise

This exercise helps you practice creating a simple webpage with headings, paragraphs, links, and images, tying into the concepts above.

**Theme**: Create a personal bio webpage.

**Objectives**:

- Use HTML elements (`<h1>`, `<p>`, `<a>`, `<img>`).
- Apply attributes (`href`, `src`, `alt`).
- Save and view the page in a browser.

**Stepwise Instructions**:

1. Open a text editor (Notepad or TextEdit).
2. Create a new HTML file with the basic structure:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Your Name - Bio</title>
</head>
<body>
</body>
</html>
```

3. Inside the `<body>`, add:
   - An `<h1>` with your name.
   - A `<p>` describing yourself (e.g., hobbies, favorite subject).
   - An `<a>` linking to a favorite website (e.g., a social media page or blog).
   - An `<img>` with a photo (use a placeholder like `https://via.placeholder.com/150` if you don’t have one).
4. Save the file as `bio.html`.
5. Open it in a browser to view.

**Hints**:

- Use `href` for the link’s destination.
- Include an `alt` attribute for the image (e.g., `alt="My photo"`).
- Check that all tags are closed properly.

**Checkpoints**:

- Does the browser tab show your name?
- Does the image load, or do you see the alt text?
- Does the link take you to the correct website when clicked?

---

## Section 3 — Weekly Project

This project combines the concepts learned to create a multi-page personal website with milestones to build confidence.

**Project Brief**: Build a simple two-page website: a homepage and an "About Me" page.

**Milestones**:

1. **Homepage**:
   - Create `index.html`.
   - Include a heading (`<h1>`), a welcome paragraph (`<p>`), and an image (`<img>`).
   - Add a link (`<a>`) to the "About Me" page.
2. **About Me Page**:
   - Create `about.html`.
   - Include a heading, a paragraph about yourself, and a link back to the homepage.
3. **Testing**:
   - Save both files in the same folder.
   - Open `index.html` in a browser and test navigation between pages.

**Success Metrics**:

- Both pages load correctly in a browser.
- Links navigate between `index.html` and `about.html`.
- Images display with appropriate alt text.
- All tags are properly closed, and the `<!DOCTYPE html>` is included.

**Research Prompts**:

- Look up how to add multiple paragraphs or headings to make your pages more detailed.
- Explore how to find free, copyright-free images online for your `<img>` tags.

**Extension Ideas**:

- Add a third page for a hobby or interest.
- Experiment with the `style` attribute to change text color (e.g., `<p style="color:blue;">`).

---

## Completion Checklist

- **Learning Goals**:
  - Understand HTML as a markup language.
  - Create a basic HTML document with `<!DOCTYPE html>`, `<html>`, `<head>`, and `<body>`.
  - Use elements (`<h1>`, `<p>`, `<a>`, `<img>`) and attributes (`href`, `src`, `alt`).
  - Save and view HTML files in a browser.
- **Runnable Example**:

```html
<!DOCTYPE html>
<html>
<head>
    <title>My First Page</title>
</head>
<body>
    <h1>Welcome to My Page</h1>
    <p>This is my first webpage!</p>
    <a href="https://www.w3schools.com">Visit W3Schools</a>
    <img src="https://via.placeholder.com/150" alt="Placeholder image">
</body>
</html>
```

- Save as `index.html` and open in a browser to test.
- **Checklist for Completion**:
  - [ ] File starts with `<!DOCTYPE html>`.
  - [ ] Includes `<html>`, `<head>`, `<title>`, and `<body>` tags.
  - [ ] Displays at least one heading, paragraph, link, and image.
  - [ ] Links work and images load (or show alt text).
  - [ ] Saved as `.html` and renders correctly in a browser.
- **Common Pitfalls**:
  - Forgetting closing tags (e.g., `</p>`).
  - Incorrect attribute syntax (e.g., missing quotes in `href` or `src`).
  - Wrong file extension (e.g., saving as `.txt`).
- **One-Line Summary**: HTML is a simple markup language that uses elements and attributes to structure and display webpage content, easily created with a text editor and viewed in a browser.