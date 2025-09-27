# Airtime Purchase Advisor Exercise Solution and Explanation

This document provides the code solution to the **Airtime Purchase Advisor** class exercise from the JavaScript Conditionals lesson, tailored for Nigerian beginners. It includes a detailed explanation of the solution, following the **AI Instructional Framework for Teaching JavaScript Beginners (Nigeria-Focused Edition)**. The explanation ensures clarity, uses Nigerian-themed examples, and builds confidence by connecting the code to relatable scenarios.

---

## Section 1 – Explanations

The **Airtime Purchase Advisor** exercise requires creating a program that checks a user’s airtime balance and advises whether they can make a call, send a text, or need to recharge, using `if`, `else if`, and `else` statements. The solution incorporates variables, comparison operators, conditional statements (`if`, `else if`, `else`), string literals, expressions, statements, comments, and proper formatting (white space and line breaks) as covered in the JavaScript Conditionals lesson.

### Solution Code
```javascript
// Airtime purchase advisor for MTN or Glo
const balance = 100;
let advice = "";
if (balance >= 50) {
  advice = "You can make a call.";
} else if (balance >= 20) {
  advice = "You can send a text.";
} else {
  advice = "You need to recharge.";
}
console.log(advice);
```

### Explanation of the Code
This section breaks down each line of the code, explaining its purpose in simple English, tying it to the lesson’s concepts, and relating it to a Nigerian context.

- **Line 1: `// Airtime purchase advisor for MTN or Glo`**
  - **Concept**: Single-line comment
  - **Explanation**: This comment, starting with `//`, describes the program’s purpose and is ignored by JavaScript. It’s like writing “For airtime check” on a *phone recharge slip* to clarify its purpose. Comments make the code easier to understand, similar to labeling a *call credit log* with a note like “For MTN balance”.
  - **Relatable Example**: When you write “For call credit” at the top of a *recharge card*, it’s a note for clarity, not part of the actual balance check. This comment serves the same purpose.

- **Line 2: `const balance = 100;`**
  - **Concepts**: Variable declaration (`const`), identifier (`balance`), number literal (`100`), assignment operator (`=`), semicolon (`;`)
  - **Explanation**: 
    - `const` declares a variable that cannot be reassigned, ideal for the airtime balance since it’s fixed for this check. The identifier `balance` uses lower camel case and follows naming rules (starts with a letter, not a reserved word).
    - `= 100` assigns the number literal `100` (no quotes, a number data type) to `balance`, representing ₦100 of airtime.
    - The semicolon (`;`) marks the end of the statement, like a full stop.
  - **Relatable Example**: This is like checking you have ₦100 airtime on your *MTN* or *Glo* phone, recorded as a fixed amount, like writing your balance on a *recharge slip*.

- **Line 3: `let advice = "";`**
  - **Concepts**: Variable declaration (`let`), identifier (`advice`), string literal (`""`), assignment operator (`=`), semicolon (`;`)
  - **Explanation**: 
    - `let` declares `advice` to store the recommendation message. `let` is used because the message will be calculated based on conditions.
    - `= ""` assigns an empty string to `advice` as a starting point, which will be updated later.
    - The semicolon ends the statement.
  - **Relatable Example**: This is like preparing a blank *note* to write whether you can call, text, or recharge, similar to a placeholder on a *phone app* before checking your balance.

- **Line 4: `if (balance >= 50) {`**
  - **Concepts**: `if` statement, comparison operator (`>=`), expression (`balance >= 50`), curly braces (`{}`), white space
  - **Explanation**: 
    - The `if` statement checks if `balance >= 50` is `true`. Here, `100 >= 50` is `true`, so the code inside the `{}` block will run.
    - The `>=` operator checks if the balance is greater than or equal to 50.
    - Curly braces `{}` define the block of code to execute if the condition is `true`.
    - White space (indentation) makes the code readable.
  - **Relatable Example**: This is like checking if your *airtime* (₦100) is enough to make a call (needs ₦50), similar to a *mobile app* confirming you can call.

- **Line 5: `advice = "You can make a call.";`**
  - **Concepts**: Assignment operator (`=`), string literal (`"You can make a call."`), statement, semicolon (`;`)
  - **Explanation**: 
    - If the `if` condition is `true`, this assigns the string “You can make a call.” to `advice`.
    - The semicolon ends the statement.
  - **Relatable Example**: This is like your *phone* telling you, “You can make a call,” after checking your ₦100 balance is enough, like a *call centre* confirmation.

- **Line 6: `} else if (balance >= 20) {`**
  - **Concepts**: `else if` statement, comparison operator (`>=`), expression (`balance >= 20`), curly braces (`{}`), white space
  - **Explanation**: 
    - The `else if` checks `balance >= 20` if the previous `if` is `false`. Since `balance >= 50` is `true` here, this block is skipped.
    - The `>=` operator checks if the balance is at least 20.
    - Curly braces define the block for this condition.
  - **Relatable Example**: If you don’t have enough airtime for a call, you check if you can send a *text* (needs ₦20), like a backup option on your *phone*.

- **Line 7: `advice = "You can send a text.";`**
  - **Concepts**: Assignment operator (`=`), string literal (`"You can send a text."`), statement, semicolon (`;`)
  - **Explanation**: 
    - If `balance >= 20` is `true` and the previous `if` is `false`, this assigns “You can send a text.” to `advice`.
    - This block is skipped in this case since the `if` block ran.
  - **Relatable Example**: This is like your *phone* suggesting you send a *text* if you have ₦20, like a *WhatsApp* notification.

- **Line 8: `} else {`**
  - **Concepts**: `else` statement, curly braces (`{}`), white space
  - **Explanation**: 
    - The `else` block runs if all previous conditions (`balance >= 50` and `balance >= 20`) are `false`. Here, it’s skipped since `balance >= 50` is `true`.
    - Curly braces define the block for when no conditions are met.
  - **Relatable Example**: If you can’t call or text, your *phone* tells you to recharge, like a *low balance alert*.

- **Line 9: `advice = "You need to recharge.";`**
  - **Concepts**: Assignment operator (`=`), string literal (`"You need to recharge."`), statement, semicolon (`;`)
  - **Explanation**: 
    - If the `else` block runs, this assigns “You need to recharge.” to `advice`.
    - This block is skipped here.
  - **Relatable Example**: This is like a *Glo* message saying, “Recharge your account,” when your balance is too low.

- **Line 10: `}`**
  - **Concept**: Curly brace closing the `else` block
  - **Explanation**: This closes the `else` block, ensuring the code is properly structured.
  - **Relatable Example**: It’s like finishing a *checklist* for your airtime options, ensuring all cases are covered.

- **Line 11: `console.log(advice);`**
  - **Concepts**: Statement, expression (`advice`), semicolon (`;`)
  - **Explanation**: 
    - `console.log(advice)` displays the value of `advice` (“You can make a call.”) in the console, a tool for viewing output, like a digital *phone screen*.
    - `advice` is an expression that retrieves the stored string.
    - The semicolon ends the statement.
  - **Relatable Example**: This is like showing a *friend* your *MTN balance check* result, “You can make a call,” on your phone.

- **Formatting Notes**:
  - **White Space**: Spaces around operators (`>=`, `=`) and consistent indentation (two spaces) make the code readable, like neatly writing a *recharge log*.
  - **Line Breaks**: Each statement is on a new line, keeping the code under 80 characters, similar to a clear *exam answer*.
  - **Case Sensitivity**: Identifiers like `balance` and `advice` use lower camel case consistently, and `if` is lowercase to avoid errors.
  - **Block Scope**: Variables are in the global scope, but `const` and `let` ensure proper scoping if used in blocks later, like separating balances for different users.

### Connection to Lesson
The solution uses:
- **Variables** (`const balance`, `let advice`).
- **Data Types** (number for `balance`, string for `advice`).
- **Conditional Statements** (`if`, `else if`, `else`).
- **Comparison Operators** (`>=`).
- **Expressions** (e.g., `balance >= 50`).
- **Statements** (each line is a complete instruction).
- **Comments** (`// Airtime purchase advisor for MTN or Glo`).
- **Semicolons** (`;`) to separate statements.
- **White Space** for readability.

### Why It’s Exciting
This program mimics a real-world *airtime balance checker*, like what you see when you dial *123# on MTN or Glo. Students can proudly show it to friends, saying, “I built an airtime advisor with JavaScript!” It’s a practical step toward creating apps like *Quickteller* or *Airtel Money*.

---

## Confidence-Building Note
You’ve created a program that feels like a *phone’s airtime checker*! This is a big step in mastering JavaScript conditionals. By using `if`, `else if`, and `else`, you’re building skills that power real-world apps used across Nigeria, like *MTN Mobile Money* or *Glo Quick Recharge*. Keep practicing, and you’ll soon create even more impressive programs to share with your peers!