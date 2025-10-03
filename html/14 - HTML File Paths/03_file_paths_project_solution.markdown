# Solution and Explanation for HTML File Paths Weekly Project: Two-Page Travel Guide Website

This markdown provides the code solution for the weekly project from the HTML File Paths tutorial, which involves creating a two-page website about a travel guide. The homepage (`index.html`) includes two `<img>` elements with relative paths (one in a subfolder `images/destination.jpg`, one in the parent folder `../map.jpg`), styled with a `class="photo"` for border and `id="featured"` for size. The Details page (`details.html`) includes an `<img>` with `id="placeImage"` and relative path `images/place.jpg`, a `<button>` to change its `src` to `images/place2.jpg` using JavaScript, a heading, and a link back to the homepage. Both pages include comments for documentation and `lang="en"` for accessibility. The explanation follows the instructional framework, ensuring beginner-friendly guidance with plain language, metaphors, and detailed breakdowns of the code, including expected outputs, visual cues, common errors, and validation checks.

---

## Section 1 — Topical Explanations

The weekly project requires building a two-page website about a travel guide. The homepage features two images linked with relative file paths—one from a subfolder (`images/destination.jpg`) and one from the parent folder (`../map.jpg`)—styled with a shared `class="photo"` for borders and a unique `id="featured"` for size, plus a heading and navigation to the Details page. The Details page has an image (`images/place.jpg`) that changes to another (`images/place2.jpg`) on button click using JavaScript, a heading, and a link back to the homepage. Both pages include comments for clarity. The theme is a travel guide to engage learners. Below are the solutions for both files, followed by a step-by-step explanation.

### Solution Code

#### Homepage (`index.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Travel Guide</title>
    <style>
        .photo {
            border: 2px solid black;
        }
        #featured {
            width: 300px;
        }
    </style>
</head>
<body>
    <!-- Main title -->
    <h1>Travel Guide</h1>
    <img src="images/destination.jpg" alt="Travel Destination" class="photo">
    <img src="../map.jpg" alt="Travel Map" class="photo" id="featured">
    <!-- Navigation to Details page -->
    <p><a href="details.html" title="Travel details">Travel Details</a></p>
    <!-- <p>Draft: Add more images later.</p> --> <!-- Hidden draft content -->
</body>
</html>
```

#### Details Page (`details.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Travel Details</title>
</head>
<body>
    <!-- Main title -->
    <h1>Travel Details</h1>
    <img id="placeImage" src="images/place.jpg" alt="Travel Place" width="200">
    <button onclick="changePlace()">Change Place</button>
    <p><a href="index.html" title="Back to travel guide">Back to Travel Guide</a></p>
    <!-- JavaScript to change image -->
    <script>
        function changePlace() {
            document.getElementById("placeImage").src = "images/place2.jpg";
        }
    </script>
    <!-- <p>Draft: Add more details later.</p> --> <!-- Hidden draft content -->
</body>
</html>
```

### Explanation of the Solution

**Overview**: The project is like creating a two-page travel brochure. The homepage is a showcase page with two images—one from a subfolder (`images/destination.jpg`) and one from the parent folder (`../map.jpg`)—styled with a shared `class="photo"` for borders and a unique `id="featured"` for a larger size, plus a heading and a link to the Details page. The Details page is a detail sheet with an image (`images/place.jpg`) that changes to another (`images/place2.jpg`) on button click using JavaScript to modify the `src` attribute, a heading, and a link back to the homepage. Both pages use comments for organization and navigation for connectivity, making the code beginner-friendly.

**Step-by-Step Instructions to Set Up**:
1. Create a parent folder (e.g., `travel-parent`).
2. Inside `travel-parent`, create a subfolder `travel-guide`.
3. Inside `travel-guide`, create a subfolder `images`.
4. Place the following images in `travel-guide/images`: `destination.jpg`, `place.jpg`, `place2.jpg`.
5. Place `map.jpg` in `travel-parent` (parent folder).
6. Open a text editor (e.g., Notepad or TextEdit).
7. Copy the code for `index.html` and save it as `index.html` in `travel-guide`.
8. Copy the code for `details.html` and save it as `details.html` in `travel-guide`.
9. Double-click `index.html` to open in a browser and test the images, styling, JavaScript, and navigation.

**Line-by-Line Breakdown (for `index.html`)**:

- `<!DOCTYPE html>`:
  - **Purpose**: Declares HTML5 for proper rendering.
  - **Metaphor**: Like a label on a travel brochure, signaling it’s an HTML5 page.
  - **Output**: No visible output, ensures correct rendering.
  - **Common Error**: Omitting causes "quirks mode."
    - **Fix**: Include at the top.

- `<html lang="en">`:
  - **Purpose**: Root element with `lang="en"` for accessibility.
  - **Metaphor**: The brochure’s cover, holding all content.
  - **Output**: No visible output, sets structure.
  - **Common Error**: Missing `lang` reduces accessibility.
    - **Fix**: Include `lang="en"`.

- `<head>`:
  - **Purpose**: Contains metadata, title, and CSS.
  - **Metaphor**: The brochure’s title page with styling rules.
  - **Output**: Affects tab title and image styles.

- `<title>Travel Guide</title>`:
  - **Purpose**: Sets tab title for SEO and clarity.
  - **Output**: Tab shows "Travel Guide."
  - **Visual Cue**: Title in tab, toolbar, favorites.
  - **Common Error**: Missing `<title>` shows file path.
    - **Fix**: Include descriptive title.

- `<style>`:
  - **Purpose**: Defines CSS for styling images with `class="photo"` and `id="featured"`.
  - **Metaphor**: A decorating guide for the images.
  - **Output**: Applies border to `.photo` and width to `#featured`.

- `.photo { border: 2px solid black; }`:
  - **Purpose**: Adds a black border to images with `class="photo"`.
  - **Output**: Both images have 2px black borders.
  - **Visual Cue**: Black outline around images.
  - **Common Error**: Class mismatch (e.g., `Photo`): No border.
    - **Fix**: Use `class="photo"` and `.photo`.

- `#featured { width: 300px; }`:
  - **Purpose**: Sets width for the image with `id="featured"`.
  - **Output**: Map image is 300px wide.
  - **Visual Cue**: Larger map image.
  - **Common Error**: Duplicate `id`: Invalid HTML.
    - **Fix**: Use `id` once.

- `<body>`:
  - **Purpose**: Contains visible content.
  - **Metaphor**: The brochure’s pages.
  - **Output**: Displays content in the browser.

- `<!-- Main title -->`:
  - **Purpose**: Documents the heading.
  - **Output**: Invisible.
  - **Common Error**: Incorrect syntax: Content displays.
    - **Fix**: Use `<!-- -->`.

- `<h1>Travel Guide</h1>`:
  - **Purpose**: Displays main heading.
  - **Output**: Large, bold "Travel Guide."
  - **Visual Cue**: Bold text at top.
  - **Common Error**: Missing `</h1>`: Layout issues.
    - **Fix**: Close tag.

- `<img src="images/destination.jpg" alt="Travel Destination" class="photo">`:
  - **Purpose**: Displays an image from the subfolder with a black border.
  - **Output**: Shows `destination.jpg` with border.
  - **Visual Cue**: Image with black outline.
  - **Common Error**: Missing `images/destination.jpg`: Broken image.
    - **Fix**: Ensure file exists in `images` subfolder.

- `<img src="../map.jpg" alt="Travel Map" class="photo" id="featured">`:
  - **Purpose**: Displays an image from the parent folder with border and larger width.
  - **Output**: Shows `map.jpg` (300px wide) with border.
  - **Visual Cue**: Larger image with black outline.
  - **Common Error**: Missing `../map.jpg`: Broken image.
    - **Fix**: Ensure `map.jpg` is in the parent folder.
  - **Common Error**: Missing `id`: Width not applied.
    - **Fix**: Include `id="featured"`.

- `<!-- Navigation to Details page -->`:
  - **Purpose**: Documents the link.
  - **Output**: Invisible.

- `<p><a href="details.html" title="Travel details">Travel Details</a></p>`:
  - **Purpose**: Links to Details page.
  - **Output**: Clickable "Travel Details" text.
  - **Visual Cue**: Hand cursor, tooltip.
  - **Common Error**: Missing `details.html`: Broken link.
    - **Fix**: Ensure file exists.

- `<!-- <p>Draft: Add more images later.</p> -->`:
  - **Purpose**: Hides draft note.
  - **Output**: Invisible.

**Line-by-Line Breakdown (for `details.html`)**:

- Structure mirrors `index.html` with `<!DOCTYPE html>`, `<html lang="en">`, `<head>`, and `<title>Travel Details</title>`, serving similar purposes.
- `<h1>Travel Details</h1>`: Displays heading.
- `<img id="placeImage" src="images/place.jpg" alt="Travel Place" width="200">`:
  - **Purpose**: Displays an image from the subfolder with `id="placeImage"`.
  - **Output**: Shows `place.jpg` (200px wide).
  - **Visual Cue**: Image appears.
  - **Common Error**: Missing `images/place.jpg`: Broken image.
    - **Fix**: Ensure file exists.
- `<button onclick="changePlace()">Change Place</button>`:
  - **Purpose**: Triggers `changePlace()` function.
  - **Output**: Clickable button.
  - **Visual Cue**: Hand cursor.
- `<p><a href="index.html" title="Back to travel guide">Back to Travel Guide</a></p>`:
  - **Purpose**: Links back to homepage.
  - **Output**: Clickable text.
- `<!-- JavaScript to change image -->` and `<script>`:
  - **Purpose**: Documents and contains JavaScript.
  - **Output**: Enables image swap.
- `function changePlace() { document.getElementById("placeImage").src = "images/place2.jpg"; }`:
  - **Purpose**: Changes image `src` to `images/place2.jpg`.
  - **Output**: Image changes to `place2.jpg` on click.
  - **Visual Cue**: New image appears.
  - **Common Error**: Missing `images/place2.jpg`: Broken image.
    - **Fix**: Ensure file exists.
- `<!-- <p>Draft: Add more details later.</p> -->`: Hides draft note.

**Expected Output in Browser**:

- For `index.html`:
  - Browser tab: "Travel Guide."
  - Page content:
    ```
    Travel Guide [large, bold text]
    [destination.jpg image with black border]
    [map.jpg image, 300px wide, with black border]
    Travel Details [clickable link]
    ```

- For `details.html`:
  - Browser tab: "Travel Details."
  - Page content:
    ```
    Travel Details [large, bold text]
    [place.jpg image, 200px wide]
    [Change Place button]
    Back to Travel Guide [clickable link]
    ```
  - Clicking "Change Place": Image changes to `place2.jpg`.

**Side Effects**: Button click changes image `src` on Details page; links navigate between pages.

**Visual Cues**:
- Homepage: Images with black borders; map image larger.
- Details page: Image changes on button click.
- Links show hand cursor and tooltips.
- Comments are invisible.

**How to Test**:
1. Create `travel-parent` folder.
2. Create `travel-guide` subfolder inside `travel-parent`.
3. Create `images` subfolder inside `travel-guide`.
4. Place `destination.jpg`, `place.jpg`, `place2.jpg` in `travel-guide/images`.
5. Place `map.jpg` in `travel-parent`.
6. Save `index.html` and `details.html` in `travel-guide`.
7. Open `index.html` in a browser.
8. Verify:
   - Images display with correct paths and styling.
   - Button on Details page changes image.
   - Navigation links work.
   - Comments are invisible.
9. Use a screen reader to confirm `alt` text.

**Common Errors and Troubleshooting**:
- **Error**: Images don't display.
  - **Cause**: Incorrect paths or missing files.
    - **Fix**: Ensure `images/destination.jpg`, `../map.jpg`, etc., exist.
- **Error**: Button doesn't change image.
  - **Cause**: Missing `id="placeImage"` or incorrect `src`.
    - **Fix**: Include `id` and ensure `place2.jpg` exists.
- **Error**: Links don't work.
  - **Cause**: Missing files or wrong paths.
    - **Fix**: Ensure both files exist in the same folder.
- **Error**: Page shows code.
  - **Cause**: Saved as `.txt`.
    - **Fix**: Save as `.html`.
- **Error**: Comment content visible.
  - **Cause**: Incorrect syntax.
    - **Fix**: Use `<!-- -->`.

**Validation Checks**:
- Confirm files start with `<!DOCTYPE html>` and include `<html lang="en">`.
- Verify relative paths, styling, JavaScript, and navigation.
- Check comments are hidden.
- Test with a screen reader.

**Metaphor for the Whole Process**: Building this website is like creating a travel brochure with photos from different drawers (subfolders and parent folders). The homepage showcases destination images, and the Details page lets you swap photos with a button, linked for easy navigation.

---

## Completion Checklist

- **Learning Goals**:
  - Use relative file paths (subfolder, parent folder).
  - Apply `class` and `id` styling to images.
  - Use JavaScript to change `src`.
  - Include navigation and comments.
- **Runnable Example**: The code above (`index.html`, `details.html`) is a complete, runnable solution (requires images in correct folders).
- **Checklist for Completion**:
  - [ ] Files start with `<!DOCTYPE html>` and include `<html lang="en">`.
  - [ ] Use relative paths (`images/destination.jpg`, `../map.jpg`, `images/place.jpg`).
  - [ ] Include `<img>` with `class="photo"` and `id="featured"`, CSS, JavaScript.
  - [ ] Include navigation and comments.
  - [ ] Images display, styling works, JavaScript changes image.
  - [ ] Saved as `.html` with images in correct folders.
- **Common Pitfalls**:
  - Incorrect file paths causing broken images.
  - Missing files or folders.
  - Case mismatch in filenames.
  - JavaScript errors from incorrect `id`.
  - Missing navigation files.
- **One-Line Summary**: The two-page travel guide website uses relative file paths to display and swap images with CSS styling and JavaScript, viewable in a browser after saving as HTML files with the correct folder structure.