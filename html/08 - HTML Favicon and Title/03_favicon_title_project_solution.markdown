# Solution and Explanation for HTML Weekly Project: Two-Page Space Exploration Website

This markdown provides the code solution for the weekly project from the HTML Favicon and Title tutorial, which involves creating a two-page website about space exploration. The homepage includes a favicon, a descriptive title, an image, a heading, and a link to the Details page. The Details page includes a favicon, a descriptive title, a heading, and an image link back to the homepage. The solution uses `<link>` for favicons, `<title>` for page titles, `<img>` for images, and `<a>` for navigation, with comments for documentation and accessibility features like `alt` and `lang="en"`. The explanation follows the instructional framework, ensuring beginner-friendly guidance with plain language, metaphors, and detailed breakdowns of the code, including expected outputs, visual cues, common errors, and validation checks.

---

## Section 1 — Topical Explanations

The weekly project requires building a two-page website about space exploration: a homepage (`index.html`) with a favicon, a descriptive title, an image, a heading, and a link to a Details page (`details.html`), which includes a favicon, a title, a heading, and an image link back to the homepage. Both pages use comments for clarity and accessibility features. The theme is space exploration to engage learners. Below are the solutions for both files, followed by a step-by-step explanation.

### Solution Code

#### Homepage (`index.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Space Exploration Home</title>
    <link rel="icon" type="image/x-icon" href="images/favicon.ico">
    <style>
        a:link {
            color: white;
            text-decoration: none;
        }
        a:visited {
            color: lightgray;
            text-decoration: none;
        }
        a:hover {
            color: yellow;
            text-decoration: underline;
        }
        a:active {
            color: orange;
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <!-- Main title -->
    <h1>Space Exploration Home</h1>
    <!-- Embedded image -->
    <p><img src="rocket.jpg" alt="Rocket launching into space" style="width:200px;height:200px;"></p>
    <!-- Link to Details page -->
    <p><a href="details.html" title="More about space exploration">More Details</a></p>
    <!-- <p>Draft: Add background image later.</p> --> <!-- Hidden draft content -->
</body>
</html>
```

#### Details Page (`details.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Space Exploration Details</title>
    <link rel="icon" type="image/x-icon" href="images/favicon.ico">
</head>
<body>
    <!-- Main title -->
    <h1>Space Exploration Details</h1>
    <!-- Image link back to homepage -->
    <p>
        <a href="index.html" title="Return to homepage">
            <img src="home_icon.jpg" alt="Home icon" style="width:50px;height:50px;">
        </a>
    </p>
    <!-- <p>Draft: Add more content later.</p> --> <!-- Hidden draft content -->
</body>
</html>
```

### Explanation of the Solution

**Overview**: The project is like creating a two-page guidebook about space exploration. The homepage is the cover, featuring a favicon (like a logo), a descriptive title, a rocket image, and a link to the Details page. The Details page is an inner chapter with the same favicon, a title, and a clickable image to return to the homepage. Comments act as hidden notes for organization, and CSS styles enhance link appearance.

**Step-by-Step Instructions to Set Up**:
1. Open a text editor (e.g., Notepad or TextEdit).
2. Create a new folder (e.g., `space-website`).
3. Copy the code for `index.html` and `details.html` into separate files, saving them with UTF-8 encoding in the `space-website` folder.
4. Create an `images` subfolder and place sample images (`favicon.ico`, `rocket.jpg`, `home_icon.jpg`) in it (use any ICO/PNG for favicon and JPEG/PNG for images, renamed for testing).
5. Double-click `index.html` to open in a browser and test favicon, title, image, and navigation.

**Line-by-Line Breakdown (for `index.html`)**:

- `<!DOCTYPE html>`:
  - **Purpose**: Declares the document as HTML5 for proper rendering.
  - **Metaphor**: Like a label on a guidebook, signaling it’s an HTML5 page.
  - **Output**: No visible output, but ensures correct rendering.
  - **Common Error**: Omitting this triggers "quirks mode."
    - **Fix**: Always include at the top.

- `<html lang="en">`:
  - **Purpose**: Root element with `lang="en"` for accessibility.
  - **Metaphor**: The guidebook’s cover, holding all content.
  - **Output**: No visible output, but sets up structure.
  - **Common Error**: Missing `lang` reduces accessibility.
    - **Fix**: Include `lang="en"`.

- `<head>`:
  - **Purpose**: Contains metadata, title, favicon, and CSS.
  - **Metaphor**: The guidebook’s title page with styling rules.
  - **Output**: Affects browser behavior (tab title, favicon, link styles).

- `<title>Space Exploration Home</title>`:
  - **Purpose**: Sets the browser tab title, aiding SEO and clarity.
  - **Output**: Tab displays "Space Exploration Home."
  - **Visual Cue**: Title in tab, toolbar, and favorites.
  - **Common Error**: Missing `<title>` shows blank tab or file path.
    - **Fix**: Include a descriptive title.

- `<link rel="icon" type="image/x-icon" href="images/favicon.ico">`:
  - **Purpose**: Links a favicon to the page.
  - **Attributes**:
    - `rel="icon"`: Specifies favicon relationship.
    - `type="image/x-icon"`: Indicates ICO format.
    - `href="images/favicon.ico"`: Points to favicon in `images/`.
  - **Output**: Shows a small icon (e.g., 16x16 pixels) in the tab.
  - **Visual Cue**: Favicon appears; default browser icon if missing.
  - **Common Error**: Wrong `href`: Favicon doesn’t display.
    - **Fix**: Ensure `favicon.ico` is in `images/`.

- `<style>`:
  - **Purpose**: Defines CSS for link styling.
  - **Metaphor**: A decorating guide for links.
  - **Output**: Applies styles to links.

- `a:link {color: white; text-decoration: none;}`, `a:visited`, `a:hover`, `a:active`:
  - **Purpose**: Styles links (unvisited: white, no underline; visited: light gray; hovered: yellow, underlined; active: orange, underlined).
  - **Output**: Links change color and decoration based on state.
  - **Common Error**: Missing semicolons: Styles ignored.
    - **Fix**: Include semicolons.

- `<body>`:
  - **Purpose**: Contains visible content (heading, image, link, comment).
  - **Metaphor**: The guidebook’s pages with photos and links.
  - **Output**: Displays content in the browser.

- `<!-- Main title -->`:
  - **Purpose**: Documents the title section.
  - **Output**: Invisible in the browser.
  - **Common Error**: Incorrect syntax: Content may display.
    - **Fix**: Use `<!-- -->`.

- `<h1>Space Exploration Home</h1>`:
  - **Purpose**: Displays the main heading.
  - **Output**: Shows "Space Exploration Home" in large, bold text.
  - **Visual Cue**: Large, bold text at the top.
  - **Common Error**: Missing `</h1>`: Layout issues.
    - **Fix**: Close tags.

- `<!-- Embedded image -->`:
  - **Purpose**: Documents the image section.
  - **Output**: Invisible in the browser.

- `<p><img src="rocket.jpg" alt="Rocket launching into space" style="width:200px;height:200px;"></p>`:
  - **Purpose**: Embeds a rocket image sized to 200x200 pixels.
  - **Attributes**:
    - `src="rocket.jpg"`: Points to the image in `images/`.
    - `alt="Rocket launching into space"`: Describes the image.
    - `style="width:200px;height:200px;"`: Sets size.
  - **Output**: Shows a 200x200 pixel rocket image; if missing, displays `alt` text.
  - **Visual Cue**: Image appears; broken icon if missing.
  - **Common Error**: Wrong `src`: Broken image.
    - **Fix**: Ensure `rocket.jpg` exists.

- `<!-- Link to Details page -->`:
  - **Purpose**: Documents the navigation link section.
  - **Output**: Invisible in the browser.

- `<p><a href="details.html" title="More about space exploration">More Details</a></p>`:
  - **Purpose**: Links to the Details page.
  - **Attributes**:
    - `href="details.html"`: Points to the Details page.
    - `title="More about space exploration"`: Shows a tooltip.
  - **Output**: Shows "More Details" as clickable text; navigates to `details.html`.
  - **Visual Cue**: White/light gray text, yellow and underlined on hover.
  - **Common Error**: Missing `details.html`: Broken link.
    - **Fix**: Ensure `details.html` exists.

- `<!-- <p>Draft: Add background image later.</p> -->`:
  - **Purpose**: Hides a draft note.
  - **Output**: Invisible in the browser.
  - **Common Error**: Incorrect syntax: Content displays.
    - **Fix**: Use `<!-- -->`.

**Line-by-Line Breakdown (for `details.html`)**:

- Structure mirrors `index.html` with `<!DOCTYPE html>`, `<html lang="en">`, `<head>`, and `<title>Space Exploration Details</title>`, serving similar purposes.
- `<link rel="icon" type="image/x-icon" href="images/favicon.ico">`: Same favicon as `index.html` for consistency.
- `<body>`: Contains visible content.
- `<!-- Main title -->`: Documents the title section.
- `<h1>Space Exploration Details</h1>`: Displays the page heading.
- `<!-- Image link back to homepage -->`: Documents the image link section.
- `<p><a href="index.html" title="Return to homepage"><img src="home_icon.jpg" alt="Home icon" style="width:50px;height:50px;"></a></p>`:
  - **Purpose**: Creates a clickable home icon linking back to the homepage.
  - **Attributes**:
    - `href="index.html"`: Points to the homepage.
    - `title="Return to homepage"`: Shows a tooltip.
    - `src="home_icon.jpg"`: Points to the icon image.
    - `alt="Home icon"`: Describes the image.
    - `style="width:50px;height:50px;"`: Sets size.
  - **Output**: Shows a 50x50 pixel home icon; clicking navigates to `index.html`.
  - **Visual Cue**: Hand cursor and tooltip on hover.
  - **Common Error**: Wrong `src` or `href`: Broken image or link.
    - **Fix**: Ensure files exist.
- `<!-- <p>Draft: Add more content later.</p> -->`: Hides a draft note.

**Expected Output in Browser**:

- For `index.html`:
  - Browser tab: "Space Exploration Home" with favicon.
  - Page content:
    ```
    Space Exploration Home [large, bold text]
    [200x200 pixel rocket image]
    More Details [white/light gray text, yellow and underlined on hover, navigates to details.html]
    ```

- For `details.html`:
  - Browser tab: "Space Exploration Details" with favicon.
  - Page content:
    ```
    Space Exploration Details [large, bold text]
    [50x50 pixel home icon, clickable to index.html]
    ```

**Side Effects**: None (static HTML/CSS; links navigate between pages).

**Visual Cues**:
- Favicon appears in both tabs (e.g., 16x16 pixel icon).
- Titles display in tabs.
- Homepage shows rocket image and styled link; Details page shows clickable home icon.
- Comments are invisible in the browser.

**How to Test**:
1. Save both files in a folder (e.g., `space-website`) with an `images` subfolder containing `favicon.ico`, `rocket.jpg`, and `home_icon.jpg`.
2. Open `index.html` in a browser.
3. Verify:
   - Tabs show correct titles and favicon.
   - Homepage displays rocket image and "More Details" link (navigates to `details.html`).
   - Details page shows home icon (navigates to `index.html`).
   - Comments are invisible but visible in "View Page Source."
4. Use a screen reader to confirm `alt` text and titles are accessible.

**Common Errors and Troubleshooting**:
- **Error**: Favicon doesn’t display.
  - **Cause**: Incorrect `href` or missing favicon.
    - **Fix**: Ensure `favicon.ico` is in `images/`.
- **Error**: Images don’t display.
  - **Cause**: Wrong `src` or missing image.
    - **Fix**: Ensure `rocket.jpg` and `home_icon.jpg` exist.
- **Error**: Links don’t work.
  - **Cause**: Missing or incorrect `href`.
    - **Fix**: Ensure `index.html` and `details.html` exist.
- **Error**: Tab shows file path.
  - **Cause**: Missing `<title>`.
    - **Fix**: Include `<title>` in `<head>`.
- **Error**: Page shows code.
  - **Cause**: Saved as `.txt`.
    - **Fix**: Save as `.html`.

**Validation Checks**:
- Confirm files start with `<!DOCTYPE html>` and include `<html lang="en">`.
- Verify favicons, titles, images, and links work.
- Ensure `alt`, `title`, and `style` attributes are used.
- Check comments are hidden.
- Test navigation between pages.

**Metaphor for the Whole Process**: Building this website is like creating a two-page space exploration guidebook. The homepage is the cover with a logo (favicon), title, and rocket photo, while the Details page is an inner chapter with a return button (image link), organized with hidden notes (comments).

---

## Completion Checklist

- **Learning Goals**:
  - Use `<link>` with `rel`, `type`, and `href` for a favicon.
  - Use `<title>` for a descriptive page title.
  - Combine with images and links from prior lessons.
- **Runnable Example**: The code above (`index.html`, `details.html`) is a complete, runnable solution.
- **Checklist for Completion**:
  - [ ] Files start with `<!DOCTYPE html>` and include `<html lang="en">`.
  - [ ] Include `<link>` for favicon and `<title>` for page title.
  - [ ] Include images and links as specified.
  - [ ] Include at least one comment per file.
  - [ ] Favicon, title, images, and links display correctly.
  - [ ] Saved as `.html` and renders correctly in a browser.
- **Common Pitfalls**:
  - Incorrect `href` for favicon or images.
  - Missing or vague `<title>`.
  - Incorrect `type` for favicon format.
  - Missing images or linked files.
  - Incorrect comment syntax.
- **One-Line Summary**: The two-page space exploration website uses `<link>` for favicons, `<title>` for descriptive titles, `<img>` for images, and `<a>` for navigation, with comments, viewable in a browser after saving as HTML files.