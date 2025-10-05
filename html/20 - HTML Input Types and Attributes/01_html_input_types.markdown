# HTML Input Types and Attributes: Beginner-Friendly Teaching Package

## Section 1 — Topical Explanations

### Overview of HTML Input Types
HTML `<input>` elements allow users to interact with forms by providing data. The `type` attribute defines the kind of input field, like text boxes, buttons, or date pickers. Each type serves a specific purpose, and the default type is `text` if none is specified. Think of input types as different tools in a toolbox—each one is designed for a particular job, like collecting names, passwords, or dates.

Below, we’ll cover the key input types and attributes from the lesson, explaining each with examples, line-by-line breakdowns, and practical tips. We’ll start with a simple example and build it up step-by-step for clarity.

### Input Type: Text
The `<input type="text">` creates a single-line text field for users to enter data like names or addresses.

**Example Code:**
```html
<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname">
</form>
```

**Line-by-Line Explanation:**
- `<form>`: Creates a container for input fields, like a bucket holding all the data you want to collect.
- `<label for="fname">First name:</label>`: The `for` attribute links the label to the input with `id="fname"`. This improves accessibility (screen readers announce the label) and makes the form clickable.
- `<input type="text" id="fname" name="fname">`: 
  - `type="text"`: Specifies a single-line text input.
  - `id="fname"`: A unique identifier for the input, used by the label and JavaScript.
  - `name="fname"`: The key sent to the server when the form is submitted, e.g., `fname=John`.
- `<br>`: Adds a line break for visual spacing in the browser.
- The second `<input>` and `<label>` pair works similarly for the last name.

**Expected Output in Browser:**
A form with two labeled text fields, one for "First name" and one for "Last name," displayed vertically.

**Common Errors and Troubleshooting:**
- **Error**: Forgetting the `name` attribute. Without it, the form data won’t be sent to the server.
  - **Fix**: Always include a `name` attribute matching the field’s purpose.
- **Error**: Mismatched `id` and `for` values. If the label’s `for` doesn’t match the input’s `id`, clicking the label won’t focus the input.
  - **Fix**: Double-check that `id` and `for` values are identical.

**Validation Check:**
- Open the HTML in a browser. Type a name in each field and check if the cursor moves to the input when you click its label.

### Input Type: Password
The `<input type="password">` masks user input (shows asterisks or dots) for secure data like passwords.

**Minimal Example (Building from Scratch):**
Let’s create a simple login form to understand this type.

```html
<form>
  <!-- Step 1: Basic password input -->
  <input type="password" id="pwd" name="pwd">
</form>
```

**Step-by-Step Build-Up:**
1. **Add a label for clarity:**
   ```html
   <form>
     <label for="pwd">Password:</label><br>
     <input type="password" id="pwd" name="pwd">
   </form>
   ```
   - The `<label>` makes it clear what the user should enter.
2. **Add a username field for a complete login form:**
   ```html
   <form>
     <label for="username">Username:</label><br>
     <input type="text" id="username" name="username"><br>
     <label for="pwd">Password:</label><br>
     <input type="password" id="pwd" name="pwd">
   </form>
   ```

**Line-by-Line Explanation:**
- `<input type="password" id="pwd" name="pwd">`:
  - `type="password"`: Masks the input so characters appear as asterisks or dots.
  - `id="pwd"`: Links to the label’s `for` attribute.
  - `name="pwd"`: Identifies the password data when sent to the server.
- **Purpose**: Ensures sensitive data isn’t displayed on the screen.
- **Inputs**: User types any characters (e.g., "mysecret123").
- **Outputs**: Browser shows asterisks (e.g., **********).
- **Side Effects**: None, but the data is sent to the server when the form is submitted.

**Expected Output:**
A form with a text field for username and a password field where typed characters are hidden.

**Common Errors:**
- **Error**: Using `type="text"` instead of `type="password"`. This exposes the password.
  - **Fix**: Always use `type="password"` for sensitive data.
- **Error**: Forgetting to test in different browsers. Some browsers may display masks differently.
  - **Fix**: Test in Chrome, Firefox, and Safari to ensure consistent behavior.

**Validation Check:**
- Type a password and confirm that characters are masked. Submit the form (if connected to a server) to verify the `name` attribute sends data correctly.

### Input Type: Submit
The `<input type="submit">` creates a button to send form data to a server.

**Example Code:**
```html
<form action="/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit" value="Submit">
</form>
```

**Line-by-Line Explanation:**
- `action="/action_page.php"`: Specifies the server URL where form data is sent.
- `<input type="submit" value="Submit">`:
  - `type="submit"`: Defines a button that submits the form.
  - `value="Submit"`: Sets the button’s text. If omitted, the browser uses a default like "Submit Query."
- **Purpose**: Triggers the form submission, sending data like `fname=John&lname=Doe` to the server.
- **Inputs**: User clicks the button.
- **Outputs**: Form data is sent to the `action` URL.
- **Side Effects**: Page may reload or redirect, depending on the server.

**Expected Output:**
A form with two text fields pre-filled with "John" and "Doe," and a "Submit" button.

**Common Errors:**
- **Error**: Missing `action` attribute. The form won’t know where to send data.
  - **Fix**: Ensure the `<form>` has a valid `action` URL.
- **Error**: Button doesn’t work due to JavaScript conflicts.
  - **Fix**: Test the form without JavaScript first to isolate issues.

**Validation Check:**
- Click the submit button and check if the browser attempts to navigate to `/action_page.php`.

### Input Type: Reset
The `<input type="reset">` resets form fields to their default values.

**Example Code:**
```html
<form action="/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit" value="Submit">
  <input type="reset" value="Reset">
</form>
```

**Line-by-Line Explanation:**
- `<input type="reset" value="Reset">`:
  - `type="reset"`: Creates a button that resets all form fields to their initial `value` attributes (or empty if no `value` is set).
  - `value="Reset"`: Sets the button’s text.
- **Purpose**: Clears user changes, restoring default values (e.g., "John" and "Doe").
- **Inputs**: User clicks the reset button.
- **Outputs**: Fields revert to their initial values.
- **Side Effects**: User-entered data is lost unless submitted first.

**Expected Output:**
A form with pre-filled fields and two buttons: "Submit" and "Reset." Clicking "Reset" restores "John" and "Doe."

**Common Errors:**
- **Error**: Expecting `reset` to clear fields completely when `value` attributes are set.
  - **Fix**: Understand that `reset` restores the `value` attribute, not necessarily an empty field.
- **Error**: Overusing `reset` buttons, confusing users.
  - **Fix**: Use sparingly, as users rarely need to reset forms.

**Validation Check:**
- Change the field values, click "Reset," and confirm they revert to "John" and "Doe."

### Input Type: Radio
The `<input type="radio">` allows users to select one option from a group.

**Example Code:**
```html
<form>
  <input type="radio" id="html" name="fav_language" value="HTML">
  <label for="html">HTML</label><br>
  <input type="radio" id="css" name="fav_language" value="CSS">
  <label for="css">CSS</label><br>
  <input type="radio" id="javascript" name="fav_language" value="JavaScript">
  <label for="javascript">JavaScript</label>
</form>
```

**Line-by-Line Explanation:**
- `<input type="radio" id="html" name="fav_language" value="HTML">`:
  - `type="radio"`: Creates a radio button for single-choice selection.
  - `id="html"`: Links to the label.
  - `name="fav_language"`: Groups radio buttons together; only one can be selected in the same `name` group.
  - `value="HTML"`: The data sent to the server if selected (e.g., `fav_language=HTML`).
- **Purpose**: Limits users to one choice from a set.
- **Inputs**: User selects one radio button.
- **Outputs**: The selected `value` is sent on form submission.
- **Side Effects**: Selecting one radio button deselects others in the same `name` group.

**Expected Output:**
Three radio buttons labeled "HTML," "CSS," and "JavaScript," where only one can be selected at a time.

**Common Errors:**
- **Error**: Different `name` attributes for radio buttons meant to be grouped.
  - **Fix**: Ensure all radio buttons in a group share the same `name`.
- **Error**: No `value` attribute. The server receives no data for the selection.
  - **Fix**: Always include a `value` for each radio button.

**Validation Check:**
- Select one radio button and confirm others in the group are deselected.

### Input Type: Checkbox
The `<input type="checkbox">` allows users to select multiple options.

**Example Code:**
```html
<form>
  <input type="checkbox" id="vehicle1" name="vehicle1" value="Bike">
  <label for="vehicle1">I have a bike</label><br>
  <input type="checkbox" id="vehicle2" name="vehicle2" value="Car">
  <label for="vehicle2">I have a car</label><br>
  <input type="checkbox" id="vehicle3" name="vehicle3" value="Boat">
  <label for="vehicle3">I have a boat</label>
</form>
```

**Line-by-Line Explanation:**
- `<input type="checkbox" id="vehicle1" name="vehicle1" value="Bike">`:
  - `type="checkbox"`: Creates a checkbox for multiple selections.
  - `id="vehicle1"`: Links to the label.
  - `name="vehicle1"`: Identifies the data sent to the server.
  - `value="Bike"`: The data sent if the checkbox is checked.
- **Purpose**: Allows users to select zero or more options.
- **Inputs**: User checks any number of boxes.
- **Outputs**: Checked boxes send their `value` to the server (e.g., `vehicle1=Bike&vehicle2=Car`).
- **Side Effects**: None, but each checkbox is independent unless grouped by logic.

**Expected Output:**
Three checkboxes labeled "I have a bike," "I have a car," and "I have a boat," where users can select any combination.

**Common Errors:**
- **Error**: Using the same `name` for checkboxes when they should be independent.
  - **Fix**: Use unique `name` attributes unless you want grouped data.
- **Error**: Forgetting `value` attributes, leading to no data being sent.
  - **Fix**: Always include a `value` for each checkbox.

**Validation Check:**
- Check multiple boxes and confirm they remain selected independently.

### Input Type: Button
The `<input type="button">` creates a clickable button, often used with JavaScript.

**Example Code:**
```html
<input type="button" onclick="alert('Hello World!')" value="Click Me!">
```

**Line-by-Line Explanation:**
- `<input type="button" onclick="alert('Hello World!')" value="Click Me!">`:
  - `type="button"`: Creates a generic button with no default form behavior.
  - `onclick="alert('Hello World!')"`: Runs JavaScript to show a pop-up when clicked.
  - `value="Click Me!"`: Sets the button’s text.
- **Purpose**: Triggers custom actions, usually via JavaScript.
- **Inputs**: User clicks the button.
- **Outputs**: In this case, a browser alert saying "Hello World!".
- **Side Effects**: Depends on the JavaScript (here, just a pop-up).

**Expected Output:**
A button labeled "Click Me!" that shows a "Hello World!" alert when clicked.

**Common Errors:**
- **Error**: JavaScript errors in the `onclick` attribute.
  - **Fix**: Test the JavaScript separately or use a function in a `<script>` tag.
- **Error**: Confusing `type="button"` with `type="submit"`.
  - **Fix**: Use `type="button"` for JavaScript actions, not form submission.

**Validation Check:**
- Click the button and confirm the alert appears.

### Other Input Types (Brief Explanations)
Here’s a quick rundown of the remaining input types from the lesson, with minimal examples for clarity:

- **Color (`<input type="color">`)**: Opens a color picker.
  ```html
  <input type="color" id="favcolor" name="favcolor">
  ```
  - **Purpose**: Select a color (e.g., #FF0000 for red).
  - **Output**: A color code sent to the server.
  - **Common Error**: Limited browser support for the picker.
    - **Fix**: Test in modern browsers like Chrome or Firefox.

- **Date (`<input type="date">`)**: Opens a date picker.
  ```html
  <input type="date" id="birthday" name="birthday" min="2000-01-01" max="2025-12-31">
  ```
  - **Purpose**: Select a date with optional `min` and `max` restrictions.
  - **Output**: A date in `YYYY-MM-DD` format.
  - **Common Error**: Users entering invalid dates.
    - **Fix**: Use `min` and `max` to enforce valid ranges.

- **Datetime-local (`<input type="datetime-local">`)**: Selects date and time.
  ```html
  <input type="datetime-local" id="event" name="event">
  ```
  - **Purpose**: Select a date and time without a timezone.
  - **Output**: A value like `2025-10-05T14:30`.
  - **Common Error**: Inconsistent picker support.
    - **Fix**: Check browser compatibility.

- **Email (`<input type="email">`)**: Validates email format on submission.
  ```html
  <input type="email" id="email" name="email">
  ```
  - **Purpose**: Ensures valid email input (e.g., user@domain.com).
  - **Output**: The entered email.
  - **Common Error**: Relying solely on client-side validation.
    - **Fix**: Add server-side validation.

- **File (`<input type="file">`)**: Uploads files.
  ```html
  <input type="file" id="myfile" name="myfile">
  ```
  - **Purpose**: Allows file selection.
  - **Output**: File data sent to the server.
  - **Common Error**: Missing `enctype="multipart/form-data"` in the `<form>`.
    - **Fix**: Include it for file uploads.

- **Hidden (`<input type="hidden">`)**: Stores data invisible to users.
  ```html
  <input type="hidden" id="custId" name="custId" value="3487">
  ```
  - **Purpose**: Sends data (e.g., user ID) without user interaction.
  - **Output**: Value sent to the server.
  - **Common Error**: Using for sensitive data.
    - **Fix**: Avoid for security-critical data, as it’s visible in source code.

- **Image (`<input type="image">`)**: Uses an image as a submit button.
  ```html
  <input type="image" src="submit.png" alt="Submit" width="48" height="48">
  ```
  - **Purpose**: Submits the form with a clickable image.
  - **Output**: Sends form data and click coordinates.
  - **Common Error**: Missing `alt` attribute.
    - **Fix**: Always include `alt` for accessibility.

- **Month (`<input type="month">`)**: Selects a month and year.
  ```html
  <input type="month" id="bdaymonth" name="bdaymonth">
  ```
  - **Purpose**: Selects a month/year (e.g., 2025-10).
  - **Output**: A value like `2025-10`.
  - **Common Error**: Limited browser support.
    - **Fix**: Provide fallback text input if needed.

- **Number (`<input type="number">`)**: Accepts numeric input with restrictions.
  ```html
  <input type="number" id="quantity" name="quantity" min="1" max="5">
  ```
  - **Purpose**: Restricts input to numbers within a range.
  - **Output**: A number (e.g., 3).
  - **Common Error**: Users typing non-numeric values.
    - **Fix**: Use `min`, `max`, and `step` for control.

- **Range (`<input type="range">`)**: A slider for selecting a number.
  ```html
  <input type="range" id="vol" name="vol" min="0" max="50">
  ```
  - **Purpose**: Selects a number without precise input.
  - **Output**: A number in the range.
  - **Common Error**: No visible value feedback.
    - **Fix**: Add JavaScript to display the current value.

- **Search (`<input type="search">`)**: A text field for searches.
  ```html
  <input type="search" id="gsearch" name="gsearch">
  ```
  - **Purpose**: Behaves like a text field but may have browser-specific features (e.g., clear button).
  - **Output**: The search query.
  - **Common Error**: Assuming advanced search features.
    - **Fix**: Test browser behavior.

- **Tel (`<input type="tel">`)**: For telephone numbers.
  ```html
  <input type="tel" id="phone" name="phone" pattern="[0-9]{3}-[0-9]{2}-[0-9]{3}">
  ```
  - **Purpose**: Accepts phone numbers, often with a pattern.
  - **Output**: The phone number.
  - **Common Error**: Inconsistent formats.
    - **Fix**: Use `pattern` for validation.

- **Time (`<input type="time">`)**: Selects a time.
  ```html
  <input type="time" id="appt" name="appt">
  ```
  - **Purpose**: Selects a time (e.g., 14:30).
  - **Output**: A time value.
  - **Common Error**: Limited browser support.
    - **Fix**: Test in modern browsers.

- **Url (`<input type="url">`)**: Validates URLs.
  ```html
  <input type="url" id="homepage" name="homepage">
  ```
  - **Purpose**: Ensures valid URL input (e.g., https://example.com).
  - **Output**: The URL.
  - **Common Error**: Relying on client-side validation.
    - **Fix**: Add server-side checks.

- **Week (`<input type="week">`)**: Selects a week and year.
  ```html
  <input type="week" id="week" name="week">
  ```
  - **Purpose**: Selects a week (e.g., 2025-W40).
  - **Output**: A week value.
  - **Common Error**: Poor browser support.
    - **Fix**: Provide fallback options.

### Input Attributes
Attributes modify how input fields behave. Here’s a breakdown of key attributes from the lesson:

- **value**: Sets the default value.
  ```html
  <input type="text" id="fname" name="fname" value="John">
  ```
  - **Purpose**: Pre-fills the field (e.g., "John").
  - **Common Error**: Forgetting it’s sent to the server even if unchanged.
    - **Fix**: Verify default values match expectations.

- **readonly**: Prevents editing but allows submission.
  ```html
  <input type="text" id="fname" name="fname" value="John" readonly>
  ```
  - **Purpose**: Displays unchangeable data.
  - **Common Error**: Confusing with `disabled`.
    - **Fix**: Use `readonly` for data that should be sent, `disabled` for data that shouldn’t.

- **disabled**: Makes the field unusable and excludes it from submission.
  ```html
  <input type="text" id="fname" name="fname" value="John" disabled>
  ```
  - **Purpose**: Prevents interaction.
  - **Common Error**: Expecting disabled data to be sent.
    - **Fix**: Use `readonly` if data needs to be submitted.

- **size**: Sets the visible width in characters.
  ```html
  <input type="text" id="fname" name="fname" size="50">
  ```
  - **Purpose**: Controls field width (default is 20).
  - **Common Error**: Confusing with `maxlength`.
    - **Fix**: Use `size` for display, `maxlength` for input limits.

- **maxlength**: Limits the number of characters.
  ```html
  <input type="text" id="pin" name="pin" maxlength="4">
  ```
  - **Purpose**: Restricts input length.
  - **Common Error**: No user feedback when limit is reached.
    - **Fix**: Add JavaScript for alerts.

- **min/max**: Sets numeric or date ranges.
  ```html
  <input type="number" id="quantity" name="quantity" min="1" max="5">
  ```
  - **Purpose**: Restricts input to a range.
  - **Common Error**: Invalid ranges (e.g., `max` < `min`).
    - **Fix**: Validate attribute values.

- **multiple**: Allows multiple selections (for `email` and `file`).
  ```html
  <input type="file" id="files" name="files" multiple>
  ```
  - **Purpose**: Enables multiple inputs.
  - **Common Error**: Forgetting `enctype` for files.
    - **Fix**: Use `multipart/form-data`.

- **pattern**: Validates input with a regular expression.
  ```html
  <input type="text" id="country_code" name="country_code" pattern="[A-Za-z]{3}">
  ```
  - **Purpose**: Enforces specific formats.
  - **Common Error**: Complex patterns confusing users.
    - **Fix**: Use `title` to explain the pattern.

- **placeholder**: Shows a hint in the field.
  ```html
  <input type="tel" id="phone" name="phone" placeholder="123-45-678">
  ```
  - **Purpose**: Guides users on expected input.
  - **Common Error**: Overusing as a label replacement.
    - **Fix**: Always pair with a `<label>`.

- **required**: Makes the field mandatory.
  ```html
  <input type="text" id="username" name="username" required>
  ```
  - **Purpose**: Prevents submission if empty.
  - **Common Error**: Relying solely on client-side validation.
    - **Fix**: Add server-side checks.

- **step**: Sets legal number intervals.
  ```html
  <input type="number" id="points" name="points" step="3">
  ```
  - **Purpose**: Restricts to specific increments.
  - **Common Error**: Incompatible with `min`/`max`.
    - **Fix**: Test valid combinations.

- **autofocus**: Focuses the field on page load.
  ```html
  <input type="text" id="fname" name="fname" autofocus>
  ```
  - **Purpose**: Saves users a click.
  - **Common Error**: Multiple `autofocus` fields.
    - **Fix**: Use only once per page.

- **height/width**: Sets dimensions for `type="image"`.
  ```html
  <input type="image" src="submit.png" alt="Submit" width="48" height="48">
  ```
  - **Purpose**: Controls image size.
  - **Common Error**: Missing `alt`.
    - **Fix**: Always include `alt`.

- **list**: Links to a `<datalist>` for suggestions.
  ```html
  <input list="browsers">
  <datalist id="browsers">
    <option value="Chrome">
    <option value="Firefox">
  </datalist>
  ```
  - **Purpose**: Provides autocomplete options.
  - **Common Error**: Mismatched `list` and `id`.
    - **Fix**: Ensure they match.

- **autocomplete**: Enables/disables browser suggestions.
  ```html
  <input type="email" id="email" name="email" autocomplete="off">
  ```
  - **Purpose**: Controls autofill behavior.
  - **Common Error**: Browser ignoring `autocomplete="off"`.
    - **Fix**: Test in target browsers.

### Form Attributes
These attributes control how `<input>` elements interact with forms:

- **form**: Links an input to a form by ID.
  ```html
  <form id="form1"></form>
  <input type="text" id="lname" name="lname" form="form1">
  ```
  - **Purpose**: Allows inputs outside the `<form>` tag.
  - **Common Error**: Mismatched `form` and `id`.
    - **Fix**: Verify IDs match.

- **formaction**: Overrides the form’s `action` for specific buttons.
  ```html
  <input type="submit" formaction="/admin_page.php" value="Submit as Admin">
  ```
  - **Purpose**: Sends data to a different URL.
  - **Common Error**: Invalid URL.
    - **Fix**: Test the URL separately.

- **formenctype**: Overrides the form’s `enctype`.
  ```html
  <input type="submit" formenctype="multipart/form-data" value="Submit with Files">
  ```
  - **Purpose**: Changes data encoding for specific submissions.
  - **Common Error**: Missing for file uploads.
    - **Fix**: Use with `type="file"`.

- **formmethod**: Overrides the form’s `method` (get/post).
  ```html
  <input type="submit" formmethod="post" value="Submit using POST">
  ```
  - **Purpose**: Changes how data is sent.
  - **Common Error**: Using `get` for sensitive data.
    - **Fix**: Use `post` for security.

- **formtarget**: Overrides the form’s `target`.
  ```html
  <input type="submit" formtarget="_blank" value="Submit to New Tab">
  ```
  - **Purpose**: Controls where the response opens.
  - **Common Error**: Unexpected new tabs.
    - **Fix**: Test behavior in browsers.

- **formnovalidate**: Bypasses validation for specific buttons.
  ```html
  <input type="submit" formnovalidate value="Submit without Validation">
  ```
  - **Purpose**: Allows submission without checks.
  - **Common Error**: Overusing, leading to invalid data.
    - **Fix**: Use sparingly.

- **novalidate (form)**: Disables validation for the entire form.
  ```html
  <form action="/action_page.php" novalidate>
  ```
  - **Purpose**: Skips all client-side validation.
  - **Common Error**: Relying on client-side validation.
    - **Fix**: Always validate server-side.

### Exercise Answers
- **Default value of the INPUT element’s type attribute**: `text`
- **Default value of the INPUT element’s size attribute**: `20`
- **Not a legal form attribute for the INPUT element**: `formtype`

## Section 2 — Class Exercise

**Theme**: Build a simple registration form for a community event.

**Objectives**:
- Practice using `text`, `email`, `date`, `radio`, and `submit` input types.
- Understand the `required` and `placeholder` attributes.
- Create a form that’s user-friendly and accessible.

**Stepwise Instructions**:
1. Create a `<form>` with `action="/register.php"`.
2. Add a `text` input for the user’s full name, with a `<label>` and `required` attribute.
3. Add an `email` input with a `placeholder` like "you@example.com" and `required`.
4. Add a `date` input for the user’s date of birth, with a `max` attribute set to today’s date (2025-10-05).
5. Add three `radio` buttons for selecting an event type (e.g., Workshop, Talk, Networking), ensuring they share the same `name`.
6. Add a `submit` button labeled "Register Now."
7. Test the form in a browser to ensure labels work and fields are required.

**Hints**:
- Use unique `id` attributes for each input and match them with `for` in labels.
- For the `date` input, set `max="2025-10-05"` to prevent future dates.
- Group radio buttons with the same `name` attribute, like `name="event_type"`.

**Checkpoints**:
- Can you click the labels to focus the inputs?
- Does the form prevent submission if required fields are empty?
- Can you select only one radio button at a time?

**No Solution Provided**: Try building the form based on the examples above. If stuck, review the `text`, `email`, and `radio` explanations.

## Section 3 — Weekly Project

**Theme**: Create a "Volunteer Sign-Up Form" for a local charity.

**Milestones**:
1. **Design the Form**:
   - Include inputs for name (`text`), email (`email`), phone (`tel` with a `pattern`), preferred volunteer date (`date`), and volunteer role (`checkbox` for roles like "Fundraising," "Event Setup," "Promotion").
   - Use `required` for name and email, and `placeholder` for phone and email.
2. **Add Submission Options**:
   - Include two `submit` buttons: one for regular submission (`action="/volunteer.php"`) and one for admin submission (`formaction="/admin_volunteer.php"`).
3. **Test Accessibility**:
   - Ensure all inputs have labels and test with a screen reader if possible.
4. **Research Prompt**:
   - Look up how to style forms with CSS to improve their appearance (e.g., W3Schools CSS Forms tutorial).
5. **Deliverable**:
   - A working HTML file with the form, saved as `volunteer_form.html`.

**Success Metrics**:
- Form submits data correctly (test with a dummy server if possible).
- All required fields prevent submission if empty.
- Checkboxes allow multiple selections, and radio buttons (if used) allow only one.
- Labels and inputs are properly linked.

**Extension Ideas**:
- Add a `range` input for volunteers to indicate availability (e.g., hours per week).
- Include a `datalist` for pre-filled city names in a `text` input.
- Research how to validate the form with JavaScript for instant feedback.

**No Solution Provided**: Use the examples and explanations to guide your work.

## Completion Checklist
- **Learning Goals**:
  - Understand the purpose and behavior of `text`, `password`, `submit`, `reset`, `radio`, `checkbox`, `button`, and other input types.
  - Master key attributes like `value`, `readonly`, `disabled`, `required`, `placeholder`, and form-specific attributes.
- **Runnable Example**:
  - All code snippets above are testable in a browser. Save them as `.html` files and open them to see the results.
- **Checklist for Completion**:
  - [ ] Test the `text` and `password` examples to confirm masking and label functionality.
  - [ ] Verify `submit` and `reset` buttons work as expected.
  - [ ] Ensure `radio` buttons allow only one selection and `checkbox` allows multiple.
  - [ ] Try the `button` example to confirm the JavaScript alert.
  - [ ] Experiment with other input types (`color`, `date`, etc.) in a modern browser.
- **Common Pitfalls**:
  - Forgetting `name` attributes, leading to missing form data.
  - Mismatching `id` and `for` attributes, breaking accessibility.
  - Relying on client-side validation without server-side checks.
- **One-Line Summary**: HTML `<input>` types and attributes create interactive, user-friendly forms for collecting and submitting data.