# HTML Canvas and SVG Graphics: Beginner-Friendly Teaching Package

## Section 1 — Topical Explanations

### Overview of HTML Canvas and SVG
The HTML `<canvas>` and `<svg>` elements are used to create graphics on web pages. `<canvas>` is a pixel-based drawing surface controlled by JavaScript, like a digital sketchpad where you draw using code. `<svg>` (Scalable Vector Graphics) defines graphics in XML, creating shapes that scale without losing quality, like a set of blueprints for shapes. Both are supported by all major browsers and serve different purposes based on their strengths.

This section explains the `<canvas>` and `<svg>` elements, their methods, and examples from the lesson, with line-by-line breakdowns, expected outputs, common errors, and validation checks. We’ll start with simple examples and build them up for clarity.

### HTML Canvas: The Basics
The `<canvas>` element is a blank rectangular area where JavaScript draws graphics. It requires an `id` for scripting and `width`/`height` attributes to define its size. Think of it as a blank piece of paper where you use JavaScript as your pencil.

**Minimal Example (Building from Scratch):**
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Basic Canvas</title>
</head>
<body>
  <canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;"></canvas>
  <script>
    // Get the canvas element
    var c = document.getElementById("myCanvas");
    // Get the 2D drawing context
    var ctx = c.getContext("2d");
    // Draw a red square
    ctx.fillStyle = "red";
    ctx.fillRect(0, 0, 50, 50);
  </script>
</body>
</html>
```

**Line-by-Line Explanation:**
- `<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;">`:
  - `id="myCanvas"`: Identifies the canvas for JavaScript.
  - `width="200" height="100"`: Sets the canvas size to 200x100 pixels.
  - `style="border:1px solid #000000;"`: Adds a visible border for clarity.
  - **Purpose**: Creates a blank drawing area.
  - **Inputs**: None (static element).
  - **Outputs**: A blank rectangle with a black border.
  - **Side Effects**: None until JavaScript is added.
- `<script>`: Contains JavaScript to draw on the canvas.
- `var c = document.getElementById("myCanvas");`:
  - Gets the canvas element by its ID.
- `var ctx = c.getContext("2d");`:
  - Creates a 2D drawing context (`ctx`), the toolset for drawing shapes, lines, etc.
- `ctx.fillStyle = "red";`:
  - Sets the fill color to red for subsequent shapes.
- `ctx.fillRect(0, 0, 50, 50);`:
  - Draws a filled rectangle at coordinates (0,0) with width 50px and height 50px.
  - **Purpose**: Fills a square area with the specified color.
  - **Inputs**: Coordinates (x, y), width, height.
  - **Outputs**: A red square in the top-left corner.
  - **Side Effects**: Alters the canvas pixel data.

**Expected Output:**
A 200x100 pixel canvas with a black border containing a 50x50 red square in the top-left corner.

**Common Errors and Troubleshooting:**
- **Error**: Forgetting the `id` attribute, causing `document.getElementById` to fail.
  - **Fix**: Always include a unique `id` for the canvas.
- **Error**: Not specifying `width`/`height`, leading to default or distorted sizes.
  - **Fix**: Set explicit `width` and `height` attributes (e.g., `width="200"`).
- **Error**: JavaScript runs before the canvas is loaded.
  - **Fix**: Place the `<script>` after the `<canvas>` or use `window.onload`.

**Validation Check:**
- Save the code as `canvas.html` and open in a browser. Confirm a red square appears in a bordered canvas.

### Canvas: Drawing a Line
**Example Code:**
```html
<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;"></canvas>
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.moveTo(0, 0);
ctx.lineTo(200, 100);
ctx.stroke();
</script>
```

**Line-by-Line Explanation:**
- `ctx.moveTo(0, 0);`:
  - Moves the drawing cursor to the starting point (0,0) without drawing.
- `ctx.lineTo(200, 100);`:
  - Defines a line path from the current point (0,0) to (200,100).
- `ctx.stroke();`:
  - Draws the line with the default stroke color (black) and width (1px).
- **Purpose**: Draws a diagonal line across the canvas.
- **Inputs**: Start and end coordinates.
- **Outputs**: A black line from the top-left to bottom-right.
- **Side Effects**: Modifies canvas pixels along the path.

**Expected Output:**
A black diagonal line from (0,0) to (200,100) inside a 200x100 bordered canvas.

**Common Errors:**
- **Error**: Forgetting `ctx.stroke()`, leaving the line invisible.
  - **Fix**: Always call `stroke()` to render paths.
- **Error**: Coordinates outside the canvas (e.g., `lineTo(300, 200)`).
  - **Fix**: Ensure coordinates are within `width`/`height`.

**Validation Check:**
- Confirm the line spans from the top-left to bottom-right corners.

### Canvas: Drawing a Circle
**Example Code:**
```html
<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;"></canvas>
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.beginPath();
ctx.arc(95, 50, 40, 0, 2 * Math.PI);
ctx.stroke();
</script>
```

**Line-by-Line Explanation:**
- `ctx.beginPath();`:
  - Starts a new path, clearing previous path data.
- `ctx.arc(95, 50, 40, 0, 2 * Math.PI);`:
  - Draws a circular arc centered at (95,50) with radius 40px, from 0 to 2π radians (full circle).
- `ctx.stroke();`:
  - Outlines the circle with default stroke settings.
- **Purpose**: Draws a circular outline.
- **Inputs**: Center (x, y), radius, start/end angles.
- **Outputs**: A black circle outline.
- **Side Effects**: Modifies canvas pixels.

**Expected Output:**
A black circle centered at (95,50) with a 40px radius.

**Common Errors:**
- **Error**: Incorrect angle (e.g., `2` instead of `2 * Math.PI`), drawing a partial arc.
  - **Fix**: Use `2 * Math.PI` for a full circle.
- **Error**: Circle exceeds canvas bounds.
  - **Fix**: Ensure center and radius fit within canvas dimensions.

**Validation Check:**
- Verify the circle is complete and centered in the canvas.

### Canvas: Drawing Text
**Example Code:**
```html
<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;"></canvas>
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.font = "30px Arial";
ctx.fillText("Hello World", 10, 50);
</script>
```

**Line-by-Line Explanation:**
- `ctx.font = "30px Arial";`:
  - Sets the font size and family for text.
- `ctx.fillText("Hello World", 10, 50);`:
  - Draws filled text “Hello World” at (10,50).
- **Purpose**: Renders text on the canvas.
- **Inputs**: Text string, x, y coordinates.
- **Outputs**: Black text in 30px Arial.
- **Side Effects**: Modifies canvas pixels.

**Expected Output:**
The text “Hello World” in black at (10,50).

**Common Errors:**
- **Error**: Font not available, causing fallback.
  - **Fix**: Use common fonts like Arial or specify fallbacks (e.g., `"30px Arial, sans-serif"`).
- **Error**: Text cut off due to canvas size.
  - **Fix**: Ensure canvas is large enough for text.

**Validation Check:**
- Confirm the text is visible and correctly positioned.

### Canvas: Stroke Text
**Example Code:**
```html
<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;"></canvas>
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.font = "30px Arial";
ctx.strokeText("Hello World", 10, 50);
</script>
```

**Line-by-Line Explanation:**
- `ctx.strokeText("Hello World", 10, 50);`:
  - Draws an outline of the text instead of filling it.
- **Purpose**: Creates outlined text.
- **Inputs**: Text string, x, y coordinates.
- **Outputs**: Black outlined text.
- **Side Effects**: Modifies canvas pixels.

**Expected Output:**
The text “Hello World” outlined in black at (10,50).

**Common Errors:**
- **Error**: Thin or invisible outline due to default stroke width.
  - **Fix**: Set `ctx.lineWidth = 2;` for thicker outlines.
- **Error**: Text positioning errors.
  - **Fix**: Adjust coordinates to fit within canvas.

**Validation Check:**
- Verify the text is outlined, not filled.

### Canvas: Linear Gradient
**Example Code:**
```html
<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;"></canvas>
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
var grd = ctx.createLinearGradient(0, 0, 200, 0);
grd.addColorStop(0, "red");
grd.addColorStop(1, "white");
ctx.fillStyle = grd;
ctx.fillRect(10, 10, 150, 80);
</script>
```

**Line-by-Line Explanation:**
- `var grd = ctx.createLinearGradient(0, 0, 200, 0);`:
  - Creates a horizontal gradient from (0,0) to (200,0).
- `grd.addColorStop(0, "red");`:
  - Sets the gradient’s start color to red.
- `grd.addColorStop(1, "white");`:
  - Sets the gradient’s end color to white.
- `ctx.fillStyle = grd;`:
  - Applies the gradient as the fill style.
- `ctx.fillRect(10, 10, 150, 80);`:
  - Fills a rectangle with the gradient.
- **Purpose**: Creates a smooth color transition.
- **Inputs**: Gradient coordinates, color stops, rectangle dimensions.
- **Outputs**: A rectangle with a red-to-white gradient.
- **Side Effects**: Modifies canvas pixels.

**Expected Output:**
A 150x80 rectangle with a horizontal red-to-white gradient at (10,10).

**Common Errors:**
- **Error**: Incorrect gradient coordinates, causing no transition.
  - **Fix**: Ensure start/end points differ (e.g., `0,0` to `200,0`).
- **Error**: Missing `addColorStop`, resulting in no gradient.
  - **Fix**: Add at least two color stops.

**Validation Check:**
- Confirm the gradient transitions smoothly from red to white.

### Canvas: Circular Gradient
**Example Code:**
```html
<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;"></canvas>
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
var grd = ctx.createRadialGradient(75, 50, 5, 90, 60, 100);
grd.addColorStop(0, "red");
grd.addColorStop(1, "white");
ctx.fillStyle = grd;
ctx.fillRect(10, 10, 150, 80);
</script>
```

**Line-by-Line Explanation:**
- `var grd = ctx.createRadialGradient(75, 50, 5, 90, 60, 100);`:
  - Creates a radial gradient with an inner circle at (75,50) with radius 5, and an outer circle at (90,60) with radius 100.
- `grd.addColorStop(0, "red");` and `grd.addColorStop(1, "white");`:
  - Sets the inner color to red and outer to white.
- `ctx.fillStyle = grd; ctx.fillRect(10, 10, 150, 80);`:
  - Fills a rectangle with the radial gradient.
- **Purpose**: Creates a circular color transition.
- **Inputs**: Inner/outer circle coordinates and radii, color stops.
- **Outputs**: A rectangle with a red-to-white radial gradient.
- **Side Effects**: Modifies canvas pixels.

**Expected Output:**
A 150x80 rectangle with a radial gradient centered roughly in the canvas.

**Common Errors:**
- **Error**: Small inner radius or large outer radius causing unexpected gradient spread.
  - **Fix**: Adjust radii (e.g., 5 and 100) to fit the canvas.
- **Error**: Gradient centers outside the rectangle.
  - **Fix**: Align centers with the rectangle’s position.

**Validation Check:**
- Verify the gradient radiates from red to white.

### Canvas: Drawing an Image
**Example Code:**
```html
<img id="scream" src="img_the_scream.jpg" alt="The Scream" style="display:none;">
<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;"></canvas>
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
var img = document.getElementById("scream");
ctx.drawImage(img, 10, 10);
</script>
```

**Line-by-Line Explanation:**
- `<img id="scream" src="img_the_scream.jpg" alt="The Scream" style="display:none;">`:
  - Loads an image, hidden from view (`display:none`).
- `var img = document.getElementById("scream");`:
  - Gets the image element.
- `ctx.drawImage(img, 10, 10);`:
  - Draws the image at (10,10).
- **Purpose**: Displays an image on the canvas.
- **Inputs**: Image object, x, y coordinates.
- **Outputs**: The image rendered on the canvas.
- **Side Effects**: Modifies canvas pixels.

**Expected Output:**
The image (e.g., “The Scream”) at (10,10) on the canvas.

**Common Errors:**
- **Error**: Image not loaded before drawing, causing nothing to appear.
  - **Fix**: Use `img.onload` or ensure the image is loaded.
- **Error**: Invalid `src` path.
  - **Fix**: Verify the image path is correct.

**Validation Check:**
- Confirm the image appears at the specified position.

### SVG: The Basics
The `<svg>` element defines vector graphics in XML, scalable without quality loss. Think of it as a set of instructions for drawing shapes that can be resized perfectly.

**Minimal Example (Building from Scratch):**
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Basic SVG</title>
</head>
<body>
  <svg width="100" height="100">
    <rect x="10" y="10" width="80" height="80" fill="blue" />
  </svg>
</body>
</html>
```

**Line-by-Line Explanation:**
- `<svg width="100" height="100">`:
  - Creates an SVG container of 100x100 pixels.
- `<rect x="10" y="10" width="80" height="80" fill="blue" />`:
  - Draws a rectangle at (10,10) with size 80x80, filled with blue.
  - **Purpose**: Defines a rectangular shape.
  - **Inputs**: Position (x, y), size, fill color.
  - **Outputs**: A blue square.
  - **Side Effects**: None (rendered as a DOM object).
- **Purpose**: Creates scalable vector shapes.
- **Inputs**: XML-based attributes for shapes.
- **Outputs**: Scalable graphics in the browser.
- **Side Effects**: Shapes are stored in the DOM, editable via JavaScript/CSS.

**Expected Output:**
A 100x100 SVG area with an 80x80 blue square.

**Common Errors:**
- **Error**: Missing `width`/`height` on `<svg>`, causing no display.
  - **Fix**: Always set `width` and `height`.
- **Error**: Incorrect attribute names (e.g., `color` instead of `fill`).
  - **Fix**: Use SVG-specific attributes like `fill` and `stroke`.

**Validation Check:**
- Confirm the blue square appears and scales cleanly when zoomed.

### SVG: Circle
**Example Code:**
```html
<svg width="100" height="100">
  <circle cx="50" cy="50" r="40" stroke="green" stroke-width="4" fill="yellow" />
</svg>
```

**Line-by-Line Explanation:**
- `<circle cx="50" cy="50" r="40" stroke="green" stroke-width="4" fill="yellow" />`:
  - `cx="50" cy="50"`: Sets the circle’s center.
  - `r="40"`: Sets the radius to 40px.
  - `stroke="green" stroke-width="4"`: Outlines the circle in green with a 4px width.
  - `fill="yellow"`: Fills the circle with yellow.
- **Purpose**: Draws a filled, outlined circle.
- **Inputs**: Center, radius, stroke/fill properties.
- **Outputs**: A yellow circle with a green border.
- **Side Effects**: Adds to the SVG DOM.

**Expected Output:**
A yellow circle with a green outline in a 100x100 SVG area.

**Common Errors:**
- **Error**: Negative or zero radius.
  - **Fix**: Ensure `r` is positive.
- **Error**: Circle outside SVG bounds.
  - **Fix**: Adjust `cx`, `cy`, and `r` to fit within `width`/`height`.

**Validation Check:**
- Verify the circle is centered with correct colors.

### SVG: Rectangle with Opacity and Rounded Corners
**Example Code:**
```html
<svg width="400" height="180">
  <rect x="50" y="20" rx="20" ry="20" width="150" height="150" style="fill:red;stroke:black;stroke-width:5;opacity:0.5" />
</svg>
```

**Line-by-Line Explanation:**
- `<rect x="50" y="20" rx="20" ry="20" width="150" height="150" style="fill:red;stroke:black;stroke-width:5;opacity:0.5" />`:
  - `x="50" y="20"`: Positions the rectangle.
  - `rx="20" ry="20"`: Rounds corners with 20px radii.
  - `width="150" height="150"`: Sets size.
  - `style="fill:red;stroke:black;stroke-width:5;opacity:0.5"`: Fills red, outlines black, 5px stroke, 50% transparency.
- **Purpose**: Draws a semi-transparent, rounded rectangle.
- **Inputs**: Position, size, corner radii, styles.
- **Outputs**: A red rectangle with rounded corners and black outline.
- **Side Effects**: Adds to the SVG DOM.

**Expected Output:**
A 150x150 red rectangle with rounded corners, semi-transparent, and a black outline.

**Common Errors:**
- **Error**: Invalid `style` syntax (e.g., missing semicolons).
  - **Fix**: Use correct CSS syntax in `style`.
- **Error**: Opacity affecting visibility.
  - **Fix**: Test opacity values (0 to 1).

**Validation Check:**
- Confirm rounded corners and semi-transparency.

### SVG: Star (Polygon)
**Example Code:**
```html
<svg width="300" height="200">
  <polygon points="100,10 40,198 190,78 10,78 160,198" style="fill:lime;stroke:purple;stroke-width:5;fill-rule:evenodd;" />
</svg>
```

**Line-by-Line Explanation:**
- `<polygon points="100,10 40,198 190,78 10,78 160,198" style="fill:lime;stroke:purple;stroke-width:5;fill-rule:evenodd;" />`:
  - `points`: Lists coordinates for the star’s vertices.
  - `fill:lime`: Fills the shape with lime green.
  - `stroke:purple;stroke-width:5`: Outlines with purple, 5px thick.
  - `fill-rule:evenodd`: Determines how overlapping areas are filled.
- **Purpose**: Draws a star shape.
- **Inputs**: Vertex coordinates, fill/stroke styles.
- **Outputs**: A lime star with a purple outline.
- **Side Effects**: Adds to the SVG DOM.

**Expected Output:**
A five-pointed star in lime with a purple outline.

**Common Errors:**
- **Error**: Incorrect `points` syntax (e.g., missing commas).
  - **Fix**: Use `x,y` pairs separated by spaces.
- **Error**: Misunderstanding `fill-rule`.
  - **Fix**: Test `evenodd` vs. `nonzero` for complex shapes.

**Validation Check:**
- Verify the star shape and colors.

### SVG: Gradient Ellipse and Text
**Example Code:**
```html
<svg height="130" width="500">
  <defs>
    <linearGradient id="grad1">
      <stop offset="0%" stop-color="yellow" />
      <stop offset="100%" stop-color="red" />
    </linearGradient>
  </defs>
  <ellipse cx="100" cy="70" rx="85" ry="55" fill="url(#grad1)" />
  <text fill="#ffffff" font-size="45" font-family="Verdana" x="50" y="86">SVG</text>
</svg>
```

**Line-by-Line Explanation:**
- `<defs>`: Defines reusable elements like gradients.
- `<linearGradient id="grad1">`:
  - Creates a gradient with ID `grad1`.
- `<stop offset="0%" stop-color="yellow" />`:
  - Sets the gradient’s start color to yellow.
- `<stop offset="100%" stop-color="red" />`:
  - Sets the end color to red.
- `<ellipse cx="100" cy="70" rx="85" ry="55" fill="url(#grad1)" />`:
  - Draws an ellipse centered at (100,70) with x-radius 85 and y-radius 55, filled with the gradient.
- `<text fill="#ffffff" font-size="45" font-family="Verdana" x="50" y="86">SVG</text>`:
  - Draws white text “SVG” at (50,86).
- **Purpose**: Creates a gradient-filled ellipse with text.
- **Inputs**: Gradient definition, ellipse dimensions, text properties.
- **Outputs**: A yellow-to-red ellipse with white text.
- **Side Effects**: Adds to the SVG DOM.

**Expected Output:**
An ellipse with a yellow-to-red gradient and “SVG” in white text.

**Common Errors:**
- **Error**: Incorrect `id` reference in `fill="url(#grad1)"`.
  - **Fix**: Ensure `id` matches exactly.
- **Error**: Text misaligned due to `y` coordinate.
  - **Fix**: Adjust `x` and `y` for proper placement.

**Validation Check:**
- Confirm the gradient and text alignment.

### Canvas vs. SVG Comparison
- **Canvas**:
  - Pixel-based, drawn via JavaScript.
  - Resolution-dependent (blurry when zoomed).
  - No DOM; graphics are “forgotten” after drawing.
  - Ideal for games or dynamic animations.
- **SVG**:
  - Vector-based, defined in XML.
  - Resolution-independent (sharp at any size).
  - Shapes are DOM objects, editable with JavaScript/CSS.
  - Better for static graphics or animations with event handlers.

## Section 2 — Class Exercise

**Theme**: Create a simple canvas drawing of a house.

**Objectives**:
- Practice using `<canvas>` with `fillRect`, `beginPath`, `moveTo`, `lineTo`, and `stroke`.
- Understand coordinate systems and basic shapes.
- Create a visually recognizable graphic.

**Stepwise Instructions**:
1. Create a `<canvas>` with `id="houseCanvas"`, `width="200"`, `height="200"`, and a black border.
2. In a `<script>`, get the canvas and 2D context.
3. Draw a square for the house body (e.g., 100x100 at (50,50)).
4. Draw a triangular roof using `beginPath`, `moveTo`, and `lineTo` (e.g., triangle from (50,50) to (150,50) to (100,20)).
5. Use `fillStyle` to color the house red and the roof blue.
6. Test in a browser to ensure the house is visible.

**Hints**:
- Use `ctx.fillRect` for the square.
- Use `beginPath` and `closePath` for the triangle.
- Set `fillStyle` before each shape to apply different colors.

**Checkpoints**:
- Does the square appear at the correct position?
- Is the triangle closed and filled correctly?
- Are the colors applied as expected?

**No Solution Provided**: Try building the canvas drawing based on the examples above.

## Section 3 — Weekly Project

**Theme**: Create an interactive SVG logo for a fictional company.

**Milestones**:
1. **Design the Logo**:
   - Use `<svg>` with `width="200"` and `height="200"`.
   - Include a circle, a rectangle, and text (e.g., company initials).
   - Apply a linear gradient to one shape.
2. **Add Interactivity**:
   - Use JavaScript to change the circle’s fill color on click (e.g., toggle between red and blue).
3. **Test Accessibility**:
   - Add a `<title>` element inside the `<svg>` for screen readers (e.g., “Company Logo”).
4. **Research Prompt**:
   - Explore SVG animation with CSS (e.g., W3Schools SVG Tutorial).
5. **Deliverable**:
   - A working HTML file named `logo.html`.

**Success Metrics**:
- Logo displays a circle, rectangle, gradient, and text.
- Circle color changes on click.
- Screen reader announces the `<title>`.
- Graphics scale cleanly when zoomed.

**Extension Ideas**:
- Add a CSS hover effect to scale the rectangle.
- Include a `<polygon>` for an additional shape.
- Research SVG filters for effects like shadows.

**No Solution Provided**: Use the SVG examples to guide your work.

## Completion Checklist
- **Learning Goals**:
  - Understand `<canvas>` methods (`fillRect`, `arc`, `fillText`, etc.).
  - Master SVG elements (`circle`, `rect`, `polygon`, `text`, gradients).
  - Compare Canvas (pixel-based) vs. SVG (vector-based).
- **Runnable Example**:
  - All code snippets are testable in a browser as `.html` files.
- **Checklist for Completion**:
  - [ ] Test canvas examples (line, circle, text, gradients, image).
  - [ ] Verify SVG examples (circle, rectangle, star, gradient ellipse).
  - [ ] Confirm canvas graphics render correctly.
  - [ ] Check SVG shapes scale without quality loss.
  - [ ] Validate JavaScript and SVG interactivity.
- **Common Pitfalls**:
  - Forgetting `stroke()` or `fill()` in canvas, leaving shapes invisible.
  - Missing `width`/`height` attributes, causing display issues.
  - Incorrect SVG attribute names (e.g., `color` instead of `fill`).
  - Running JavaScript before canvas/image loads.
- **One-Line Summary**: HTML `<canvas>` and `<svg>` enable dynamic and scalable graphics, with Canvas using JavaScript for pixel-based drawing and SVG using XML for vector-based shapes.