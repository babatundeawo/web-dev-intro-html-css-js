# Solution and Explanation for HTML Weekly Project: Two-Page Hobby Website

This markdown provides the code solution for the weekly project from the HTML CSS tutorial, which involves creating a two-page website about a favorite hobby (photography) using inline, internal, and external CSS to apply `background-color`, `color`, `font-family`, `font-size`, `border`, `padding`, and `margin` properties, with comments for documentation. The explanation follows the instructional framework, ensuring beginner-friendly guidance with plain language, metaphors, and detailed breakdowns of the code, including expected outputs, visual cues, common errors, and validation checks.

---

## Section 1 — Topical Explanations

The weekly project requires building a two-page website: a homepage (`index.html`) introducing the hobby with a styled title, introduction, and bordered section, and a Details page (`details.html`) with more information, styled similarly and linked back to the homepage. The pages use inline CSS for headings, internal CSS for paragraphs, and external CSS for bordered sections, with comments to document or hide content. Below are the solutions for all files, followed by a step-by-step explanation.

### Solution Code

#### Homepage (`index.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Photography Hobby</title>
    <style>
        p {
            color: green;
            font-family: arial;
            font-size: 120%;
        }
    </style>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Main title with inline CSS -->
    <h1 style="background-color:lightgray; color:blue;">Photography Hobby</h1>
    <!-- Introduction -->
    <p>I love capturing moments with my camera!</p>
    <!-- Fun fact with external CSS -->
    <div>Photography is about creativity and light.</div>
    <!-- Navigation link -->
    <p><a href="details.html">Go to Details</a></p>
    <!-- <p>Draft: Add camera types.</p> --> <!-- Hidden draft content -->
</body>
</html>
```

#### Details Page (`details.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Why I Love Photography</title>
    <style>
        p {
            color: darkblue;
            font-family: times;
            font-size: 120%;
            margin: 20px;
        }
    </style>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Page title with inline CSS -->
    <h1 style="background-color:lightgray; color:blue;">Why I Love Photography</h1>
    <!-- Details -->
    <p>Photography lets me freeze special moments like sunsets or family gatherings.</p>
    <!-- Bordered section with external CSS -->
    <div>I enjoy experimenting with angles and lighting.</div>
    <!-- Navigation link -->
    <p><a href="index.html">Back to Homepage</a></p>
    <!-- <p>Draft: Include favorite photographers.</p> --> <!-- Hidden draft content -->
</body>
</html>
```

#### External CSS (`styles.css`)

```css
div {
    border: 2px solid powderblue;
    padding: 20px;
}
```

### Explanation of the Solution

**Overview**: The project is like creating a two-page photo album about photography. The homepage introduces the hobby with a highlighted title, a styled introduction, and a bordered section, while the Details page dives deeper with similar styling and navigation. Inline CSS adds unique touches to headings, internal CSS ensures consistent paragraph styling, and external CSS applies reusable borders and padding. Comments keep the code organized, like hidden notes in the album.

**Step-by-Step Instructions to Set Up**:
1. Open a text editor (e.g., Notepad or TextEdit).
2. Create a new folder (e.g., `photography-hobby`) to store all files.
3. Copy the code for `index.html` into a new file, save as `index.html` with UTF-8 encoding.
4. Copy the code for `details.html` into a new file, save as `details.html` in the same folder.
5. Copy the code for `styles.css` into a new file, save as `styles.css` in the same folder.
6. Double-click `index.html` to open in a browser and test navigation, styles, and comments.

**Line-by-Line Breakdown (for `index.html`)**:

- `<!DOCTYPE html>`:
  - **Purpose**: Declares the document as HTML5 for proper browser rendering.
  - **Metaphor**: Like a label on a photo album, signaling it’s an HTML5 page.
  - **Output**: No visible output, but ensures correct rendering.
  - **Common Error**: Omitting this triggers "quirks mode," causing display issues.
    - **Fix**: Always include at the top.

- `<html lang="en">`:
  - **Purpose**: The root element, wrapping all content, with `lang="en"` for accessibility.
  - **Metaphor**: The album’s cover, holding all pages together.
  - **Output**: No visible output, but sets up the structure.
  - **Common Error**: Missing `lang` reduces accessibility.
    - **Fix**: Include `lang="en"`.

- `<head>`:
  - **Purpose**: Contains metadata, internal CSS, and the external CSS link.
  - **Metaphor**: The album’s title page, providing context and styling rules.
  - **Output**: Affects browser behavior (e.g., tab title, styles).

- `<title>Photography Hobby</title>`:
  - **Purpose**: Sets the browser tab title.
  - **Output**: Browser tab displays "Photography Hobby."
  - **Common Error**: Missing `<title>` shows a blank tab or file path.
    - **Fix**: Include a descriptive title.

- `<style>`:
  - **Purpose**: Defines internal CSS for paragraph styling.
  - **Metaphor**: A decorating guide for all paragraphs in the album.
  - **Output**: Applies styles to all `<p>` elements.

- `p {color: green; font-family: arial; font-size: 120%;}`:
  - **Purpose**: Styles all `<p>` elements with green text, Arial font, and 120% size.
  - **Output**: Paragraphs are green, in Arial, slightly larger than default.
  - **Common Error**: Missing semicolon (e.g., `color: green`): Subsequent styles ignored.
    - **Fix**: Include semicolons after each property-value pair.

- `<link rel="stylesheet" href="styles.css">`:
  - **Purpose**: Links to the external CSS file for `<div>` styling.
  - **Output**: Applies `styles.css` rules to matching elements.
  - **Common Error**: Incorrect `href` or missing `rel="stylesheet"`: Styles don’t apply.
    - **Fix**: Ensure `href` matches file name and include `rel="stylesheet"`.

- `<body>`:
  - **Purpose**: Contains all visible content (heading, paragraphs, div, link, comment).
  - **Metaphor**: The album’s pages where photos and captions are displayed.
  - **Output**: Displays all content in the browser window.

- `<!-- Main title with inline CSS -->`:
  - **Purpose**: Documents the title section for clarity.
  - **Output**: Invisible in the browser, visible in "View Page Source."
  - **Common Error**: Missing `-->` hides unintended content.
    - **Fix**: Ensure `<!--` and `-->` are paired.

- `<h1 style="background-color:lightgray; color:blue;">Photography Hobby</h1>`:
  - **Purpose**: Displays the title with inline CSS for background and text color.
  - **Output**: Shows "Photography Hobby" in large, bold, blue text on a light gray background.
  - **Visual Cue**: Large, bold blue text with a gray background.
  - **Common Error**: Misspelling `lightgray` (e.g., `lightgrey`): No background color.
    - **Fix**: Use exact color name (`lightgray`).

- `<!-- Introduction -->`:
  - **Purpose**: Documents the introduction section.
  - **Output**: Invisible in the browser.

- `<p>I love capturing moments with my camera!</p>`:
  - **Purpose**: Introduces the hobby, styled by internal CSS.
  - **Output**: Shows the paragraph in green, Arial font, 120% size.
  - **Visual Cue**: Green text with paragraph spacing.
  - **Common Error**: Placing `<p>` outside `<body>`: May not display.
    - **Fix**: Ensure content is inside `<body>`.

- `<!-- Fun fact with external CSS -->`:
  - **Purpose**: Documents the bordered section.
  - **Output**: Invisible in the browser.

- `<div>Photography is about creativity and light.</div>`:
  - **Purpose**: Highlights a fun fact, styled by external CSS.
  - **Output**: Shows the text inside a 2px powderblue border with 20px padding.
  - **Visual Cue**: Text within a light blue border, spaced inside.
  - **Common Error**: Missing `styles.css`: Border and padding don’t apply.
    - **Fix**: Ensure `styles.css` exists in the same folder.

- `<!-- Navigation link -->`:
  - **Purpose**: Documents the navigation link.
  - **Output**: Invisible in the browser.

- `<p><a href="details.html">Go to Details</a></p>`:
  - **Purpose**: Links to the Details page, styled by internal CSS.
  - **Output**: Shows "Go to Details" as a clickable link in green, Arial font.
  - **Visual Cue**: Underlined, typically blue text (browser default for links).
  - **Common Error**: Incorrect `href` or missing `details.html`: Broken link.
    - **Fix**: Ensure `details.html` exists in the same folder.

- `<!-- <p>Draft: Add camera types.</p> -->`:
  - **Purpose**: Hides a draft paragraph for future use.
  - **Output**: Invisible in the browser.
  - **Common Error**: Incorrect comment syntax: Content may display.
    - **Fix**: Use `<!-- -->` correctly.

**Line-by-Line Breakdown (for `details.html`)**:

- The structure mirrors `index.html` with `<!DOCTYPE html>`, `<html lang="en">`, `<head>`, and `<title>Why I Love Photography</title>`, serving the same purposes.
- `<style>`:
  - `p {color: darkblue; font-family: times; font-size: 120%; margin: 20px;}`: Styles paragraphs with dark blue text, Times font, 120% size, and 20px outer spacing.
  - **Common Error**: Missing units for `margin` (e.g., `margin: 20`): Ignored.
    - **Fix**: Include units (e.g., `20px`).
- `<link rel="stylesheet" href="styles.css">`: Links to the same external CSS file.
- `<body>`: Contains visible content.
- `<!-- Page title with inline CSS -->`: Documents the title section.
- `<h1 style="background-color:lightgray; color:blue;">Why I Love Photography</h1>`: Displays the title with inline CSS.
- `<!-- Details -->`: Documents the details section.
- `<p>Photography lets me freeze special moments...</p>`: Describes the hobby, styled by internal CSS.
- `<!-- Bordered section with external CSS -->`: Documents the bordered section.
- `<div>I enjoy experimenting with angles and lighting.</div>`: Shows text in a bordered section, styled by external CSS.
- `<!-- Navigation link -->`: Documents the navigation link.
- `<p><a href="index.html">Back to Homepage</a></p>`: Links back to the homepage, styled by internal CSS.
- `<!-- <p>Draft: Include favorite photographers.</p> -->`: Hides a draft paragraph.

**External CSS (`styles.css`)**:

- `div {border: 2px solid powderblue; padding: 20px;}`:
  - **Purpose**: Styles all `<div>` elements with a 2px powderblue border and 20px padding.
  - **Output**: Applies to `<div>` elements in both pages.
  - **Common Error**: Missing semicolon or curly braces: Invalid syntax.
    - **Fix**: Use proper CSS syntax.

**Expected Output in Browser**:

- For `index.html`:
  - Browser tab: "Photography Hobby"
  - Page content:
    ```
    Photography Hobby [large, bold, blue text on a light gray background]
    I love capturing moments with my camera! [green, Arial font, 120% size]
    Photography is about creativity and light. [inside a 2px powderblue border with 20px padding]
    Go to Details [clickable link in green, Arial font]
    ```

- For `details.html`:
  - Browser tab: "Why I Love Photography"
  - Page content:
    ```
    Why I Love Photography [large, bold, blue text on a light gray background]
    Photography lets me freeze special moments like sunsets or family gatherings. [dark blue, Times font, 120% size, 20px margin]
    I enjoy experimenting with angles and lighting. [inside a 2px powderblue border with 20px padding]
    Back to Homepage [clickable link in dark blue, Times font]
    ```

**Side Effects**: None (static HTML/CSS displays content).

**Visual Cues**:
- Headings have a light gray background and blue text.
- Paragraphs use green (homepage) or dark blue (details) text, with Arial or Times fonts.
- `<div>` elements have a powderblue border and padding.
- Links are underlined, typically blue (browser default).
- Comments are invisible in the browser.

**How to Test**:
1. Save all files in the same folder (e.g., `photography-hobby`).
2. Open `index.html` in a browser by double-clicking.
3. Verify:
   - Browser tabs show correct titles.
   - Inline CSS (headings), internal CSS (paragraphs), and external CSS (divs) apply correctly.
   - Colors, fonts, sizes, borders, padding, and margins display as expected.
   - Links navigate between pages.
   - Comments are invisible but visible in "View Page Source."
4. Use a screen reader (if available) to confirm accessibility.

**Common Errors and Troubleshooting**:
- **Error**: Styles don’t apply.
  - **Cause**: Misspelled properties (e.g., `colour`) or color names (e.g., `lightgrey`).
    - **Fix**: Use correct names (`color`, `lightgray`).
- **Error**: External CSS doesn’t work.
  - **Cause**: Incorrect `href` or missing `styles.css`.
    - **Fix**: Ensure `href="styles.css"` and file exists in the same folder.
- **Error**: Links don’t work.
  - **Cause**: Incorrect `href` or files in different folders.
    - **Fix**: Ensure files are in the same folder and `href` matches file names.
- **Error**: Spacing or fonts incorrect.
  - **Cause**: Missing units (e.g., `margin: 20`) or invalid `font-family`.
    - **Fix**: Use units (e.g., `20px`) and valid fonts (e.g., `times`).
- **Error**: Page shows code.
  - **Cause**: Saved as `.txt`.
    - **Fix**: Save as `.html` or `.css`.

**Validation Checks**:
- Confirm files start with `<!DOCTYPE html>` and include `<html lang="en">`.
- Check browser tabs for titles.
- Verify all CSS methods and properties display correctly.
- Ensure links navigate and comments are hidden.
- Confirm inline, internal, and external CSS are used.

**Metaphor for the Whole Process**: Building this website is like assembling a two-page photo album about photography. The homepage is the cover with a highlighted title and styled captions, the Details page adds deeper stories with consistent formatting, and the external CSS is a shared style guide for borders. Comments are hidden notes for the album’s creator, keeping everything organized.

---

## Completion Checklist

- **Learning Goals**:
  - Use inline, internal, and external CSS.
  - Apply `background-color`, `color`, `font-family`, `font-size`, `border`, `padding`, and `margin`.
  - Create and link multiple HTML pages with a `.css` file.
  - Include comments for documentation.
- **Runnable Example**: The code above (`index.html`, `details.html`, `styles.css`) is a complete, runnable solution.
- **Checklist for Completion**:
  - [ ] Files start with `<!DOCTYPE html>` and include `<html lang="en">`.
  - [ ] Use inline, internal, and external CSS.
  - [ ] Apply `background-color`, `color`, `font-family`, `font-size`, `border`, `padding`, `margin`.
  - [ ] Include at least one comment per HTML file.
  - [ ] Links navigate between pages.
  - [ ] Styles display correctly.
  - [ ] Saved as `.html` and `.css` and renders correctly in a browser.
- **Common Pitfalls**:
  - Incorrect `href` in `<link>` or missing `rel="stylesheet"`.
  - Missing semicolons or curly braces in CSS.
  - Invalid `font-family` or missing units (e.g., `font-size:120`).
  - Incorrect `border` syntax (e.g., `border:powderblue`).
  - Files saved in different folders or with wrong extensions.
- **One-Line Summary**: The two-page photography website uses inline, internal, and external CSS to style text, backgrounds, borders, and spacing, with comments and navigation, viewable in a browser after saving as HTML and CSS files.