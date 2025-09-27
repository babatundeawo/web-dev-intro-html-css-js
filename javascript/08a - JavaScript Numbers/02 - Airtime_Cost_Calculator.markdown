# **Airtime Cost Calculator - Solution and Explanation**

This document provides the complete code solution for the **Airtime Cost Calculator** class exercise from the JavaScript Numbers lesson, tailored for Nigerian beginners. It includes a detailed explanation of the code, adhering to the Nigeria-focused instructional framework. The explanation uses simple language, relatable Nigerian examples, and emphasizes how the program builds confidence by creating a practical, shareable tool that students can boast about to peers.

---

## **Section 1 – Explanation**

The **Airtime Cost Calculator** exercise requires creating a program that calculates the total cost of airtime based on the number of units and price per unit, then formats the result as a string for display. It uses number concepts like multiplication, `toFixed()`, and `Number.isNaN()`, combined with template strings for output. The program is designed to feel like a tool a vendor might use at a POS shop, making it exciting and relevant for Nigerian students who buy airtime daily.

### **Code Solution**

```javascript
let units = 5; // Simulating user input
let pricePerUnit = 100; // Simulating user input

let total = units * pricePerUnit;
if (!Number.isNaN(total)) {
  let formattedTotal = total.toFixed(2);
  let message = `Total cost for ${units} units: ₦${formattedTotal}`;
  console.log(message);
} else {
  console.log("Error: Invalid calculation. Please check your inputs.");
}
```

### **Step-by-Step Explanation**

1. **Storing Input Variables:**
   - The code defines two variables: `units = 5` and `pricePerUnit = 100`, simulating user input for the number of airtime units (e.g., 5 units of ₦100 airtime) and the price per unit.
   - In a real program, you’d use `prompt()` to get these values, but hard-coding simplifies testing. Think of `units` as the number of ₦100 airtime cards you buy at a roadside shop, and `pricePerUnit` as the cost of each card.
   - **Relatable Nigerian Example:** This is like a customer telling a vendor, “I want 5 units of ₦100 MTN airtime.”

2. **Calculating the Total:**
   - `let total = units * pricePerUnit;` multiplies `units` (5) by `pricePerUnit` (100), giving `total = 500`. This is like a vendor calculating your bill: 5 units at ₦100 each equals ₦500.
   - Multiplication is a core number operation, showing how JavaScript handles basic arithmetic, similar to tallying items at a market.
   - **Relatable Nigerian Example:** It’s like a POS agent saying, “5 units at ₦100 is ₦500 total.”

3. **Checking for Valid Calculation with `Number.isNaN()`:**
   - The `if (!Number.isNaN(total))` condition checks if `total` is a valid number (not `NaN`). This ensures the calculation worked, e.g., no invalid inputs like dividing by “fish.”
   - If `total` is `NaN` (e.g., if `units` or `pricePerUnit` were non-numeric), the program outputs: `"Error: Invalid calculation. Please check your inputs."`
   - **Relatable Nigerian Example:** This is like a vendor checking if your payment amount makes sense before processing it, rejecting nonsense inputs like “pay with yam.”

4. **Formatting the Total with `toFixed(2)`:**
   - `let formattedTotal = total.toFixed(2);` converts the `total` (500) to a string with 2 decimal places (`"500.00"`). This is ideal for money, making the output look professional, like a receipt.
   - Without `toFixed(2)`, a number like `500` might display as `"500"`, but adding `.00` mimics how prices are shown in Nigeria, e.g., ₦500.00 on a POS screen.
   - **Relatable Nigerian Example:** This is like a receipt showing ₦500.00 instead of just ₦500, making it clear and formal.

5. **Creating the Output with Template Literals:**
   - `let message = `Total cost for ${units} units: ₦${formattedTotal}`;` uses a template string to format the output, embedding `units` and `formattedTotal`. It produces: `Total cost for 5 units: ₦500.00`.
   - Template literals (backticks) make it easy to combine numbers and text, like writing a neat receipt note.
   - **Relatable Nigerian Example:** The output looks like a message from a vendor: “Your total for 5 units is ₦500.00,” similar to what you’d see after buying airtime.

6. **Displaying the Output:**
   - `console.log(message)` prints the formatted message to the console, like showing the total on a POS machine’s screen.
   - If the calculation is invalid, `console.log("Error: Invalid calculation. Please check your inputs.")` displays, like a vendor saying, “Oga, your input no correct o.”
   - **Relatable Nigerian Example:** The output is like the confirmation you get after buying airtime, which you can share with friends to show you built a useful tool.

### **Why It’s Cool and Shareable**
- Airtime purchases are a daily activity in Nigeria, whether for calls, data, or SMS. This program feels like a mini POS system, making it practical and exciting.
- Students can show it off to peers, saying, “I made a program that calculates airtime costs like a vendor!” It’s a small step toward building real-world apps, like a payment system.
- The formatted output (e.g., ₦500.00) looks professional, boosting confidence and making it brag-worthy.

### **How It Reinforces Number Concepts**
- **Numbers and Multiplication:** The program uses multiplication to calculate the total, reinforcing basic arithmetic.
- **toFixed():** Formatting the total with 2 decimals teaches number-to-string conversion, crucial for money-related outputs.
- **Number.isNaN():** Checking for `NaN` teaches input validation, a key skill for reliable programs.
- **Template Strings:** Combining numbers with text in a template literal ties in string concepts from previous lessons.
- **Practical Application:** The airtime scenario makes numbers feel relevant, like calculating costs at a local shop.

### **Example Output**
For `units = 5` and `pricePerUnit = 100`, the output is:
```
Total cost for 5 units: ₦500.00
```
If `units = "fish"` (invalid input), the output is:
```
Error: Invalid calculation. Please check your inputs.
```

---

## **Section 2 – Running the Code**
To run this program, use a JavaScript environment like a browser console, VS Code with Node.js, or an online editor like Replit. For beginners, open a browser (e.g., Chrome), press `F12` to open Developer Tools, go to the Console tab, and paste the code. For an interactive version with user input, use `prompt()`:

```javascript
let units = Number(prompt("Enter number of airtime units:"));
let pricePerUnit = Number(prompt("Enter price per unit (₦):"));

let total = units * pricePerUnit;
if (!Number.isNaN(total)) {
  let formattedTotal = total.toFixed(2);
  let message = `Total cost for ${units} units: ₦${formattedTotal}`;
  console.log(message);
} else {
  console.log("Error: Invalid calculation. Please check your inputs.");
}
```

This version asks the user to input the number of units and price, making it interactive like a real POS transaction. The `Number()` function ensures inputs are converted to numbers, preventing errors like string concatenation.

---

## **Section 3 – Confidence-Building Takeaway**
This program is a practical step toward building tools Nigerians use every day, like calculating airtime costs at a vendor’s shop. By mastering numbers and string formatting, you’ve created something that feels like a real POS system. You can proudly show this to friends, saying, “I built a program that calculates airtime costs!” Keep practicing, and you’ll soon create even cooler apps, like a full payment system or a market calculator, that everyone will admire!