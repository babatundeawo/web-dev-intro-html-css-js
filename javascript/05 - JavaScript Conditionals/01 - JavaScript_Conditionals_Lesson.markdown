# JavaScript Conditionals for Beginners (Nigeria-Focused Edition)

This response follows the **AI Instructional Framework for Teaching JavaScript Beginners (Nigeria-Focused Edition)**, covering the provided lesson note on JavaScript Conditionals in detail. The content is broken down into three sections: **Explanations**, **Class Exercise**, and **Weekly Project**, using simple, relatable, and Nigerian-themed examples to make learning clear, practical, and exciting.

---

## Section 1 – Explanations

This section explains the concepts in the lesson note step-by-step, using clear language, Nigerian-themed examples, and confidence-building connections to everyday scenarios.

### 1. Conditional Statements
Conditional statements allow you to run different code based on whether a condition is `true` or `false`.

- **Explanation**: Conditionals are like making decisions in real life. For example, if you have enough *airtime*, you make a call; otherwise, you send a text. JavaScript uses conditionals to choose which code to execute based on conditions.
- **Relatable Example**: When you decide to buy *suya* only if you have ₦500, that’s a condition. If you don’t have enough, you might buy *bole* instead. Conditionals in JavaScript work the same way, deciding what to do based on a situation.

### 2. Types of Conditional Statements
The lesson covers five types of conditionals: `if`, `if...else`, `if...else if...else`, `switch`, and the ternary operator (`?:`).

- **The `if` Statement**:
  ```javascript
  if (hour < 18) {
    greeting = "Good day";
  }
  ```
  - **Explanation**: 
    - The `if` statement checks a condition (e.g., `hour < 18`). If `true`, it runs the code inside the `{}` block. Here, if the hour is less than 18 (6 PM), `greeting` is set to “Good day”.
    - The condition must be in lowercase (`if`, not `If` or `IF`) to avoid errors.
  - **Relatable Example**: If it’s before 6 PM, you might say “Good day” to a *market trader*. If it’s later, you don’t say anything. The `if` statement is like deciding to greet based on the time.

- **The `else` Statement**:
  ```javascript
  if (hour < 18) {
    greeting = "Good day";
  } else {
    greeting = "Good evening";
  }
  ```
  - **Explanation**: 
    - The `else` statement runs if the `if` condition is `false`. Here, if `hour` is 18 or more, `greeting` is set to “Good evening”.
    - It’s a fallback option when the condition isn’t met.
  - **Relatable Example**: If it’s before 6 PM, you greet with “Good day”; otherwise, you say “Good evening” to a *danfo driver*. The `else` is like choosing a different greeting.

- **The `else if` Statement**:
  ```javascript
  if (time < 10) {
    greeting = "Good morning";
  } else if (time < 20) {
    greeting = "Good day";
  } else {
    greeting = "Good evening";
  }
  ```
  - **Explanation**: 
    - `else if` checks a new condition if the previous `if` or `else if` is `false`. Here, if `time < 10` is `false`, it checks `time < 20`. If both are `false`, the `else` block runs.
    - This allows multiple conditions to be tested in sequence.
  - **Relatable Example**: At a *school gate*, if it’s before 10 AM, you say “Good morning”; if it’s before 8 PM, “Good day”; otherwise, “Good evening”. It’s like choosing the right greeting based on the time.

- **The `switch` Statement**:
  ```javascript
  switch (new Date().getDay()) {
    case 0:
      day = "Sunday";
      break;
    case 1:
      day = "Monday";
      break;
    default:
      day = "Another day";
  }
  ```
  - **Explanation**: 
    - The `switch` statement evaluates an expression (e.g., `new Date().getDay()` returns 0–6 for Sunday to Saturday) and matches it to a `case`. If it matches, the code block runs until a `break` stops it.
    - The `default` case runs if no match is found, like a fallback.
    - `break` prevents “fall-through” to the next case.
    - Uses strict comparison (`===`), so types must match.
  - **Relatable Example**: At a *church*, you might have different activities based on the day: Sunday (service), Monday (prayer), or another day (general meeting). `switch` picks the activity like a schedule.

- **The Ternary Operator (`?:`)**:
  ```javascript
  let age = 16;
  let text = (age < 18) ? "Minor" : "Adult";
  ```
  - **Explanation**: 
    - The ternary operator is a shorthand for `if...else`. It has three parts: `condition ? expression1 : expression2`. If `age < 18` is `true`, `text` is “Minor”; otherwise, “Adult”.
    - It’s concise but limited to simple `if...else` cases.
  - **Relatable Example**: At a *cinema*, if you’re under 18, you’re a “Minor” and get a cheaper ticket; otherwise, you’re an “Adult”. The ternary operator is like a quick ticket check.

### 3. Nested `if` Statements
- **Example**:
  ```javascript
  let age = 16;
  let country = "USA";
  let text = "You can Not drive!";
  if (country == "USA") {
    if (age >= 16) {
      text = "You can drive!";
    }
  }
  ```
  - **Explanation**: 
    - An `if` statement inside another `if` checks multiple conditions. Here, it checks if `country` is “USA” and then if `age >= 16`. If both are `true`, `text` is set to “You can drive!”.
    - Nested `if` statements can make code complex.
  - **Relatable Example**: To enter a *school club*, you might need to be in a certain class and over 16. Nested `if` statements check both conditions, like a *school prefect* verifying eligibility.

- **Using Logical AND (`&&`) Instead**:
  ```javascript
  if (country == "USA" && age >= 16) {
    text = "You can drive!";
  }
  ```
  - **Explanation**: The `&&` operator combines conditions, making the code simpler than nested `if` statements. Here, `text` changes if both `country == "USA"` and `age >= 16` are `true`.
  - **Relatable Example**: It’s like a *security guard* checking if you have a *school ID* and are over 16 in one step, instead of two separate checks.

### 4. JavaScript Booleans
Booleans are values that are either `true` or `false`, used in conditions.

- **Examples**:
  ```javascript
  let x = 5;
  Boolean(x < 8); // true
  Boolean(0); // false
  Boolean("Hello"); // true
  ```
  - **Explanation**: 
    - Booleans result from comparisons (e.g., `x < 8` returns `true`). The `Boolean()` function tests if a value is “truthy” or “falsy”.
    - Truthy values: numbers (except 0), non-empty strings, `true`.
    - Falsy values: `0`, `""`, `undefined`, `null`, `NaN`, `false`.
    - Booleans must be lowercase and without quotes.
  - **Relatable Example**: Checking if you have *airtime* (`true`) or not (`false`) decides if you can make a call. A non-empty *wallet* (e.g., ₦100) is truthy, but an empty one (₦0) is falsy.

### 5. JavaScript Logical Operators
Logical operators combine boolean expressions.

- **Logical AND (`&&`)**:
  ```javascript
  let x = 6;
  let y = 3;
  let z = (x < 10 && y > 1); // true
  ```
  - **Explanation**: `&&` returns `true` if both conditions are `true`. Here, `x < 10` (true) and `y > 1` (true) make `z` true.
  - **Relatable Example**: To board a *danfo*, you need both enough *money* and a *destination*. Both must be true.

- **Logical OR (`||`)**:
  ```javascript
  let x = 6;
  let y = -3;
  let z = (x > 0 || y > 0); // true
  ```
  - **Explanation**: `||` returns `true` if at least one condition is `true`. Here, `x > 0` (true) makes `z` true, even though `y > 0` is false.
  - **Relatable Example**: You can pay a *danfo* fare with *cash* or a *card*. If either is available, you can board.

- **Logical NOT (`!`)**:
  ```javascript
  let x = (5 == 8); // false
  let y = !(5 == 8); // true
  ```
  - **Explanation**: `!` reverses a boolean. If `5 == 8` is `false`, `!` makes it `true`.
  - **Relatable Example**: If you’re *not* a student (`!isStudent`), you pay the full *danfo* fare.

- **Nullish Coalescing (`??`)**:
  ```javascript
  let name = null;
  let text = name ?? "missing"; // text = "missing"
  ```
  - **Explanation**: `??` returns the second value if the first is `null` or `undefined`. Here, since `name` is `null`, `text` is set to “missing”.
  - **Relatable Example**: If a *passenger’s name* isn’t provided (`null`), you use “missing” on the *ticket*, like a placeholder.

---

## Section 2 – Class Exercise

This exercise is designed to be fun, Nigerian-themed, and practical, allowing students to practice conditionals while building something they can boast about.

### Exercise: Airtime Purchase Advisor
**Objective**: Create a program that checks how much airtime a user has and advises whether they can make a call, send a text, or need to recharge, based on their balance.

**Why It’s Cool**: Students will feel proud to create a program that mimics an *airtime balance checker*, like checking your MTN or Glo balance. They can show friends, “I built an airtime advisor with JavaScript!”

**Instructions**:
1. Declare a variable for the user’s airtime balance using `const` (e.g., ₦100).
2. Use `if`, `else if`, and `else` to check:
   - If balance is ≥ ₦50, advise they can make a call.
   - If balance is ≥ ₦20 but < ₦50, advise they can send a text.
   - Otherwise, advise they need to recharge.
3. Store the advice in a variable and use `console.log()` to display it.
4. Add a comment explaining what your code does.
5. Ensure readability with spaces, indentation, and lines under 80 characters.

**Guidance (No Solution)**:
- Think of checking your *phone’s airtime balance* (e.g., “You can call with ₦50”).
- Use `const` for the balance since it’s fixed, and `let` for the advice message.
- Use comparison operators (`>=`, `<`) in conditions.
- Example structure (not the answer):
  ```javascript
  // My airtime purchase advisor
  const balance = ...;
  let advice = "";
  if (...) {
    advice = "...";
  } else if (...) {
    advice = "...";
  } else {
    advice = "...";
  }
  console.log(advice);
  ```

**Connection to Lesson**: This uses `if`, `else if`, `else`, comparison operators (`>=`, `<`), variables, assignment (`=`), string literals, statements, comments, and white space.

---

## Section 3 – Weekly Project

This project combines the lesson’s concepts into a practical, Nigerian-themed task that students will be excited to share.

### Project: Danfo Fare Discount System
**Objective**: Build a program that calculates a *danfo* passenger’s fare, applies a discount based on their status (student or not) and time of day, and displays a message with the final fare.

**Why It’s Exciting**: Students will create a tool that feels like a *danfo conductor’s fare system*, applying discounts for students or off-peak hours, like in Lagos. They can boast, “My program calculates danfo fares with discounts!” It’s relatable and practical in Nigeria.

**Project Brief**:
- **Goal**: Create a program that:
  1. Stores the passenger’s fare, student status, and travel hour in `const` variables.
  2. Calculates the final fare with discounts using `if...else` or ternary operators.
  3. Displays a message like “Your fare with student discount is ₦150.”
- **Milestones**:
  1. Declare `const` variables for fare (e.g., ₦200), `isStudent` (e.g., `true`), and `hour` (e.g., 15 for 3 PM).
  2. Use `if...else` or ternary to apply:
     - A 20% discount if `isStudent` is `true`.
     - A 10% discount if `hour` is before 12 (noon).
     - Both discounts if both conditions are true (using `&&`).
  3. Store the final fare and a message using `let`.
  4. Use `console.log()` to display the message.
  5. Add comments to explain each section.
  6. Ensure readability with spaces and line breaks.
- **Extension Ideas**:
  - Include route names (e.g., “Oshodi to CMS”).
  - Add a message if no discount applies.
- **Relatable Scenario**: Imagine a *danfo conductor* reducing the fare for a student or during morning hours. Your program acts like a smart fare calculator.

**Guidance (No Solution)**:
- Use `const` for fare, status, and hour since they’re fixed.
- Use `let` for the final fare and message since they’re calculated.
- Use `&&` to combine conditions or a ternary for concise logic.
- Break long strings into lines for readability.
- Example structure:
  ```javascript
  // My danfo fare discount system
  const fare = ...;
  const isStudent = ...;
  const hour = ...;
  let finalFare = ...;
  let message = ...;
  console.log(...);
  ```

**Connection to Lesson**: This uses `if...else`, ternary operator, logical operators (`&&`), comparison operators (`<`), variables, assignment (`=`), arithmetic (`*`), string concatenation, statements, comments, white space, and line breaks.

---

## Confidence-Building Note
By completing this exercise and project, you’re building tools like an *airtime advisor* or *danfo fare calculator* that feel real and useful in Nigeria. These skills are the foundation of apps like *MTN Quick Recharge* or *Opay*. Keep practicing, and you’ll soon create programs that impress your friends and family!