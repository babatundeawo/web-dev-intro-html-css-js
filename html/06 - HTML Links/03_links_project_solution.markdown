# Solution and Explanation for HTML Weekly Project: Two-Page Space Exploration Website

This markdown provides the code solution for the weekly project from the HTML Links tutorial, which involves creating a two-page website about space exploration. The homepage includes links to an external site and a local Details page, while the Details page includes an email link, a bookmark link, and a link back to the homepage, all styled with internal CSS. The solution uses the `<a>` tag with `href`, `target`, `title`, and `id` attributes, and comments for documentation. The explanation follows the instructional framework, ensuring beginner-friendly guidance with plain language, metaphors, and detailed breakdowns of the code, including expected outputs, visual cues, common errors, and validation checks.

---

## Section 1 — Topical Explanations

The weekly project requires building a two-page website: a homepage (`index.html`) with an external link (to NASA) and a local link (to `details.html`), and a Details page (`details.html`) with an email link, a bookmark link, and a link back to the homepage. Both pages use internal CSS to style links (`a:link`, `a:visited`, `a:hover`, `a:active`) and include comments for clarity. The solution uses a space exploration theme, with accessibility features like `title` attributes and clear navigation. Below are the solutions for all files, followed by a step-by-step explanation.

### Solution Code

#### Homepage (`index.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Space Exploration</title>
    <style>
        a:link {
            color: green;
            text-decoration: none;
        }
        a:visited {
            color: purple;
            text-decoration: none;
        }
        a:hover {
            color: red;
            text-decoration: underline;
        }
        a:active {
            color: yellow;
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <!-- Main title -->
    <h1>Space Exploration</h1>
    <!-- External link -->
    <p><a href="https://www.nasa.gov/" target="_blank" title="Visit NASA">Explore NASA</a></p>
    <!-- Local link -->
    <p><a href="details.html" title="More about space exploration">Details</a></p>
    <!-- <p>Draft: Add more external links.</p> --> <!-- Hidden draft content -->
</body>
</html>
```

#### Details Page (`details.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Space Exploration Details</title>
    <style>
        a:link {
            color: darkblue;
            text-decoration: none;
        }
        a:visited {
            color: navy;
            text-decoration: none;
        }
        a:hover {
            color: orange;
            text-decoration: underline;
        }
        a:active {
            color: gold;
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <!-- Page title -->
    <h1>Space Exploration Details</h1>
    <!-- Email link -->
    <p><a href="mailto:info@spacefan.com" title="Contact us">Send Feedback</a></p>
    <!-- Bookmark link -->
    <p><a href="#facts" title="Jump to space facts">Space Facts</a></p>
    <!-- Bookmark section -->
    <h2 id="facts">Fascinating Space Facts</h2>
    <p>The universe is over 13 billion years old!</p>
    <!-- Local link back to homepage -->
    <p><a href="index.html" title="Return to homepage">Back to Homepage</a></p>
    <!-- <p>Draft: Add more facts.</p> --> <!-- Hidden draft content -->
</body>
</html>
```

### Explanation of the Solution

**Overview**: The project is like creating a two-page space exploration guidebook. The homepage is the cover, linking to an external resource (NASA) and a Details page, like chapters in a book. The Details page dives deeper with an email link, a bookmark to jump to a facts section, and a link back to the homepage. Internal CSS styles links like decorating signposts, and comments act as hidden notes for organization.

**Step-by-Step Instructions to Set Up**:
1. Open a text editor (e.g., Notepad or TextEdit).
2. Create a new folder (e.g., `space-website`).
3. Copy the code for `index.html` into a new file, save as `index.html` with UTF-8 encoding.
4. Copy the code for `details.html` into a new file, save as `details.html` in the same folder.
5. Double-click `index.html` to open in a browser and test navigation, links, styles, and comments.

**Line-by-Line Breakdown (for `index.html`)**:

- `<!DOCTYPE html>`:
  - **Purpose**: Declares the document as HTML5 for proper browser rendering.
  - **Metaphor**: Like a label on a guidebook, signaling it’s an HTML5 page.
  - **Output**: No visible output, but ensures correct rendering.
  - **Common Error**: Omitting this triggers "quirks mode," causing display issues.
    - **Fix**: Always include at the top.

- `<html lang="en">`:
  - **Purpose**: The root element, wrapping all content, with `lang="en"` for accessibility.
  - **Metaphor**: The guidebook’s cover, holding all pages together.
  - **Output**: No visible output, but sets up the structure.
  - **Common Error**: Missing `lang` reduces accessibility.
    - **Fix**: Include `lang="en"`.

- `<head>`:
  - **Purpose**: Contains metadata, the page title, and internal CSS.
  - **Metaphor**: The guidebook’s title page, providing context and styling rules.
  - **Output**: Affects browser behavior (e.g., tab title, link styles).

- `<title>Space Exploration</title>`:
  - **Purpose**: Sets the browser tab title.
  - **Output**: Browser tab displays "Space Exploration."
  - **Common Error**: Missing `<title>` shows a blank tab or file path.
    - **Fix**: Include a descriptive title.

- `<style>`:
  - **Purpose**: Defines internal CSS for link styling.
  - **Metaphor**: A decorating guide for all links in the guidebook.
  - **Output**: Applies styles to all `<a>` elements based on their state.

- `a:link {color: green; text-decoration: none;}`:
  - **Purpose**: Styles unvisited links with green color and no underline.
  - **Output**: Unvisited links are green without underlines.
  - **Common Error**: Misspelling `a:link` (e.g., `a:linkk`): Styles ignored.
    - **Fix**: Use correct pseudo-class (`a:link`).

- `a:visited {color: purple; text-decoration: none;}`:
  - **Purpose**: Styles visited links with purple color and no underline.
  - **Output**: Visited links are purple without underlines.
  - **Common Error**: Missing semicolon: Subsequent styles ignored.
    - **Fix**: Include semicolons after each property.

- `a:hover {color: red; text-decoration: underline;}`:
  - **Purpose**: Styles links on mouse-over with red color and an underline.
  - **Output**: Links turn red and underlined on hover.
  - **Common Error**: Incorrect pseudo-class: No hover effect.
    - **Fix**: Use `a:hover`.

- `a:active {color: yellow; text-decoration: underline;}`:
  - **Purpose**: Styles links when clicked with yellow color and an underline.
  - **Output**: Links turn yellow and underlined when clicked.
  - **Common Error**: Invalid property (e.g., `colour`): Ignored.
    - **Fix**: Use `color`.

- `<body>`:
  - **Purpose**: Contains all visible content (heading, links, comment).
  - **Metaphor**: The guidebook’s pages where content is displayed.
  - **Output**: Displays all content in the browser window.

- `<!-- Main title -->`:
  - **Purpose**: Documents the title section for clarity.
  - **Output**: Invisible in the browser, visible in "View Page Source."
  - **Common Error**: Missing `-->` hides unintended content.
    - **Fix**: Ensure `<!--` and `-->` are paired.

- `<h1>Space Exploration</h1>`:
  - **Purpose**: Displays the main title.
  - **Output**: Shows "Space Exploration" in large, bold text.
  - **Visual Cue**: Large, bold text at the top.
  - **Common Error**: Missing closing `</h1>`: May disrupt layout.
    - **Fix**: Ensure tags are closed.

- `<!-- External link -->`:
  - **Purpose**: Documents the external link section.
  - **Output**: Invisible in the browser.

- `<p><a href="https://www.nasa.gov/" target="_blank" title="Visit NASA">Explore NASA</a></p>`:
  - **Purpose**: Creates an external link to NASA, opening in a new tab.
  - **Attributes**:
    - `href="https://www.nasa.gov/"`: Specifies the destination.
    - `target="_blank"`: Opens in a new tab/window.
    - `title="Visit NASA"`: Shows a tooltip on hover.
  - **Output**: Shows "Explore NASA" as clickable text; clicking opens NASA in a new tab.
  - **Visual Cue**: Green (unvisited) or purple (visited), no underline until hover (red, underlined).
  - **Common Error**: Invalid URL (e.g., `htp://`): Broken link.
    - **Fix**: Use correct URL (`https://`).

- `<!-- Local link -->`:
  - **Purpose**: Documents the local link section.
  - **Output**: Invisible in the browser.

- `<p><a href="details.html" title="More about space exploration">Details</a></p>`:
  - **Purpose**: Links to the Details page.
  - **Attributes**:
    - `href="details.html"`: Points to a file in the same folder.
    - `title="More about space exploration"`: Shows a tooltip.
  - **Output**: Shows "Details" as clickable text; clicking navigates to `details.html`.
  - **Visual Cue**: Green/purple text, no underline until hover.
  - **Common Error**: Missing `details.html` or wrong path: Broken link.
    - **Fix**: Ensure `details.html` exists in the same folder.

- `<!-- <p>Draft: Add more external links.</p> -->`:
  - **Purpose**: Hides a draft paragraph for future use.
  - **Output**: Invisible in the browser.
  - **Common Error**: Incorrect comment syntax: Content may display.
    - **Fix**: Use `<!-- -->` correctly.

**Line-by-Line Breakdown (for `details.html`)**:

- Structure mirrors `index.html` with `<!DOCTYPE html>`, `<html lang="en">`, `<head>`, and `<title>Space Exploration Details</title>`, serving the same purposes.
- `<style>`:
  - Styles links with `a:link` (dark blue, no underline), `a:visited` (navy, no underline), `a:hover` (orange, underlined), `a:active` (gold, underlined).
  - **Common Error**: Missing curly braces or semicolons: Invalid CSS.
    - **Fix**: Use proper syntax `{property: value;}`.
- `<body>`: Contains visible content.
- `<!-- Page title -->`: Documents the title section.
- `<h1>Space Exploration Details</h1>`: Displays the page title.
- `<!-- Email link -->`: Documents the email link section.
- `<p><a href="mailto:info@spacefan.com" title="Contact us">Send Feedback</a></p>`:
  - **Purpose**: Creates a link to open an email client.
  - **Output**: Shows "Send Feedback" as clickable text; clicking opens an email client with `info@spacefan.com`.
  - **Visual Cue**: Dark blue/navy text, orange and underlined on hover.
  - **Common Error**: Invalid `mailto` syntax: Doesn’t open email client.
    - **Fix**: Use `mailto:email@domain.com`.
- `<!-- Bookmark link -->`: Documents the bookmark link section.
- `<p><a href="#facts" title="Jump to space facts">Space Facts</a></p>`:
  - **Purpose**: Links to a bookmark section on the same page.
  - **Output**: Shows "Space Facts" as clickable text; clicking scrolls to the `facts` section.
  - **Visual Cue**: Dark blue/navy text, orange and underlined on hover.
  - **Common Error**: Missing `id="facts"`: Link doesn’t scroll.
    - **Fix**: Ensure `id` matches `href="#id"`.
- `<!-- Bookmark section -->`: Documents the bookmark section.
- `<h2 id="facts">Fascinating Space Facts</h2>`:
  - **Purpose**: Creates a bookmark section with an `id`.
  - **Output**: Shows "Fascinating Space Facts" as a subheading.
  - **Visual Cue**: Smaller, bold text.
- `<p>The universe is over 13 billion years old!</p>`: Adds content to the bookmark section.
- `<!-- Local link back to homepage -->`: Documents the back link.
- `<p><a href="index.html" title="Return to homepage">Back to Homepage</a></p>`:
  - **Purpose**: Links back to the homepage.
  - **Output**: Shows "Back to Homepage" as clickable text; clicking navigates to `index.html`.
  - **Visual Cue**: Dark blue/navy text, orange and underlined on hover.
- `<!-- <p>Draft: Add more facts.</p> -->`: Hides a draft paragraph.

**Expected Output in Browser**:

- For `index.html`:
  - Browser tab: "Space Exploration"
  - Page content:
    ```
    Space Exploration [large, bold text]
    Explore NASA [green/purple text, no underline, red and underlined on hover, opens new tab]
    Details [green/purple text, no underline, red and underlined on hover, navigates to details.html]
    ```

- For `details.html`:
  - Browser tab: "Space Exploration Details"
  - Page content:
    ```
    Space Exploration Details [large, bold text]
    Send Feedback [dark blue/navy text, no underline, orange and underlined on hover, opens email client]
    Space Facts [dark blue/navy text, no underline, orange and underlined on hover, scrolls to section]
    Fascinating Space Facts [smaller, bold text]
    The universe is over 13 billion years old! [normal text]
    Back to Homepage [dark blue/navy text, no underline, orange and underlined on hover, navigates to index.html]
    ```

**Side Effects**: None (static HTML/CSS; email link may open an email client).

**Visual Cues**:
- Links are green/purple (homepage) or dark blue/navy (details), with no underline until hover (red/orange, underlined).
- Tooltips appear on hover for links with `title`.
- Bookmark link scrolls to the "Fascinating Space Facts" section.
- Comments are invisible in the browser.

**How to Test**:
1. Save both files in the same folder (e.g., `space-website`).
2. Open `index.html` in a browser by double-clicking.
3. Verify:
   - Browser tabs show correct titles.
   - External link opens NASA in a new tab.
   - Local links navigate between `index.html` and `details.html`.
   - Email link opens an email client with `info@spacefan.com`.
   - Bookmark link scrolls to "Fascinating Space Facts."
   - CSS styles apply (color changes, no underline until hover).
   - Comments are invisible but visible in "View Page Source."
4. Use a screen reader (if available) to confirm accessibility.

**Common Errors and Troubleshooting**:
- **Error**: Links don’t work.
  - **Cause**: Incorrect `href` (e.g., wrong URL, path, or missing `details.html`).
    - **Fix**: Use correct URLs (`https://`) and ensure files are in the same folder.
- **Error**: Bookmark doesn’t scroll.
  - **Cause**: Missing or mismatched `id` (e.g., `href="#fact"`).
    - **Fix**: Ensure `href="#id"` matches `id` value.
- **Error**: Email link doesn’t open.
  - **Cause**: Invalid `mailto` syntax.
    - **Fix**: Use `mailto:email@domain.com`.
- **Error**: Styles don’t apply.
  - **Cause**: Incorrect pseudo-class or missing semicolons.
    - **Fix**: Use correct syntax (e.g., `a:link`, `color: green;`).
- **Error**: Page shows code.
  - **Cause**: Saved as `.txt`.
    - **Fix**: Save as `.html`.

**Validation Checks**:
- Confirm files start with `<!DOCTYPE html>` and include `<html lang="en">`.
- Check browser tabs for correct titles.
- Verify all links (external, local, email, bookmark) function correctly.
- Ensure CSS styles apply and comments are hidden.
- Confirm `href`, `target`, `title`, and `id` attributes are used.

**Metaphor for the Whole Process**: Building this website is like creating a two-page guidebook about space exploration. The homepage is the cover with signposts to external resources and deeper details, while the Details page offers more information with quick access to a facts section and a way to contact the author. CSS decorates the signposts, and comments keep the guidebook organized.

---

## Completion Checklist

- **Learning Goals**:
  - Use `<a>` with `href`, `target`, and `title` attributes.
  - Create bookmarks with `id` and `href="#id"`.
  - Style links with CSS (`a:link`, `a:visited`, `a:hover`, `a:active`).
  - Create and link multiple HTML pages.
- **Runnable Example**: The code above (`index.html`, `details.html`) is a complete, runnable solution.
- **Checklist for Completion**:
  - [ ] Files start with `<!DOCTYPE html>` and include `<html lang="en">`.
  - [ ] Include external, local, email, and bookmark links.
  - [ ] Use `href`, `target`, `title`, and `id` attributes.
  - [ ] Apply CSS to style link states.
  - [ ] Include at least one comment per file.
  - [ ] Links navigate correctly (external, local, email, bookmark).
  - [ ] Saved as `.html` and renders correctly in a browser.
- **Common Pitfalls**:
  - Incorrect `href` values (e.g., wrong URL or path).
  - Missing `id` for bookmarks.
  - Invalid `mailto` syntax.
  - Incorrect CSS pseudo-classes or missing semicolons.
  - Files in different folders causing broken links.
- **One-Line Summary**: The two-page space exploration website uses `<a>` tags with `href`, `target`, and `title` for external, local, email, and bookmark links, styled with CSS and enhanced with comments, viewable in a browser after saving as HTML files.