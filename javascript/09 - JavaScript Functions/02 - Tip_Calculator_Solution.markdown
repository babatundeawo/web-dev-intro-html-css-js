# Solution to the Class Exercise: Tip Calculator Function

This document provides the complete code solution for the **Build a Tip Calculator Function** exercise, along with a detailed explanation for JavaScript beginners. The solution demonstrates how functions, parameters, arguments, and return values work in a practical, real-world context, building on the lesson's concepts. In a real learning scenario, try solving it yourself before checking the solution!

## Complete Code Solution

```javascript
// Step 1-3: Define the function with parameters and return the calculated tip
function calculateTip(billAmount, tipPercentage) {
  return billAmount * tipPercentage;
}

// Step 4: Call the function with different examples
let tip1 = calculateTip(50, 0.15);  // $50 bill with 15% tip
let tip2 = calculateTip(100, 0.20); // $100 bill with 20% tip

// Step 5: Display the results in console.log sentences
console.log(`The tip for a $50 bill at 15% is $${tip1.toFixed(2)}.`);  // Outputs: The tip for a $50 bill at 15% is $7.50.
console.log(`The tip for a $100 bill at 20% is $${tip2.toFixed(2)}.`); // Outputs: The tip for a $100 bill at 20% is $20.00.

// Step 6: Testing with incorrect or missing arguments
let tipMissing = calculateTip();      // No arguments
console.log(tipMissing);              // Outputs: NaN (Not a Number)

let tipOneArg = calculateTip(50);     // Only one argument
console.log(tipOneArg);               // Outputs: NaN (because tipPercentage is undefined)
```

## Step-by-Step Explanation

This solution follows the exercise guidance exactly, creating a reusable function to calculate restaurant tips. Each part is explained clearly, using relatable analogies like splitting a bill with friends at a cafe. This builds confidence by showing how a simple function can turn you into the "bill expert" among your peers!

### 1. Defining the Function (`calculateTip`)

- **Code**: 
  ```javascript
  function calculateTip(billAmount, tipPercentage) {
    return billAmount * tipPercentage;
  }
  ```
- **Explanation**: We start with the `function` keyword to declare a new function named `calculateTip`. This name is descriptive, like labeling a recipe "Make Coffee" so you know what it does.
  - **Parameters**: `billAmount` and `tipPercentage` are placeholders (like empty slots on a form). `billAmount` holds the total bill (e.g., $50), and `tipPercentage` holds the tip rate as a decimal (e.g., 0.15 for 15%—remember, percentages in math are divided by 100!).
  - **Body**: Inside the curly brackets `{}`, we multiply `billAmount` by `tipPercentage` using the `*` operator. This is basic arithmetic, like calculating 15% of $50 by doing `50 * 0.15 = 7.5`.
  - **Return Statement**: The `return` keyword sends the result back to wherever the function was called. Without it, the function would calculate the tip but not share it—like figuring out the bill in your head but not telling your friends!
  - **Relatable Analogy**: Think of this function as a quick tip jar calculator at a cafe. You input the bill and tip rate, and it spits out the amount to leave, saving you from mental math during a fun meal.

### 2. Calling the Function with Examples

- **Code**: 
  ```javascript
  let tip1 = calculateTip(50, 0.15);
  let tip2 = calculateTip(100, 0.20);
  ```
- **Explanation**: We "invoke" (call) the function using its name followed by parentheses `()`. Inside the parentheses, we pass **arguments**—actual values that fill in the parameters.
  - For `tip1`: `50` is the argument for `billAmount` (like saying "the bill is $50"), and `0.15` is for `tipPercentage` (15% tip). The function returns `7.5`, which we store in `tip1`.
  - For `tip2`: Similarly, `100` and `0.20` (20% tip) return `20`, stored in `tip2`.
  - **Why Reusable?**: This shows the power of functions—you use the same code for different bills, like reusing a calculator app for various meals instead of buying a new one each time.
  - **Relatable Analogy**: Imagine you're the group leader at dinner; you pull out your "tip calculator" (this function) and quickly figure out tips for everyone's shares, impressing your friends with how efficient you are.

### 3. Displaying Results with `console.log`

- **Code**: 
  ```javascript
  console.log(`The tip for a $50 bill at 15% is $${tip1.toFixed(2)}.`);
  console.log(`The tip for a $100 bill at 20% is $${tip2.toFixed(2)}.`);
  ```
- **Explanation**: We use `console.log` to print messages to the console (like a note on your phone screen). The backticks `` ` `` allow template literals for easy string interpolation with `${}`.
  - `${tip1.toFixed(2)}` formats the number to two decimal places (e.g., `7.5` becomes `7.50` for money). `toFixed(2)` is a built-in method for numbers, rounding to cents.
  - This creates a readable sentence, making the output user-friendly—not just raw numbers.
  - **Relatable Analogy**: It's like texting your friends: "Hey, the tip is $7.50!" instead of just saying "7.5" and leaving them confused. This makes your code feel like a helpful tool you can share.

### 4. Testing with Incorrect or Missing Arguments

- **Code**: 
  ```javascript
  let tipMissing = calculateTip();
  console.log(tipMissing);
  let tipOneArg = calculateTip(50);
  console.log(tipOneArg);
  ```
- **Explanation**: This tests what happens when you forget arguments, as suggested in the exercise.
  - With no arguments: `billAmount` and `tipPercentage` are `undefined`, so `undefined * undefined` returns `NaN` (Not a Number). It's JavaScript's way of saying "I can't calculate without info!"
  - With one argument: `tipPercentage` is `undefined`, so `50 * undefined` is still `NaN`.
  - **Why This Matters**: It teaches that functions need the right inputs to work, like a recipe needing ingredients. In real code, you might add checks (e.g., `if` statements) to handle errors, but that's for later lessons.
  - **Relatable Analogy**: Picture ordering food without specifying the quantity or type—the waiter can't serve you! This experiment builds confidence by showing you how to debug simple issues, so you can fix your own code like a pro.

This solution is simple yet powerful, turning abstract function concepts into a tool you can "brag about" using with friends. If you run this in a browser console or Node.js, you'll see it works perfectly. Practice by modifying it—e.g., add more calls or calculate the total bill including tip—to make it your own!