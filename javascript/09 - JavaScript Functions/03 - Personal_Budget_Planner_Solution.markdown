# Solution to the Weekly Project: Personal Budget Planner

This document provides the complete code solution for the **Personal Budget Planner** project, along with a detailed explanation for JavaScript beginners. The solution demonstrates how to combine functions, parameters, return values, variables, and basic arithmetic in a practical way, building on the lesson's concepts. In a real learning scenario, try solving it yourself before checking the solution!

## Complete Code Solution

```javascript
// Milestone 1: Expense Calculator Function
function calculateExpense(itemCost, quantity) {
  return itemCost * quantity;
}

// Milestone 2: Remaining Budget Function
function remainingBudget(totalBudget, expense1, expense2) {
  return totalBudget - (expense1 + expense2);
}

// Milestone 3: Savings Suggestion Function
function suggestSavings(remaining, savingsPercentage) {
  return remaining * savingsPercentage;
}

// Milestone 4: Combine the Functions
// Example data: $500 budget, food (10 pizzas at $20 each = $200), decorations ($50)
let foodCost = calculateExpense(20, 10); // Calculates $200
let decorationsCost = calculateExpense(50, 1); // Calculates $50
let totalBudget = 500;
let remaining = remainingBudget(totalBudget, foodCost, decorationsCost); // Calculates $250
let savings = suggestSavings(remaining, 0.2); // 20% savings = $50

// Milestone 5: Display the results
console.log(`Your food costs $${foodCost}, decorations cost $${decorationsCost}, remaining budget is $${remaining}, and you should save $${savings}.`);
// Outputs: Your food costs $200, decorations cost $50, remaining budget is $250, and you should save $50.
```

## Step-by-Step Explanation

This solution follows the project milestones exactly, creating a set of reusable functions to plan a school club event budget (like a party). Each part is explained clearly, relating it to everyday experiences like managing pocket money for a group outing with friends. This builds confidence by showing how functions turn simple math into a "pro" tool you can share with your club, saying, "Look what I built to handle our funds!"

### 1. Creating the Expense Calculator Function (`calculateExpense`)

- **Code**: 
  ```javascript
  function calculateExpense(itemCost, quantity) {
    return itemCost * quantity;
  }
  ```
- **Explanation**: This function calculates the total cost for any item by multiplying the price per item (`itemCost`) by how many you need (`quantity`). It's like a basic shopping calculator.
  - **Parameters**: `itemCost` (e.g., $20 for one pizza) and `quantity` (e.g., 10 pizzas) are placeholders for your inputs.
  - **Body and Return**: Uses the `*` operator for multiplication and `return` to send back the result. For example, `20 * 10 = 200`.
  - **Relatable Analogy**: Imagine buying snacks for a school party—you tell the function "pizzas cost $20 each, and we need 10," and it figures out the total like a helpful store clerk, saving you from counting on your fingers.

### 2. Creating the Remaining Budget Function (`remainingBudget`)

- **Code**: 
  ```javascript
  function remainingBudget(totalBudget, expense1, expense2) {
    return totalBudget - (expense1 + expense2);
  }
  ```
- **Explanation**: This function subtracts two expenses from your total budget to find what's left. It uses parentheses to add the expenses first (`expense1 + expense2`), then subtracts with `-`.
  - **Parameters**: `totalBudget` (e.g., $500 from club funds), `expense1` (e.g., food cost), and `expense2` (e.g., decorations cost).
  - **Body and Return**: Simple arithmetic: e.g., `500 - (200 + 50) = 250`. The `return` shares the result.
  - **Relatable Analogy**: Think of checking your allowance after buying games and snacks with friends—this function is like glancing at your wallet to see what's left for the next fun thing, helping you avoid overspending.

### 3. Creating the Savings Suggestion Function (`suggestSavings`)

- **Code**: 
  ```javascript
  function suggestSavings(remaining, savingsPercentage) {
    return remaining * savingsPercentage;
  }
  ```
- **Explanation**: This multiplies the remaining budget by a savings rate (as a decimal, e.g., 0.2 for 20%) to suggest how much to set aside.
  - **Parameters**: `remaining` (e.g., $250 left) and `savingsPercentage` (e.g., 0.2).
  - **Body and Return**: Arithmetic with `*`: e.g., `250 * 0.2 = 50`. Returns the savings amount.
  - **Relatable Analogy**: Like deciding to save some of your birthday money for a future trip—the function acts as a smart piggy bank, calculating "save this much" so you can brag to friends about your responsible planning.

### 4. Combining the Functions

- **Code**: 
  ```javascript
  let foodCost = calculateExpense(20, 10); // Calculates $200
  let decorationsCost = calculateExpense(50, 1); // Calculates $50
  let totalBudget = 500;
  let remaining = remainingBudget(totalBudget, foodCost, decorationsCost); // Calculates $250
  let savings = suggestSavings(remaining, 0.2); // Calculates $50
  ```
- **Explanation**: Here, we call each function with arguments (actual values) and store results in variables. This chains them together: first calculate expenses, then remaining budget, then savings.
  - We reuse `calculateExpense` twice for different categories, showing functions' modularity.
  - Variables like `foodCost` hold results for easy reuse, building on earlier lessons.
  - **Relatable Analogy**: It's like organizing a group picnic—you calculate costs for food and drinks, subtract from your group fund, and decide on savings for the next event, all in one smooth plan that impresses your friends.

### 5. Testing with Real Data and Displaying Results

- **Code**: 
  ```javascript
  console.log(`Your food costs $${foodCost}, decorations cost $${decorationsCost}, remaining budget is $${remaining}, and you should save $${savings}.`);
  ```
- **Explanation**: We use `console.log` with template literals (backticks and `${}`) to print a clear summary. Test with different numbers (e.g., change `totalBudget` to 600) to see updates.
  - Outputs a full sentence for readability, like a report you can show your club.
  - **Why This Matters**: Combines everything into a usable tool; try modifying values to plan real events.
  - **Relatable Analogy**: Picture sharing a budget summary at a club meeting—this is like texting your group: "Here's our plan!" making you the go-to person for organized fun.

This solution is practical and expandable—add more expenses or use arrow functions for practice. Run it in a console to see it in action, and feel proud sharing your "budget app" with peers!