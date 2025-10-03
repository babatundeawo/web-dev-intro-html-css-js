# Solution and Explanation for HTML Weekly Project: Two-Page Space Exploration Website

This markdown provides the code solution for the weekly project from the HTML Images tutorial, which involves creating a two-page website about space exploration. The homepage includes an embedded image, an image link to an external site, a background image styled with CSS, and a link to the Details page. The Details page includes an image map with clickable areas, a responsive `<picture>` element, and a link back to the homepage. The solution uses `<img>`, `<a>`, `<map>`, `<area>`, and `<picture>` tags, with comments for documentation and accessibility features like `alt` and `title` attributes. The explanation follows the instructional framework, ensuring beginner-friendly guidance with plain language, metaphors, and detailed breakdowns of the code, including expected outputs, visual cues, common errors, and validation checks.

---

## Section 1 — Topical Explanations

The weekly project requires building a two-page website about space exploration: a homepage (`index.html`) with an embedded image, an image link to an external site (e.g., NASA), a CSS background image, and a link to a Details page (`details.html`), which includes an image map with two clickable areas (e.g., `rect` and `circle`) and a responsive `<picture>` element with two `<source>` tags and a fallback `<img>`. Both pages use comments for clarity and accessibility features. The solution uses a space exploration theme to engage learners. Below are the solutions for all files, followed by a step-by-step explanation.

### Solution Code

#### Homepage (`index.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Space Exploration</title>
    <style>
        body {
            background-image: url('stars.jpg');
            background-repeat: no-repeat;
            background-size: cover;
            background-attachment: fixed;
        }
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
    <h1>Space Exploration</h1>
    <!-- Embedded image -->
    <p><img src="rocket.jpg" alt="Rocket launching into space" style="width:200px;height:200px;"></p>
    <!-- Image link -->
    <p><a href="https://www.nasa.gov" target="_blank" title="Visit NASA's website">
        <img src="nasa_logo.jpg" alt="NASA logo" style="width:100px;height:100px;">
    </a></p>
    <!-- Link to Details page -->
    <p><a href="details.html" title="More about space exploration">More Details</a></p>
    <!-- <p>Draft: Add more images later.</p> --> <!-- Hidden draft content -->
</body>
</html>
```

#### Details Page (`details.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Space Exploration Details</title>
</head>
<body>
    <!-- Page title -->
    <h1>Space Exploration Details</h1>
    <!-- Image map -->
    <p><img src="space_scene.jpg" alt="Space scene with planet and star" usemap="#spacemap" style="width:400px;height:300px;"></p>
    <map name="spacemap">
        <area shape="rect" coords="50,50,200,200" alt="Planet" href="planet.html" title="Learn about planets">
        <area shape="circle" coords="300,100,50" alt="Star" href="star.html" title="Learn about stars">
    </map>
    <!-- Responsive image -->
    <p>
        <picture>
            <source media="(min-width:650px)" srcset="galaxy_large.jpg">
            <source media="(min-width:465px)" srcset="galaxy_medium.jpg">
            <img src="galaxy_small.jpg" alt="Galaxy view" style="width:200px;height:200px;">
        </picture>
    </p>
    <!-- Link back to homepage -->
    <p><a href="index.html" title="Return to homepage">Back to Homepage</a></p>
    <!-- <p>Draft: Add more interactive elements.</p> --> <!-- Hidden draft content -->
</body>
</html>
```

#### Dummy Page for Image Map (`planet.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Planets</title>
</head>
<body>
    <h1>About Planets</h1>
    <p>Planets orbit stars and vary in size and composition.</p>
    <p><a href="details.html">Back to Details</a></p>
</body>
</html>
```

#### Dummy Page for Image Map (`star.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Stars</title>
</head>
<body>
    <h1>About Stars</h1>
    <p>Stars are massive balls of gas that produce light.</p>
    <p><a href="details.html">Back to Details</a></p>
</body>
</html>
```

### Explanation of the Solution

**Overview**: The project is like creating a two-page space exploration guidebook. The homepage is the cover, showcasing a rocket image, a clickable NASA logo, a starry background, and a link to the Details page. The Details page dives deeper with an image map (clickable planet and star) and a responsive galaxy image that changes based on screen size. Comments act as hidden notes for organization, and CSS styles enhance the visual appeal.

**Step-by-Step Instructions to Set Up**:
1. Open a text editor (e.g., Notepad or TextEdit).
2. Create a new folder (e.g., `space-website`).
3. Copy the code for `index.html`, `details.html`, `planet.html`, and `star.html` into separate files, saving them with UTF-8 encoding in the `space-website` folder.
4. Place sample images (`stars.jpg`, `rocket.jpg`, `nasa_logo.jpg`, `space_scene.jpg`, `galaxy_large.jpg`, `galaxy_medium.jpg`, `galaxy_small.jpg`) in the same folder (use any JPEG images renamed for testing).
5. Double-click `index.html` to open in a browser and test images, links, background, image map, and responsiveness.

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
  - **Purpose**: Contains metadata, title, and internal CSS.
  - **Metaphor**: The guidebook’s title page with styling rules.
  - **Output**: Affects browser behavior (tab title, background, link styles).

- `<title>Space Exploration</title>`:
  - **Purpose**: Sets the browser tab title.
  - **Output**: Tab displays "Space Exploration."
  - **Common Error**: Missing `<title>` shows a blank tab.
    - **Fix**: Include a descriptive title.

- `<style>`:
  - **Purpose**: Defines CSS for background and link styling.
  - **Metaphor**: A decorating guide for the page and links.
  - **Output**: Applies background image and link styles.

- `body {background-image: url('stars.jpg'); background-repeat: no-repeat; background-size: cover; background-attachment: fixed;}`:
  - **Purpose**: Sets a starry background that covers the page without repeating.
  - **Output**: Background image fills the page, stays fixed on scroll.
  - **Common Error**: Wrong `url`: No background.
    - **Fix**: Ensure `stars.jpg` exists in the folder.

- `a:link {color: white; text-decoration: none;}`:
  - **Purpose**: Styles unvisited links as white with no underline.
  - **Output**: Links are white without underlines.
  - **Common Error**: Misspelling `a:link`: Styles ignored.
    - **Fix**: Use correct pseudo-class.

- `a:visited`, `a:hover`, `a:active`:
  - **Purpose**: Styles visited (light gray), hovered (yellow, underlined), and active (orange, underlined) links.
  - **Output**: Links change color and decoration based on state.
  - **Common Error**: Missing semicolons: Styles ignored.
    - **Fix**: Include semicolons.

- `<body>`:
  - **Purpose**: Contains visible content (heading, images, links, comment).
  - **Metaphor**: The guidebook’s pages with photos and links.
  - **Output**: Displays content in the browser.

- `<!-- Main title -->`:
  - **Purpose**: Documents the title section.
  - **Output**: Invisible in the browser.
  - **Common Error**: Incorrect syntax: Content may display.
    - **Fix**: Use `<!-- -->`.

- `<h1>Space Exploration</h1>`:
  - **Purpose**: Displays the main title.
  - **Output**: Shows "Space Exploration" in large, bold text.
  - **Visual Cue**: Large, bold text at the top.
  - **Common Error**: Missing `</h1>`: Layout issues.
    - **Fix**: Close tags.

- `<!-- Embedded image -->`:
  - **Purpose**: Documents the image section.
  - **Output**: Invisible in the browser.

- `<p><img src="rocket.jpg" alt="Rocket launching into space" style="width:200px;height:200px;"></p>`:
  - **Purpose**: Embeds a rocket image sized to 200x200 pixels.
  - **Attributes**:
    - `src="rocket.jpg"`: Points to the image.
    - `alt="Rocket launching into space"`: Describes the image.
    - `style="width:200px;height:200px;"`: Sets size.
  - **Output**: Shows a 200x200 pixel rocket image; if missing, displays `alt` text.
  - **Visual Cue**: Image appears; broken icon if missing.
  - **Common Error**: Wrong `src`: Broken image.
    - **Fix**: Ensure `rocket.jpg` exists.

- `<!-- Image link -->`:
  - **Purpose**: Documents the image link section.
  - **Output**: Invisible in the browser.

- `<p><a href="https://www.nasa.gov" target="_blank" title="Visit NASA's website"><img src="nasa_logo.jpg" alt="NASA logo" style="width:100px;height:100px;"></a></p>`:
  - **Purpose**: Creates a clickable NASA logo linking to NASA’s website.
  - **Attributes**:
    - `href="https://www.nasa.gov"`: External destination.
    - `target="_blank"`: Opens in a new tab.
    - `title="Visit NASA's website"`: Shows a tooltip.
    - `src="nasa_logo.jpg"`: Points to the logo.
    - `alt="NASA logo"`: Describes the image.
    - `style="width:100px;height:100px;"`: Sets size.
  - **Output**: Shows a 100x100 pixel NASA logo; clicking opens NASA in a new tab.
  - **Visual Cue**: Hand cursor, tooltip on hover.
  - **Common Error**: Invalid `href`: Broken link.
    - **Fix**: Use correct URL.

- `<!-- Link to Details page -->`:
  - **Purpose**: Documents the navigation link section.
  - **Output**: Invisible in the browser.

- `<p><a href="details.html" title="More about space exploration">More Details</a></p>`:
  - **Purpose**: Links to the Details page.
  - **Output**: Shows "More Details" as clickable text; navigates to `details.html`.
  - **Visual Cue**: White/light gray text, yellow and underlined on hover.
  - **Common Error**: Missing `details.html`: Broken link.
    - **Fix**: Ensure `details.html` exists.

- `<!-- <p>Draft: Add more images later.</p> -->`:
  - **Purpose**: Hides a draft note.
  - **Output**: Invisible in the browser.
  - **Common Error**: Incorrect syntax: Content displays.
    - **Fix**: Use `<!-- -->`.

**Line-by-Line Breakdown (for `details.html`)**:

- Structure mirrors `index.html` with `<!DOCTYPE html>`, `<html lang="en">`, `<head>`, and `<title>Space Exploration Details</title>`, serving similar purposes.
- `<body>`: Contains visible content.
- `<!-- Page title -->`: Documents the title section.
- `<h1>Space Exploration Details</h1>`: Displays the page title.
- `<!-- Image map -->`: Documents the image map section.
- `<p><img src="space_scene.jpg" alt="Space scene with planet and star" usemap="#spacemap" style="width:400px;height:300px;"></p>`:
  - **Purpose**: Embeds an image with a map of clickable areas.
  - **Attributes**:
    - `src="space_scene.jpg"`: Points to the image.
    - `alt="Space scene with planet and star"`: Describes the image.
    - `usemap="#spacemap"`: Links to the map.
    - `style="width:400px;height:300px;"`: Sets size.
  - **Output**: Shows a 400x300 pixel image; clickable areas navigate to pages.
  - **Visual Cue**: Hand cursor over clickable areas.
  - **Common Error**: Wrong `usemap`: Map doesn’t work.
    - **Fix**: Match `usemap="#spacemap"` with `<map name="spacemap">`.

- `<map name="spacemap">`:
  - **Purpose**: Defines the image map.
  - **Output**: Invisible but enables clickable areas.
  - **Common Error**: Mismatched `name`: Map fails.
    - **Fix**: Match `name` with `usemap`.

- `<area shape="rect" coords="50,50,200,200" alt="Planet" href="planet.html" title="Learn about planets">`:
  - **Purpose**: Defines a rectangular clickable area for a planet.
  - **Output**: Clicking the rectangle (50,50 to 200,200) navigates to `planet.html`.
  - **Visual Cue**: Hand cursor over the area.
  - **Common Error**: Incorrect `coords`: Wrong clickable area.
    - **Fix**: Verify coordinates.

- `<area shape="circle" coords="300,100,50" alt="Star" href="star.html" title="Learn about stars">`:
  - **Purpose**: Defines a circular clickable area for a star.
  - **Output**: Clicking the circle (center 300,100, radius 50) navigates to `star.html`.
  - **Visual Cue**: Hand cursor over the area.
  - **Common Error**: Incorrect `coords`: Wrong clickable area.
    - **Fix**: Verify coordinates.

- `<!-- Responsive image -->`:
  - **Purpose**: Documents the responsive image section.
  - **Output**: Invisible in the browser.

- `<picture><source media="(min-width:650px)" srcset="galaxy_large.jpg"><source media="(min-width:465px)" srcset="galaxy_medium.jpg"><img src="galaxy_small.jpg" alt="Galaxy view" style="width:200px;height:200px;"></picture>`:
  - **Purpose**: Displays different images based on screen size.
  - **Output**: Shows `galaxy_large.jpg` (≥650px), `galaxy_medium.jpg` (≥465px), or `galaxy_small.jpg` (fallback), sized to 200x200 pixels.
  - **Visual Cue**: Image changes with browser width.
  - **Common Error**: Missing `<img>` fallback: No image in unsupported browsers.
    - **Fix**: Include `<img>` as the last child.

- `<!-- Link back to homepage -->`:
  - **Purpose**: Documents the back link section.
  - **Output**: Invisible in the browser.

- `<p><a href="index.html" title="Return to homepage">Back to Homepage</a></p>`:
  - **Purpose**: Links back to the homepage.
  - **Output**: Shows "Back to Homepage" as clickable text; navigates to `index.html`.
  - **Visual Cue**: Browser-default link style (e.g., blue, underlined).
  - **Common Error**: Missing `index.html`: Broken link.
    - **Fix**: Ensure `index.html` exists.

- `<!-- <p>Draft: Add more interactive elements.</p> -->`:
  - **Purpose**: Hides a draft note.
  - **Output**: Invisible in the browser.

**Line-by-Line Breakdown (for `planet.html` and `star.html`)**:
- Simple pages with `<h1>`, content, and a link back to `details.html`, ensuring image map links work for testing.

**Expected Output in Browser**:

- For `index.html`:
  - Browser tab: "Space Exploration"
  - Page content (on starry background):
    ```
    Space Exploration [large, bold text]
    [200x200 pixel rocket image]
    [100x100 pixel NASA logo, clickable to NASA]
    More Details [white/light gray text, yellow and underlined on hover, navigates to details.html]
    ```

- For `details.html`:
  - Browser tab: "Space Exploration Details"
  - Page content:
    ```
    Space Exploration Details [large, bold text]
    [400x300 pixel space scene image, clickable areas for planet and star]
    [200x200 pixel galaxy image, changes with screen size]
    Back to Homepage [blue underlined text, navigates to index.html]
    ```

**Side Effects**: None (static HTML/CSS; image link and image map links open new tabs or navigate; responsive image changes with screen size).

**Visual Cues**:
- Homepage: Starry background, sized images, white/light gray links turning yellow on hover.
- Details: Clickable areas in the image map show a hand cursor, responsive image swaps based on screen size.
- Comments are invisible in the browser.

**How to Test**:
1. Save all files in the same folder (e.g., `space-website`) with sample images.
2. Open `index.html` in a browser.
3. Verify:
   - Browser tabs show correct titles.
   - Homepage displays rocket image, NASA logo (clickable), and starry background.
   - "More Details" link navigates to `details.html`.
   - Details page shows image map (click planet and star areas to navigate to `planet.html` and `star.html`).
   - Responsive image changes when resizing the browser.
   - Back link returns to `index.html`.
   - Comments are invisible but visible in "View Page Source."
4. Use a screen reader to confirm `alt` text accessibility.

**Common Errors and Troubleshooting**:
- **Error**: Images don’t display.
  - **Cause**: Incorrect `src` or missing images.
    - **Fix**: Ensure images exist in the folder.
- **Error**: Image map doesn’t work.
  - **Cause**: Mismatched `usemap` and `name` or incorrect `coords`.
    - **Fix**: Match `usemap="#spacemap"` with `<map name="spacemap">` and verify coordinates.
- **Error**: Responsive image doesn’t switch.
  - **Cause**: Missing `<img>` fallback or incorrect `media` queries.
    - **Fix**: Include `<img>` and check `min-width` values.
- **Error**: Background image doesn’t appear.
  - **Cause**: Wrong `url` or missing image.
    - **Fix**: Ensure `stars.jpg` exists.
- **Error**: Page shows code.
  - **Cause**: Saved as `.txt`.
    - **Fix**: Save as `.html`.

**Validation Checks**:
- Confirm files start with `<!DOCTYPE html>` and include `<html lang="en">`.
- Verify images, links, background, image map, and responsive image work.
- Ensure `alt`, `title`, and `usemap` attributes are used.
- Check comments are hidden.
- Test responsiveness by resizing the browser.

**Metaphor for the Whole Process**: Building this website is like creating a two-page space exploration guidebook. The homepage is the cover with a rocket photo, a clickable NASA logo, and starry wallpaper, while the Details page offers an interactive map and adaptive photos, all organized with hidden notes (comments).

---

## Completion Checklist

- **Learning Goals**:
  - Use `<img>` with `src`, `alt`, and `style` attributes.
  - Create image links with `<a>` and `<img>`.
  - Define image maps with `<map>` and `<area>`.
  - Set background images with CSS.
  - Use `<picture>` for responsive images.
- **Runnable Example**: The code above (`index.html`, `details.html`, `planet.html`, `star.html`) is a complete, runnable solution.
- **Checklist for Completion**:
  - [ ] Files start with `<!DOCTYPE html>` and include `<html lang="en">`.
  - [ ] Include embedded images, image links, background images, image maps, and responsive images.
  - [ ] Use `src`, `alt`, `style`, `href`, `usemap`, `shape`, `coords`, `srcset`, and `media` attributes.
  - [ ] Apply CSS for background and link styling.
  - [ ] Include at least one comment per file.
  - [ ] Images, links, and responsive features work.
  - [ ] Saved as `.html` and renders correctly in a browser.
- **Common Pitfalls**:
  - Incorrect `src` or image paths.
  - Missing `alt` attributes.
  - Mismatched `usemap` and `map name`.
  - Invalid CSS properties or missing units.
  - Missing `<img>` fallback in `<picture>`.
- **One-Line Summary**: The two-page space exploration website uses `<img>`, `<a>`, `<map>`, `<area>`, and `<picture>` for images, links, maps, and responsive images, styled with CSS and enhanced with comments, viewable in a browser after saving as HTML files.