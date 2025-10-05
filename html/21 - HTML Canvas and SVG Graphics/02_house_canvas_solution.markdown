# Solution to Class Exercise: Canvas Drawing of a House

This markdown provides the solution to the class exercise described in the HTML Canvas and SVG Graphics teaching package, along with a detailed explanation tailored for beginners. The exercise involves creating a simple house drawing on an HTML `<canvas>` using `fillRect`, `beginPath`, `moveTo`, `lineTo`, and `stroke`, with different colors for the house body and roof.

## Section 1 — Topical Explanations

### Exercise Requirements Recap
The task is to create a simple house drawing on a `<canvas>` with the following specifications:
- Create a `<canvas>` with `id="houseCanvas"`, `width="200"`, `height="200"`, and a black border.
- Use JavaScript to:
  - Draw a square for the house body (e.g., 100x100 at (50,50)).
  - Draw a triangular roof using `beginPath`, `moveTo`, and `lineTo` (e.g., triangle from (50,50) to (150,50) to (100,20)).
  - Color the house body red and the roof blue using `fillStyle`.
- Test in a browser to ensure the house is visible.
- Ensure the square and triangle are correctly positioned and filled with the specified colors.

Below is the complete HTML code solution, followed by a line-by-line explanation, expected output, common errors, and validation checks.

### Solution Code
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>House Drawing on Canvas</title>
</head>
<body>
  <h1>Simple House Drawing</h1>
  <canvas id="houseCanvas" width="200" height="200" style="border:1px solid #000000;"></canvas>
  <script>
    // Get the canvas element
    var canvas = document.getElementById("houseCanvas");
    // Get the 2D drawing context
    var ctx = canvas.getContext("2d");

    // Draw the house body (red square)
    ctx.fillStyle = "red";
    ctx.fillRect(50, 50, 100, 100);

    // Draw the roof (blue triangle)
    ctx.fillStyle = "blue";
    ctx.beginPath();
    ctx.moveTo(50, 50);
    ctx.lineTo(150, 50);
    ctx.lineTo(100, 20);
    ctx.closePath();
    ctx.fill();
  </script>
</body>
</html>
```

### Line-by-Line Explanation
Think of the `<canvas>` as a blank sketchpad where JavaScript acts like a pencil to draw shapes. The house is built by drawing a square for the body and a triangle for the roof, each with a different color.

- `<!DOCTYPE html>`: Declares the document as HTML5 for proper browser rendering.
- `<html lang="en">`: Sets the language to English for accessibility (e.g., screen readers).
- `<head>`:
  - `<meta charset="UTF-8">`: Ensures correct character encoding for special characters.
  - `<title>House Drawing on Canvas</title>`: Sets the browser tab title.
- `<body>`: Contains the visible content.
- `<h1>Simple House Drawing</h1>`: A heading to clarify the canvas’s purpose.
- `<canvas id="houseCanvas" width="200" height="200" style="border:1px solid #000000;">`:
  - `id="houseCanvas"`: Identifies the canvas for JavaScript access.
  - `width="200" height="200"`: Sets the canvas size to 200x200 pixels.
  - `style="border:1px solid #000000;"`: Adds a black border for visibility.
  - **Purpose**: Creates a blank drawing area.
  - **Inputs**: None (static element).
  - **Outputs**: A blank 200x200 rectangle with a black border.
  - **Side Effects**: None until JavaScript draws on it.
- `<script>`: Contains JavaScript to draw the house.
- `var canvas = document.getElementById("houseCanvas");`:
  - Gets the canvas element by its ID.
- `var ctx = canvas.getContext("2d");`:
  - Creates a 2D drawing context (`ctx`), the toolset for drawing shapes.
- `ctx.fillStyle = "red";`:
  - Sets the fill color to red for the next shape.
- `ctx.fillRect(50, 50, 100, 100);`:
  - Draws a filled rectangle at (50,50) with width 100px and height 100px.
  - **Purpose**: Creates the house body as a red square.
  - **Inputs**: Coordinates (x=50, y=50), width (100), height (100).
  - **Outputs**: A red square centered in the canvas.
  - **Side Effects**: Modifies canvas pixels.
- `ctx.fillStyle = "blue";`:
  - Changes the fill color to blue for the roof.
- `ctx.beginPath();`:
  - Starts a new path, ensuring the triangle is drawn independently of the rectangle.
- `ctx.moveTo(50, 50);`:
  - Moves the drawing cursor to (50,50), the top-left corner of the house body, without drawing.
- `ctx.lineTo(150, 50);`:
  - Defines a line to (150,50), the top-right corner of the house body.
- `ctx.lineTo(100, 20);`:
  - Defines a line to (100,20), the peak of the roof.
- `ctx.closePath();`:
  - Closes the triangle by connecting (100,20) back to (50,50).
- `ctx.fill();`:
  - Fills the triangle with blue.
  - **Purpose**: Creates a blue triangular roof.
  - **Inputs**: Coordinates for three points forming a triangle.
  - **Outputs**: A blue triangle above the house body.
  - **Side Effects**: Modifies canvas pixels.

**Purpose**: Draws a simple house with a red square body and a blue triangular roof.
**Inputs**: Coordinates and dimensions for the square and triangle, plus color settings.
**Outputs**: A red 100x100 square and a blue triangle forming a house shape.
**Side Effects**: Permanently alters the canvas pixel data (until redrawn).

### Expected Output in Browser
The canvas displays:
- A 200x200 pixel area with a black border.
- A red square (100x100) centered at (50,50) for the house body.
- A blue triangle with vertices at (50,50), (150,50), and (100,20) forming the roof.
The house resembles a simple geometric shape with the triangle resting atop the square, creating a recognizable house silhouette.

### Common Errors and Troubleshooting
- **Error**: Forgetting `ctx.fill()` for the triangle, leaving it invisible or only outlined.
  - **Fix**: Ensure `fill()` is called after `closePath()` to fill the triangle.
- **Error**: Incorrect coordinates causing the triangle to misalign with the square.
  - **Fix**: Verify triangle points match the square’s top edge (e.g., (50,50) and (150,50)).
- **Error**: Missing `beginPath()`, causing the rectangle and triangle to merge into one shape.
  - **Fix**: Always call `beginPath()` before starting a new shape.
- **Error**: Canvas size too small, cutting off the drawing.
  - **Fix**: Ensure `width="200" height="200"` accommodates the house (150px wide, 130px tall).
- **Error**: JavaScript runs before the canvas is loaded, causing errors.
  - **Fix**: Place `<script>` after `<canvas>` or use `window.onload`.

### Validation Checks
- **Square Position**: Confirm the red square is centered at (50,50) with a 100x100 size.
- **Triangle Shape**: Verify the blue triangle connects (50,50), (150,50), and (100,20), forming a closed shape.
- **Colors**: Check that the square is red and the triangle is blue.
- **Border**: Ensure the canvas has a visible black border.
- **Rendering**: Test in a modern browser (e.g., Chrome, Firefox) to confirm the house displays correctly.

### Runnable Example
Save the code as `house.html` and open it in a modern browser. The house should appear as a red square with a blue triangular roof inside a 200x200 bordered canvas. No server is required, as the drawing is client-side.

## Completion Checklist
- **Learning Goals**:
  - Mastered `<canvas>` methods: `fillRect`, `beginPath`, `moveTo`, `lineTo`, `closePath`, `fill`.
  - Understood coordinate systems for positioning shapes.
  - Applied `fillStyle` to use different colors.
- **Runnable Example**:
  - The provided HTML code is fully testable in a browser as `house.html`.
- **Checklist for Completion**:
  - [ ] Canvas displays with a 200x200 size and black border.
  - [ ] Red square (100x100) appears at (50,50).
  - [ ] Blue triangle connects (50,50), (150,50), and (100,20).
  - [ ] Triangle is filled, not just outlined.
  - [ ] Shapes align to form a house silhouette.
- **Common Pitfalls**:
  - Forgetting `fill()` or `closePath()`, leaving the triangle incomplete.
  - Misaligning triangle coordinates with the square.
  - Not resetting the path with `beginPath()`, causing shape overlap.
  - Using incorrect canvas dimensions, cutting off the drawing.
- **One-Line Summary**: The house drawing uses `<canvas>` with `fillRect` and path methods to create a red square body and blue triangular roof, demonstrating basic shape rendering and color application.