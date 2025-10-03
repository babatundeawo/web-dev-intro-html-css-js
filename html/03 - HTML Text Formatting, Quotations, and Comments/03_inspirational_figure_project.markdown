# Solution and Explanation for HTML Weekly Project: Two-Page Inspirational Figure Website

This markdown provides the code solution for the weekly project from the HTML tutorial, which involves creating a two-page website about an inspirational figure (Nelson Mandela) using text formatting elements (`<strong>`, `<em>`, `<mark>`, `<small>`, `<del>`, `<ins>`), quotation elements (`<blockquote>`, `<cite>`, `<abbr>`, `<address>`), and comments (`<!-- -->`). The explanation follows the instructional framework, ensuring beginner-friendly guidance with plain language, metaphors, and detailed breakdowns of the code, including expected outputs, visual cues, common errors, and validation checks.

---

## Section 1 — Topical Explanations

The weekly project requires building a two-page website: a homepage (`index.html`) introducing the inspirational figure with a title, introduction, quote, and link to a Details page, and a Details page (`details.html`) with more information, including achievements, contact info, and navigation back to the homepage. The pages use text formatting, quotation, and comment elements. Below are the solutions for both pages, followed by a step-by-step explanation.

### Solution Code

#### Homepage (`index.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Nelson Mandela Tribute</title>
</head>
<body>
    <!-- Page title and introduction -->
    <h1>Nelson Mandela Tribute</h1>
    <p><strong>Welcome</strong> to my tribute page for <em>Nelson Mandela</em>, a global icon for peace and justice.</p>
    <!-- Famous quote section -->
    <blockquote cite="https://www.nelsonmandela.org">
      Education is the most powerful weapon which you can use to change the world.
    </blockquote>
    <p><cite>Nelson Mandela</cite> said this in a <small>1993 speech</small>.</p>
    <p>Learn more about this <mark>inspirational</mark> leader!</p>
    <!-- <p>Draft: Add more about his early life here.</p> --> <!-- Hidden draft text -->
    <p><a href="details.html">Go to Details</a></p>
</body>
</html>
```

#### Details Page (`details.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>About Nelson Mandela</title>
</head>
<body>
    <!-- Page title and achievements -->
    <h1>About Nelson Mandela</h1>
    <p>Mandela’s work with the <abbr title="African National Congress">ANC</abbr> changed history. He was <em>instrumental</em> in ending <del>oppression</del> <ins>apartheid</ins> in South Africa.</p>
    <!-- Contact/source info -->
    <address>
      Learn more at:<br>
      nelsonmandela.org<br>
      South Africa<br>
      <!-- Contact email: info@nelsonmandela.org -->
    </address>
    <p><mark>His legacy</mark> continues to inspire global movements for equality.</p>
    <p><a href="index.html">Back to Homepage</a></p>
</body>
</html>
```

### Explanation of the Solution

**Overview**: The project is like creating a two-part exhibit for a museum about an inspirational figure. The homepage welcomes visitors with a quote and overview, while the Details page dives deeper into achievements and sources, connected by navigation links. HTML elements structure the content, formatting adds emphasis, and comments document or hide drafts.

**Step-by-Step Instructions to Set Up**:
1. Open a text editor (e.g., Notepad or TextEdit).
2. Create a new folder (e.g., `mandela-tribute`) to store both files.
3. Copy the code for `index.html` into a new file, save as `index.html` with UTF-8 encoding.
4. Copy the code for `details.html` into a new file, save as `details.html` in the same folder.
5. Double-click `index.html` to open in a browser and test navigation, formatting, and content.

**Line-by-Line Breakdown (for `index.html`)**:

- `<!DOCTYPE html>`:
  - **Purpose**: Declares the document as HTML5, ensuring correct browser rendering.
  - **Metaphor**: Like a sign saying, "This is an HTML5 exhibit."
  - **Output**: No visible output, but critical for rendering.
  - **Common Error**: Omitting this triggers "quirks mode," causing display issues.
    - **Fix**: Always include at the top.

- `<html lang="en">`:
  - **Purpose**: The root element, wrapping all content, with `lang="en"` for accessibility.
  - **Metaphor**: The foundation of the exhibit, holding all displays together.
  - **Output**: No visible output, but sets up the page structure.
  - **Common Error**: Missing `lang` reduces accessibility.
    - **Fix**: Include `lang="en"`.

- `<head>`:
  - **Purpose**: Contains metadata, like the page title.
  - **Metaphor**: The exhibit’s welcome sign, providing context.
  - **Output**: Affects browser behavior (e.g., tab title).

- `<title>Nelson Mandela Tribute</title>`:
  - **Purpose**: Sets the browser tab title.
  - **Output**: Browser tab displays "Nelson Mandela Tribute."
  - **Common Error**: Missing `<title>` shows a blank tab or file path.
    - **Fix**: Include a descriptive title.

- `<body>`:
  - **Purpose**: Contains all visible content (headings, paragraphs, quotes, links).
  - **Metaphor**: The main display area of the exhibit.
  - **Output**: Shows all content in the browser window.

- `<!-- Page title and introduction -->`:
  - **Purpose**: Documents the title and introduction section.
  - **Output**: Invisible in the browser, visible in "View Page Source."
  - **Common Error**: Missing `-->` hides unintended content.
    - **Fix**: Ensure `<!--` and `-->` are paired.

- `<h1>Nelson Mandela Tribute</h1>`:
  - **Purpose**: Displays the main title.
  - **Output**: Shows "Nelson Mandela Tribute" in large, bold text.
  - **Visual Cue**: Largest, boldest text with spacing.
  - **Common Error**: Multiple `<h1>` tags confuse search engines.
    - **Fix**: Use one `<h1>` per page.

- `<p><strong>Welcome</strong> to my tribute page for <em>Nelson Mandela</em>, a global icon for peace and justice.</p>`:
  - **Purpose**: Introduces the topic, with "Welcome" bold and "Nelson Mandela" emphasized.
  - **Elements**:
    - `<strong>`: Marks "Welcome" as important, typically bold.
    - `<em>`: Emphasizes "Nelson Mandela," typically italic.
  - **Output**: Shows the sentence with "Welcome" bold and "Nelson Mandela" italic.
  - **Visual Cue**: Bold and italic text within a paragraph.
  - **Common Error**: Using `<b>` or `<i>` instead of `<strong>` or `<em>` reduces semantic meaning.
    - **Fix**: Use `<strong>` and `<em>` for accessibility.

- `<!-- Famous quote section -->`:
  - **Purpose**: Documents the quote section.
  - **Output**: Invisible in the browser.

- `<blockquote cite="https://www.nelsonmandela.org">Education is the most powerful weapon...</blockquote>`:
  - **Purpose**: Displays a long quote, indented, with a source URL.
  - **Attributes**:
    - `cite="https://www.nelsonmandela.org"`: References the quote’s source.
  - **Output**: Shows the quote indented.
  - **Visual Cue**: Indented text block.
  - **Common Error**: Missing `cite` attribute reduces context.
    - **Fix**: Include a valid URL.

- `<p><cite>Nelson Mandela</cite> said this in a <small>1993 speech</small>.</p>`:
  - **Purpose**: Credits the quote’s author, with the year in smaller text.
  - **Elements**:
    - `<cite>`: Marks "Nelson Mandela" as the source, typically italic.
    - `<small>`: Displays "1993 speech" in smaller font.
  - **Output**: Shows "Nelson Mandela" in italic and "1993 speech" smaller.
  - **Visual Cue**: Italic and smaller text in a paragraph.
  - **Common Error**: Incorrect `<cite>` usage (e.g., for non-works).
    - **Fix**: Ensure `<cite>` is appropriate.

- `<p>Learn more about this <mark>inspirational</mark> leader!</p>`:
  - **Purpose**: Encourages further exploration, with "inspirational" highlighted.
  - **Elements**:
    - `<mark>`: Highlights "inspirational," typically with a yellow background.
  - **Output**: Shows the sentence with "inspirational" highlighted.
  - **Visual Cue**: Highlighted text in a paragraph.

- `<!-- <p>Draft: Add more about his early life here.</p> -->`:
  - **Purpose**: Hides a draft paragraph.
  - **Output**: Invisible in the browser.
  - **Common Error**: Incorrect comment syntax.
    - **Fix**: Ensure proper `<!-- -->`.

- `<p><a href="details.html">Go to Details</a></p>`:
  - **Purpose**: Links to the Details page.
  - **Output**: Shows "Go to Details" as a clickable link.
  - **Visual Cue**: Underlined, typically blue text.
  - **Common Error**: Incorrect `href` breaks the link.
    - **Fix**: Ensure `details.html` exists in the same folder.

**Line-by-Line Breakdown (for `details.html`)**:

- The structure mirrors `index.html` with `<!DOCTYPE html>`, `<html lang="en">`, `<head>`, and `<title>About Nelson Mandela</title>`, serving the same purposes.
- `<body>`: Contains visible content.
- `<!-- Page title and achievements -->`: Documents the section.
- `<h1>About Nelson Mandela</h1>`: Displays the page title.
- `<p>Mandela’s work with the <abbr title="African National Congress">ANC</abbr> changed history. He was <em>instrumental</em> in ending <del>oppression</del> <ins>apartheid</ins> in South Africa.</p>`:
  - **Purpose**: Describes achievements, with formatting.
  - **Elements**:
    - `<abbr>`: Shows "ANC" with hover text "African National Congress."
    - `<em>`: Emphasizes "instrumental" (italic).
    - `<del>`: Strikes through "oppression."
    - `<ins>`: Underlines "apartheid."
  - **Output**: Shows the sentence with "ANC" hoverable, "instrumental" italic, "oppression" struck, and "apartheid" underlined.
  - **Visual Cue**: Formatted text with hover effect.
  - **Common Error**: Missing `title` in `<abbr>` reduces accessibility.
    - **Fix**: Include `title="Full Form"`.
- `<!-- Contact/source info -->`: Documents the section.
- `<address>Learn more at:<br>nelsonmandela.org<br>South Africa<br><!-- Contact email: info@nelsonmandela.org --></address>`:
  - **Purpose**: Provides source info, with a hidden comment.
  - **Output**: Shows contact info in italic with line breaks.
  - **Visual Cue**: Italic text with breaks.
  - **Common Error**: Forgetting `<br>` causes text to run together.
    - **Fix**: Use `<br>` for line breaks.
- `<p><mark>His legacy</mark> continues to inspire...</p>`: Highlights "His legacy."
- `<p><a href="index.html">Back to Homepage</a></p>`: Links back to the homepage.

**Expected Output in Browser**:

- For `index.html`:
  - Browser tab: "Nelson Mandela Tribute"
  - Page content:
    ```
    Nelson Mandela Tribute
    Welcome to my tribute page for Nelson Mandela, a global icon for peace and justice. [Welcome bold, Nelson Mandela italic]
      Education is the most powerful weapon which you can use to change the world. [indented]
    Nelson Mandela said this in a 1993 speech. [Nelson Mandela italic, 1993 speech smaller]
    Learn more about this inspirational leader! [inspirational highlighted]
    Go to Details [clickable link]
    ```

- For `details.html`:
  - Browser tab: "About Nelson Mandela"
  - Page content:
    ```
    About Nelson Mandela
    Mandela’s work with the ANC changed history. He was instrumental in ending oppression apartheid in South Africa. [ANC hoverable, instrumental italic, oppression struck, apartheid underlined]
    Learn more at:
    nelsonmandela.org
    South Africa [italic]
    His legacy continues to inspire global movements for equality. [His legacy highlighted]
    Back to Homepage [clickable link]
    ```

**Side Effects**: None (static HTML displays content).

**Visual Cues**:
- Headings are large and bold.
- `<strong>`, `<em>`, `<mark>`, `<small>`, `<del>`, `<ins>` show bold, italic, highlighted, smaller, struck, or underlined text.
- `<blockquote>` is indented, `<cite>` is italic, `<abbr>` shows hover text, `<address>` is italic with breaks.
- Links are underlined and typically blue.
- Comments are invisible in the browser.

**How to Test**:
1. Save both files in the same folder (e.g., `mandela-tribute`).
2. Open `index.html` in a browser by double-clicking.
3. Verify:
   - Browser tabs show correct titles.
   - Formatting (`<strong>`, `<em>`, `<mark>`, etc.) displays correctly.
   - `<blockquote>`, `<cite>`, `<abbr>`, `<address>` render as expected.
   - Links navigate between pages.
   - Comments are invisible but visible in "View Page Source."
4. Hover over `<abbr>` to check the title.
5. Use a screen reader (if available) to confirm accessibility.

**Common Errors and Troubleshooting**:
- **Error**: Links don’t work.
  - **Cause**: Incorrect `href` or files in different folders.
  - **Fix**: Ensure files are in the same folder and `href` matches file names.
- **Error**: Formatting doesn’t apply.
  - **Cause**: Missing closing tags (e.g., `</strong>`).
  - **Fix**: Check all tags are closed.
- **Error**: Quote isn’t indented.
  - **Cause**: Using `<p>` instead of `<blockquote>`.
  - **Fix**: Use `<blockquote>` for long quotes.
- **Error**: `<abbr>` lacks hover text.
  - **Cause**: Missing `title` attribute.
  - **Fix**: Add `title="Full Form"`.
- **Error**: Page shows code.
  - **Cause**: Saved as `.txt`.
  - **Fix**: Save as `.html`.

**Validation Checks**:
- Confirm files start with `<!DOCTYPE html>` and include `<html lang="en">`.
- Check browser tabs for titles.
- Verify formatting, quotation, and comment elements display correctly.
- Ensure links navigate and comments are hidden.
- Confirm `<abbr>` hover text and `<address>` formatting.

**Metaphor for the Whole Process**: Building this website is like creating a two-room museum exhibit. The homepage is the welcome hall with a bold title and inspiring quote, while the Details page is a deeper dive with achievements and sources. Formatting elements add flair, quotation elements provide context, comments are hidden notes, and links are doorways between rooms.

---

## Completion Checklist

- **Learning Goals**:
  - Use text formatting elements (`<strong>`, `<em>`, `<mark>`, `<small>`, `<del>`, `<ins>`).
  - Use quotation elements (`<blockquote>`, `<cite>`, `<abbr>`, `<address>`).
  - Add comments for documentation or hiding content.
  - Create and link multiple HTML pages.
- **Runnable Example**: The code above (`index.html` and `details.html`) is a complete, runnable solution.
- **Checklist for Completion**:
  - [ ] Files start with `<!DOCTYPE html>` and include `<html lang="en">`.
  - [ ] Use at least three text formatting elements and two quotation elements per page.
  - [ ] Include at least one comment per page.
  - [ ] Links navigate between pages.
  - [ ] Formatting and quotation elements display correctly.
  - [ ] Saved as `.html` and renders correctly in a browser.
- **Common Pitfalls**:
  - Forgetting closing tags (e.g., `</p>`, `</blockquote>`).
  - Incorrect `cite` attribute URL in `<blockquote>`.
  - Missing `title` in `<abbr>`.
  - Improper comment syntax hiding content.
  - Incorrect `href` values or files in different folders.
- **One-Line Summary**: The two-page inspirational figure website uses HTML text formatting, quotation, and comment elements to create a structured, styled, and navigable site, viewable in a browser after saving as HTML files.