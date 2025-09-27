# Market Price Calculator Exercise Solution and Explanation

This document provides the code solution to the **Market Price Calculator** class exercise from the JavaScript Operators lesson, tailored for Nigerian beginners. It includes a detailed explanation of the solution, following the **AI Instructional Framework for Teaching JavaScript Beginners (Nigeria-Focused Edition)**. The explanation ensures clarity, uses Nigerian-themed examples, and builds confidence by connecting the code to relatable scenarios.

---

## Section 1 – Explanations

The **Market Price Calculator** exercise requires creating a program that calculates the total cost of buying two items at a market, applies a discount, and displays a message with the final price using `console.log()`. The solution incorporates variables, assignment operators, arithmetic operators, string concatenation, expressions, statements, comments, and proper formatting (white space and line breaks) as covered in the JavaScript Operators lesson.

### Solution Code
```javascript
// Market price calculator for Oyingbo Market
const price1 = 300;
const price2 = 200;
const discount = 50;
let total = price1 + price2 - discount;
let message = "Your total cost after discount is ₦" + total + ".";
console.log(message);
```

### Explanation of the Code
This section breaks down each line of the code, explaining its purpose in simple English, tying it to the lesson’s concepts, and relating it to a Nigerian context.

- **Line 1: `// Market price calculator for Oyingbo Market`**
  - **Concept**: Single-line comment
  - **Explanation**: This comment, starting with `//`, describes the program’s purpose and is ignored by JavaScript. It’s like writing “For market shopping” on a *receipt* to clarify its purpose. Comments make the code easier to understand for you or others, similar to labeling a *market list* with a note like “For Oyingbo purchases”.
  - **Relatable Example**: When you write “For tomatoes and fish” at the top of a *shopping list*, it’s a note for clarity, not part of the actual purchase. This comment serves the same purpose.

- **Line 2: `const price1 = 300;`**
  - **Concepts**: Variable declaration (`const`), identifier (`price1`), number literal (`300`), assignment operator (`=`), semicolon (`;`)
  - **Explanation**: 
    - `const` declares a variable that cannot be reassigned, ideal for a fixed item price. The identifier `price1` uses lower camel case and follows naming rules (starts with a letter, not a reserved word).
    - `= 300` assigns the number literal `300` (no quotes, a number data type) to `price1`, representing ₦300 for an item (e.g., tomatoes).
    - The semicolon (`;`) marks the end of the statement, like a full stop.
  - **Relatable Example**: This is like recording ₦300 for *tomatoes* on a *market list*. Using `const` ensures the price stays fixed, like a set price at *Oyingbo Market*.

- **Line 3: `const price2 = 200;`**
  - **Concepts**: Variable declaration (`const`), identifier (`price2`), number literal (`200`), assignment operator (`=`), semicolon (`;`)
  - **Explanation**: 
    - `const` declares `price2`, another fixed price for a second item (e.g., fish). The identifier `price2` is clear and follows naming rules.
    - `= 200` assigns the number `200` (₦200) to `price2`.
    - The semicolon ends the statement.
  - **Relatable Example**: This is like noting ₦200 for *fish* on the same *market list*. It’s fixed, like a standard price in the market.

- **Line 4: `const discount = 50;`**
  - **Concepts**: Variable declaration (`const`), identifier (`discount`), number literal (`50`), assignment operator (`=`), semicolon (`;`)
  - **Explanation**: 
    - `const` declares `discount`, a fixed discount amount. The identifier `discount` is descriptive.
    - `= 50` assigns the number `50` (₦50) to `discount`.
    - The semicolon ends the statement.
  - **Relatable Example**: This is like getting a ₦50 discount after bargaining at *Oyingbo Market* and recording it on your list.

- **Line 5: `let total = price1 + price2 - discount;`**
  - **Concepts**: Variable declaration (`let`), identifier (`total`), expression (`price1 + price2 - discount`), arithmetic operators (`+`, `-`), assignment operator (`=`), semicolon (`;`)
  - **Explanation**: 
    - `let` declares `total`, using `let` because the total is calculated and could potentially change later (e.g., if more items are added). The identifier `total` is descriptive.
    - The expression `price1 + price2 - discount` adds `300` + `200` to get `500`, then subtracts `50` to get `450`. The `+` and `-` operators perform arithmetic.
    - `=` assigns the result (450) to `total`, and `;` ends the statement.
  - **Relatable Example**: This is like adding ₦300 (tomatoes) + ₦200 (fish) on a *calculator* to get ₦500, then subtracting a ₦50 discount to get ₦450, like calculating your final *market bill*. The `let` allows flexibility if you later adjust the total.

- **Line 6: `let message = "Your total cost after discount is ₦" + total + ".";`**
  - **Concepts**: Variable declaration (`let`), identifier (`message`), expression (string concatenation with `+`), string literals (`"Your total cost after discount is ₦"`, `"."`), assignment operator (`=`), semicolon (`;`)
  - **Explanation**: 
    - `let` declares `message` to store the final output string. `let` is used because the message is calculated and could change if needed.
    - The expression combines:
      - A string literal `"Your total cost after discount is ₦"` for formatting.
      - `total` (450), which is converted to a string during concatenation.
      - A string literal `"."` to end the sentence.
    - The `+` operator concatenates these into one string: “Your total cost after discount is ₦450.”.
    - `=` assigns the concatenated string to `message`, and `;` ends the statement.
  - **Relatable Example**: This is like writing a *market receipt* that says, “Your total cost after ₦50 discount is ₦450.” You’re combining text and the total into a clear message, like a trader summarizing your purchase after bargaining.

- **Line 7: `console.log(message);`**
  - **Concepts**: Statement, expression (`message`), semicolon (`;`)
  - **Explanation**: 
    - `console.log(message)` is a statement that displays the value of `message` (“Your total cost after discount is ₦450.”) in the console, a tool for viewing output, like a digital *market noticeboard*.
    - `message` is an expression that retrieves the stored string.
    - The semicolon ends the statement.
  - **Relatable Example**: This is like showing your *market receipt* to a friend to prove what you paid after bargaining. The console is like a screen displaying your final bill.

- **Formatting Notes**:
  - **White Space**: Spaces around operators (`=`, `+`, `-`) and consistent indentation (two spaces) make the code readable, like neatly writing a *market list*.
  - **Line Breaks**: Each statement is on a new line, keeping the code under 80 characters, similar to writing a clear *exam answer*.
  - **Case Sensitivity**: Identifiers like `price1` and `total` use lower camel case consistently, avoiding errors from case sensitivity.
  - **Block Scope**: All variables are in the global scope here, but `const` and `let` ensure proper scoping if used in blocks later, like separating purchases for different customers.

### Connection to Lesson
The solution uses:
- **Variables** (`const price1`, `const price2`, `const discount`, `let total`, `let message`).
- **Data Types** (numbers for `price1`, `price2`, `discount`, and `total`; strings for `message`).
- **Operators** (`=` for assignment, `+` for arithmetic and concatenation, `-` for subtraction).
- **Expressions** (adding prices, subtracting discount, concatenating strings).
- **Statements** (each line is a complete instruction).
- **Comments** (`// Market price calculator for Oyingbo Market`).
- **Semicolons** (`;`) to separate statements.
- **White Space** for readability.

### Why It’s Exciting
This program mimics a real-world *market receipt* after bargaining at *Oyingbo Market*, a common experience in Nigeria. Students can proudly show it to friends, saying, “I built a market price calculator with JavaScript!” It’s a practical step toward creating apps like *Jumia* or *Konga* that calculate totals for shoppers.

---

## Confidence-Building Note
You’ve just created a program that feels like a real *market receipt* with a discount! This is a big step in mastering JavaScript operators. By using arithmetic and assignment operators, you’re building skills that power real-world apps used across Nigeria, like *Paystack* or *Flutterwave*. Keep practicing, and you’ll soon create even more impressive programs to share with your peers!