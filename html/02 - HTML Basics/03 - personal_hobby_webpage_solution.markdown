# Personal Hobby Webpage Solution

This Markdown provides the complete code solution for the **Weekly Project: Build a Personal Hobby Webpage** from the HTML Basics lesson. It includes the full HTML code based on the provided milestones, using example values for personalization (e.g., hobby: soccer, with sample descriptions, link, image, and fun fact). Following the code is a detailed explanation that breaks down each part, reinforcing the HTML concepts from the lesson note. This helps beginners see how the tags and attributes come together to create a structured, visual webpage they can be proud of.

## Code Solution

Save this code in a file named `hobby.html` and open it in a browser to see your personal hobby webpage in action!

```html
<!DOCTYPE html>
<html lang="en">
<body>
<h1>My Love for Soccer</h1>
<h2>Why I Love It</h2>
<p>Soccer is a team sport played with a ball on a field. It's exciting and requires skill and teamwork.</p>
<p>I play soccer every weekend. <br> It keeps me active and happy!</p>
<a href="https://www.fifa.com" title="Check out soccer news!">Visit FIFA for Soccer News</a>
<img src="soccer_ball.jpg" alt="A soccer ball on a green field" width="200" height="150">
<p style="color:red;">Did you know soccer is the most popular sport in the world?</p>
</body>
</html>
```

**Notes on the Code:**
- Replace placeholders like the hobby name, descriptions, facts, link URL, image source, and fun fact with your own details to make it personal.
- For the image, use a real file path (e.g., `soccer_ball.jpg` in the same folder) or an online URL (e.g., `https://via.placeholder.com/200x150`). Ensure any online image is copyright-free.

## Explanation

This explanation breaks down the code milestone by milestone, connecting back to the HTML concepts from the lesson note (e.g., document structure, headings, paragraphs, links, images, and attributes). It uses relatable analogies to make it clear and builds confidence by emphasizing what you'll see in the browser, turning your code into a shareable digital poster.

### Milestone 1: Set Up the Document
- **Code**: `<!DOCTYPE html>`  
  `<html lang="en">` ... `</html>`  
  `<body>` ... `</body>`
- **Explanation**: Start with the `<!DOCTYPE html>` declaration, like a blueprint telling the browser this is an HTML5 document—it ensures everything displays correctly. The `<html>` tag is the root element, like the outer frame of your digital poster, holding all content. The `lang="en"` attribute specifies English for better accessibility. Inside, the `<body>` tag is like the canvas where visible elements go. This basic structure nests everything else, following the lesson's emphasis on proper nesting. In the browser, this setup creates a blank page ready for your hobby details, giving you a solid foundation to build on.

### Milestone 2: Add a Main Heading
- **Code**: `<h1>My Love for Soccer</h1>`  
  `<h2>Why I Love It</h2>`
- **Explanation**: The `<h1>` tag defines the largest heading, like a bold title at the top of your poster announcing your hobby—it's the most important and grabs attention. The `<h2>` is a smaller subheading, like a section label, organizing the content. Each has a start tag, content, and end tag. This demonstrates heading hierarchy from the lesson (<h1> to <h6>). In the browser, you'll see "My Love for Soccer" in large, bold text, followed by "Why I Love It" slightly smaller, making your page look structured and professional right away.

### Milestone 3: Write a Description
- **Code**: `<p>Soccer is a team sport played with a ball on a field. It's exciting and requires skill and teamwork.</p>`  
  `<p>I play soccer every weekend. <br> It keeps me active and happy!</p>`
- **Explanation**: The `<p>` tags create paragraphs, like blocks of text on your poster describing your hobby. The first <p> explains what the hobby is, and the second shares why you enjoy it. Inside the second, the `<br>` is an empty element (no closing tag) that adds a line break, splitting ideas like pressing Enter for a quick list effect. This uses paragraph and empty element concepts from the lesson. In the browser, these appear as spaced-out text blocks below the headings, making your descriptions easy to read and adding personality to your page.

### Milestone 4: Include a Link
- **Code**: `<a href="https://www.fifa.com" title="Check out soccer news!">Visit FIFA for Soccer News</a>`
- **Explanation**: The `<a>` tag makes a hyperlink, like a clickable button on your poster leading to more info. The `href` attribute sets the destination URL (absolute here, but relative works too), and the `title` adds a hover tooltip for extra details. The text between the tags is what's clickable. This ties into the lesson's link examples. In the browser, it shows as underlined blue text; hovering reveals the tooltip, and clicking opens the site—making your page interactive and exciting to share!

### Milestone 5: Add an Image
- **Code**: `<img src="soccer_ball.jpg" alt="A soccer ball on a green field" width="200" height="150">`
- **Explanation**: The `<img>` tag embeds an image, like sticking a photo on your poster to make it visual. It's an empty element with no closing tag. Attributes include `src` for the file path (relative or absolute), `alt` for alternative text (if it doesn't load or for accessibility), and `width`/`height` to size it in pixels. This matches the lesson's image attributes. In the browser, the image appears at the specified size, adding color and fun—if it fails to load, the alt text shows instead.

### Milestone 6: Style a Fun Fact
- **Code**: `<p style="color:red;">Did you know soccer is the most popular sport in the world?</p>`
- **Explanation**: This `<p>` tag adds a paragraph with a fun fact, using the `style` attribute to apply inline styling—like highlighting a note in red marker for emphasis. `style="color:red;"` changes the text color, as per the lesson's style examples. In the browser, this stands out in red below the image, drawing attention and making your poster more engaging.

### Milestone 7: Test and Share
- **Overall**: The code ensures all tags are nested properly (e.g., everything in <body>, no missing end tags) and uses lowercase with quoted attributes for best practices. No case sensitivity issues here, as tags are lowercase.
- **Confidence Booster**: Opening `hobby.html` in a browser reveals a complete webpage: headings organizing your hobby info, readable paragraphs, a working link, a visible image, and a colorful fact—all created by you! It's like a digital poster you can brag about to friends or family. If needed, use Ctrl + U for source view or "Inspect" to check elements, reinforcing the lesson's tools for viewing HTML.

This solution adheres strictly to the tags and attributes from the lesson note, making it a perfect, beginner-built example of a personal hobby page.