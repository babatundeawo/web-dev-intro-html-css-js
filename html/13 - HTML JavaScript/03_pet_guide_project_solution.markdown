# Solution and Explanation for HTML JavaScript Weekly Project: Two-Page Pet Guide Website

This markdown provides the code solution for the weekly project from the HTML JavaScript tutorial, which involves creating a two-page website about a pet guide. The homepage (`index.html`) includes an image with `id="petImage"`, a button to change the image’s `src` attribute, a heading, and a link to the Details page. The Details page (`details.html`) includes a paragraph with `id="demo"`, a button to change its text and style, a `<noscript>` tag for fallback, a heading, and a link back to the homepage. Both pages use `<script>` for JavaScript, comments for documentation, and `lang="en"` for accessibility. The explanation follows the instructional framework, ensuring beginner-friendly guidance with plain language, metaphors, and detailed breakdowns of the code, including expected outputs, visual cues, common errors, and validation checks.

---

## Section 1 — Topical Explanations

The weekly project requires building a two-page website about a pet guide. The homepage features an image that changes (e.g., from `dog.jpg` to `cat.jpg`) when a button is clicked, using `document.getElementById()` to modify the `src` attribute, along with a heading and navigation to the Details page. The Details page has a paragraph that changes text and style (e.g., color) when a button is clicked, a `<noscript>` tag for users with JavaScript disabled, and navigation back to the homepage. Both pages include comments for clarity and use `<script>` for interactivity. The theme is a pet guide to engage learners. Below are the solutions for both files, followed by a step-by-step explanation.

### Solution Code

#### Homepage (`index.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Pet Guide</title>
</head>
<body>
    <!-- Main title -->
    <h1>Pet Guide</h1>
    <img id="petImage" src="dog.jpg" alt="Dog Image" width="200">
    <button onclick="changeImage()">Change Pet</button>
    <p><a href="details.html" title="Learn more about pets">Pet Details</a></p>
    <!-- JavaScript to change image -->
    <script>
        function changeImage() {
            document.getElementById("petImage").src = "cat.jpg";
        }
    </script>
    <!-- <p>Draft: Add more pets later.</p> --> <!-- Hidden draft content -->
</body>
</html>
```

#### Details Page (`details.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Pet Details</title>
</head>
<body>
    <!-- Main title -->
    <h1>Pet Details</h1>
    <p id="demo">Learn about your pet!</p>
    <button onclick="changeText()">Change Details</button>
    <noscript>Sorry, your browser does not support JavaScript!</noscript>
    <p><a href="index.html" title="Back to pet guide">Back to Pet Guide</a></p>
    <!-- JavaScript to change text and style -->
    <script>
        function changeText() {
            document.getElementById("demo").innerHTML = "Discover fun pet facts!";
            document.getElementById("demo").style.color = "blue";
        }
    </script>
    <!-- <p>Draft: Add more details later.</p> --> <!-- Hidden draft content -->
</body>
</html>
```

### Explanation of the Solution

**Overview**: The project is like creating a two-page pet guidebook. The homepage is a showcase page with a photo frame (image) that switches pictures (e.g., dog to cat) when a button is clicked, using JavaScript to change the `src` attribute, plus a heading and a link to the Details page. The Details page is an information sheet with a paragraph that updates its text and color when a button is clicked, a fallback message for non-JavaScript users, and a link back to the homepage. Both pages use `<script>` for interactivity, comments for organization, and navigation for connectivity, making the code beginner-friendly.

**Step-by-Step Instructions to Set Up**:
1. Open a text editor (e.g., Notepad or TextEdit).
2. Create a new folder (e.g., `pet-guide-website`).
3. Copy the code for `index.html` and `details.html` into separate files, saving them with UTF-8 encoding in the `pet-guide-website` folder.
4. Add two placeholder images named `dog.jpg` and `cat.jpg` to the same folder (e.g., download sample images or create 200x200 pixel images).
5. Double-click `index.html` to open in a browser and test the image swap, text/style change, navigation, and `<noscript>` functionality.

**Line-by-Line Breakdown (for `index.html`)**:

- `<!DOCTYPE html>`:
  - **Purpose**: Declares HTML5 for proper rendering.
  - **Metaphor**: Like a label on a pet guidebook, signaling it’s an HTML5 page.
  - **Output**: No visible output, ensures correct rendering.
  - **Common Error**: Omitting causes "quirks mode."
    - **Fix**: Include at the top.

- `<html lang="en">`:
  - **Purpose**: Root element with `lang="en"` for accessibility.
  - **Metaphor**: The guidebook’s cover, holding all content.
  - **Output**: No visible output, sets structure.
  - **Common Error**: Missing `lang` reduces accessibility.
    - **Fix**: Include `lang="en"`.

- `<head>`:
  - **Purpose**: Contains metadata and title.
  - **Metaphor**: The guidebook’s title page.
  - **Output**: Affects tab title.

- `<title>Pet Guide</title>`:
  - **Purpose**: Sets tab title for SEO and clarity.
  - **Output**: Tab shows "Pet Guide."
  - **Visual Cue**: Title in tab, toolbar, favorites.
  - **Common Error**: Missing `<title>` shows file path.
    - **Fix**: Include descriptive title.

- `<body>`:
  - **Purpose**: Contains visible content.
  - **Metaphor**: The guidebook’s pages.
  - **Output**: Displays content in the browser.

- `<!-- Main title -->`:
  - **Purpose**: Documents the heading.
  - **Output**: Invisible.
  - **Common Error**: Incorrect syntax: Content displays.
    - **Fix**: Use `<!-- -->`.

- `<h1>Pet Guide</h1>`:
  - **Purpose**: Displays main heading.
  - **Output**: Large, bold "Pet Guide."
  - **Visual Cue**: Bold text at top.
  - **Common Error**: Missing `</h1>`: Layout issues.
    - **Fix**: Close tag.

- `<img id="petImage" src="dog.jpg" alt="Dog Image" width="200">`:
  - **Purpose**: Displays an image with `id="petImage"` for JavaScript targeting.
  - **Output**: Shows `dog.jpg` (200px wide).
  - **Visual Cue**: Dog image appears.
  - **Common Error**: Missing `dog.jpg`: Broken image icon.
    - **Fix**: Ensure file exists in folder.
  - **Common Error**: Missing `id`: JavaScript fails.
    - **Fix**: Include `id="petImage"`.

- `<button onclick="changeImage()">Change Pet</button>`:
  - **Purpose**: Triggers the `changeImage()` function.
  - **Output**: Clickable "Change Pet" button.
  - **Visual Cue**: Hand cursor on hover.
  - **Common Error**: Incorrect function name: Button does nothing.
    - **Fix**: Match `onclick="changeImage()"`.

- `<p><a href="details.html" title="Learn more about pets">Pet Details</a></p>`:
  - **Purpose**: Links to Details page.
  - **Output**: Clickable "Pet Details" text.
  - **Visual Cue**: Hand cursor, tooltip on hover.
  - **Common Error**: Missing `details.html`: Broken link.
    - **Fix**: Ensure file exists.

- `<!-- JavaScript to change image -->`:
  - **Purpose**: Documents JavaScript section.
  - **Output**: Invisible.

- `<script>`:
  - **Purpose**: Contains JavaScript for interactivity.
  - **Metaphor**: A recipe card for the button’s action.
  - **Output**: Enables image swap.

- `function changeImage() { document.getElementById("petImage").src = "cat.jpg"; }`:
  - **Purpose**: Changes image `src` to `cat.jpg`.
  - **Output**: Image changes to `cat.jpg` on click.
  - **Visual Cue**: Cat image replaces dog.
  - **Common Error**: Missing `cat.jpg`: Broken image.
    - **Fix**: Ensure file exists.
  - **Common Error**: Incorrect `id`: No change.
    - **Fix**: Use `id="petImage"`.

- `<!-- <p>Draft: Add more pets later.</p> -->`:
  - **Purpose**: Hides draft note.
  - **Output**: Invisible.
  - **Common Error**: Incorrect syntax: Content displays.
    - **Fix**: Use `<!-- -->`.

**Line-by-Line Breakdown (for `details.html`)**:

- Structure mirrors `index.html` with `<!DOCTYPE html>`, `<html lang="en">`, `<head>`, and `<title>Pet Details</title>`, serving similar purposes.
- `<h1>Pet Details</h1>`: Displays heading.
- `<p id="demo">Learn about your pet!</p>`:
  - **Purpose**: Paragraph with `id="demo"` for JavaScript.
  - **Output**: Displays "Learn about your pet!".
  - **Visual Cue**: Plain text paragraph.
  - **Common Error**: Missing `id`: JavaScript fails.
    - **Fix**: Include `id="demo"`.

- `<button onclick="changeText()">Change Details</button>`:
  - **Purpose**: Triggers `changeText()` function.
  - **Output**: Clickable "Change Details" button.
  - **Visual Cue**: Hand cursor on hover.

- `<noscript>Sorry, your browser does not support JavaScript!</noscript>`:
  - **Purpose**: Shows fallback message if JavaScript is disabled.
  - **Output**: Displays message only if JavaScript is off.
  - **Visual Cue**: Text appears in place of JavaScript content.
  - **Common Error**: Misplaced `<noscript>`: May not display.
    - **Fix**: Place in `<body>`.

- `<p><a href="index.html" title="Back to pet guide">Back to Pet Guide</a></p>`:
  - **Purpose**: Links back to homepage.
  - **Output**: Clickable "Back to Pet Guide" text.

- `<!-- JavaScript to change text and style -->` and `<script>`:
  - **Purpose**: Documents and contains JavaScript.
  - **Output**: Enables text and style changes.

- `function changeText() { document.getElementById("demo").innerHTML = "Discover fun pet facts!"; document.getElementById("demo").style.color = "blue"; }`:
  - **Purpose**: Changes paragraph text and color.
  - **Output**: On click, `<p>` changes to:
    ```
    Discover fun pet facts! [blue text]
    ```
  - **Visual Cue**: Text and color change.
  - **Common Error**: Incorrect property: No style change.
    - **Fix**: Use `style.color`.

- `<!-- <p>Draft: Add more details later.</p> -->`: Hides draft note.

**Expected Output in Browser**:

- For `index.html`:
  - Browser tab: "Pet Guide."
  - Page content:
    ```
    Pet Guide [large, bold text]
    [dog.jpg image, 200px wide]
    [Change Pet button]
    Pet Details [clickable link]
    ```
  - Clicking "Change Pet": Image changes to `cat.jpg`.

- For `details.html`:
  - Browser tab: "Pet Details."
  - Page content (JavaScript enabled):
    ```
    Pet Details [large, bold text]
    Learn about your pet!
    [Change Details button]
    Back to Pet Guide [clickable link]
    ```
  - Clicking "Change Details":
    ```
    Discover fun pet facts! [blue text]
    ```
  - JavaScript disabled:
    ```
    Pet Details [large, bold text]
    Sorry, your browser does not support JavaScript!
    Back to Pet Guide [clickable link]
    ```

**Side Effects**: Button clicks trigger image swap (homepage) or text/style change (Details page); `<noscript>` displays if JavaScript is disabled.

**Visual Cues**:
- Homepage: Image changes from dog to cat on button click.
- Details page: Paragraph text and color change; `<noscript>` text appears if JavaScript is off.
- Links show hand cursor and tooltips.
- Comments are invisible.

**How to Test**:
1. Save both files in a folder (e.g., `pet-guide-website`) with `dog.jpg` and `cat.jpg`.
2. Open `index.html` in a browser.
3. Verify:
   - Tabs show correct titles.
   - Homepage shows image, changes on button click.
   - Details page shows text change and blue color on button click.
   - Disable JavaScript (browser settings) to confirm `<noscript>` message.
   - Navigation links work.
   - Comments are invisible.
4. Use a screen reader to confirm accessibility.

**Common Errors and Troubleshooting**:
- **Error**: Button does nothing.
  - **Cause**: Incorrect `id` or function name.
    - **Fix**: Match `id` and `onclick`.
- **Error**: Image doesn’t change.
  - **Cause**: Missing `cat.jpg` or incorrect `id`.
    - **Fix**: Ensure file exists, use `id="petImage"`.
- **Error**: Text or color doesn’t change.
  - **Cause**: `<script>` before `<p>` or incorrect property.
    - **Fix**: Place `<script>` after `<p>`, use `style.color`.
- **Error**: `<noscript>` doesn’t show.
  - **Cause**: JavaScript enabled or misplaced tag.
    - **Fix**: Disable JavaScript, place in `<body>`.
- **Error**: Links don’t work.
  - **Cause**: Missing files.
    - **Fix**: Ensure both files exist.

**Validation Checks**:
- Confirm files start with `<!DOCTYPE html>` and include `<html lang="en">`.
- Verify image swap, text/style change, `<noscript>`, and navigation.
- Check comment visibility.
- Test with a screen reader.

**Metaphor for the Whole Process**: Building this website is like creating a two-page pet guidebook where the homepage switches pet photos like a digital frame, and the Details page updates pet facts like a dynamic sign, with a backup message for non-JavaScript users.

---

## Completion Checklist

- **Learning Goals**:
  - Use `<script>` and `document.getElementById()`.
  - Change attributes (`src`), content (`innerHTML`), and styles (`style.color`).
  - Use `<noscript>` for fallback.
  - Include navigation and comments.
- **Runnable Example**: The code above (`index.html`, `details.html`) is a complete, runnable solution (requires `dog.jpg` and `cat.jpg`).
- **Checklist for Completion**:
  - [ ] Files start with `<!DOCTYPE html>` and include `<html lang="en">`.
  - [ ] Include `<script>`, `document.getElementById()`, and `<noscript>`.
  - [ ] Change image `src`, text, and style.
  - [ ] Include navigation and comments.
  - [ ] Image swap, text/style change, and `<noscript>` work.
  - [ ] Saved as `.html` with images, displays in a browser.
- **Common Pitfalls**:
  - Missing `id` values causing JavaScript errors.
  - Incorrect JavaScript properties (e.g., `color` instead of `style.color`).
  - Missing image files.
  - `<script>` before element declaration.
  - Missing navigation files.
- **One-Line Summary**: The two-page pet guide website uses `<script>` to change images, text, and styles, with `<noscript>` for fallback, viewable in a browser after saving as HTML files with images.