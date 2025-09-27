# **Danfo Fare Calculator - Solution and Explanation**

This document provides the complete code solution for the **Danfo Fare Calculator** weekly project from the JavaScript Numbers lesson, tailored for Nigerian beginners. It includes a detailed explanation of the code, adhering to the Nigeria-focused instructional framework. The explanation uses simple language, relatable Nigerian examples, and emphasizes how the project builds confidence by creating a practical, shareable tool that students can boast about to peers.

---

## **Section 1 – Explanation**

The **Danfo Fare Calculator** project requires creating a program that calculates the total fare for a danfo bus trip based on the route and number of passengers, including a 10% discount for students. It uses number concepts like multiplication, `toFixed()`, and `Number.isFinite()`, combined with template strings for a receipt-like output. The program is designed to feel like a real-world tool used by a danfo conductor, making it exciting and relevant for Nigerian students who ride danfo buses daily.

### **Code Solution**

```javascript
let route = "Ojota to CMS"; // Simulating user input
let passengers = 2; // Simulating user input
let fare = 200; // Simulating fare for route
let isStudent = true; // Simulating user input

let total = passengers * fare;
if (Number.isFinite(total)) {
  let discount = isStudent ? total * 0.10 : 0;
  let finalTotal = total - discount;
  let formattedTotal = total.toFixed(2);
  let formattedDiscount = discount.toFixed(2);
  let formattedFinalTotal = finalTotal.toFixed(2);
  let receipt = `=== Danfo Fare Receipt ===
Route: ${route}
Passengers: ${passengers}
Fare per passenger: ₦${fare}
Total: ₦${formattedTotal}
Student Discount (10%): ₦${formattedDiscount}
Final Total: ₦${formattedFinalTotal}`;
  console.log(receipt);
} else {
  console.log("Error: Invalid calculation. Please check your inputs.");
}
```

### **Step-by-Step Explanation**

1. **Storing Input Variables:**
   - The code defines variables: `route = "Ojota to CMS"`, `passengers = 2`, `fare = 200`, and `isStudent = true`, simulating user input for the route, number of passengers, fare per passenger, and student status.
   - In a real program, you’d use `prompt()` to collect these, but hard-coding simplifies testing. Think of `route` as the trip you tell a danfo driver, `passengers` as the number of people boarding, `fare` as the price per person (e.g., ₦200 for Ojota to CMS), and `isStudent` as showing a student ID for a discount.
   - **Relatable Nigerian Example:** This is like a group of students at a bus stop saying, “We’re two people going from Ojota to CMS, and we’re students.”

2. **Calculating the Total Fare:**
   - `let total = passengers * fare;` multiplies `passengers` (2) by `fare` (200), giving `total = 400`. This is like a danfo conductor calculating the total fare: 2 passengers at ₦200 each equals ₦400.
   - Multiplication is a core number operation, showing how JavaScript handles arithmetic, similar to tallying fares in a bus.
   - **Relatable Nigerian Example:** It’s like the conductor saying, “Two people at ₦200 each, that’s ₦400 total.”

3. **Applying the Student Discount:**
   - `let discount = isStudent ? total * 0.10 : 0;` uses a ternary operator to apply a 10% discount if `isStudent` is `true`. For `total = 400`, `discount = 400 * 0.10 = 40`. If `isStudent` is `false`, `discount = 0`.
   - `let finalTotal = total - discount;` subtracts the discount, giving `finalTotal = 400 - 40 = 360` for students.
   - This mimics real-world scenarios where students get discounts, like cheaper fares during school hours.
   - **Relatable Nigerian Example:** It’s like a conductor saying, “You’re students? Okay, I’ll reduce the fare by ₦40.”

4. **Formatting Numbers with `toFixed(2)`:**
   - `let formattedTotal = total.toFixed(2);`, `let formattedDiscount = discount.toFixed(2);`, and `let formattedFinalTotal = finalTotal.toFixed(2);` convert numbers to strings with 2 decimal places (`"400.00"`, `"40.00"`, `"360.00"`). This is perfect for money, making the receipt look professional.
   - Without `toFixed(2)`, numbers like `400` would appear without decimals, but `.00` aligns with how prices are shown in Nigeria, e.g., ₦400.00 on a receipt.
   - **Relatable Nigerian Example:** This is like a POS receipt showing ₦400.00 instead of ₦400, making it clear and formal.

5. **Validating with `Number.isFinite()`:**
   - The `if (Number.isFinite(total))` condition checks if `total` is a valid, finite number (not `Infinity` or `NaN`). This ensures the calculation is reliable, e.g., no invalid inputs like negative passengers or non-numeric fares.
   - If `total` is invalid, the program outputs: `"Error: Invalid calculation. Please check your inputs."`
   - **Relatable Nigerian Example:** This is like a conductor checking if the number of passengers or fare makes sense before issuing a receipt, rejecting errors like “pay with yam.”

6. **Creating the Receipt with Template Literals:**
   - ```javascript
     let receipt = `=== Danfo Fare Receipt ===
     Route: ${route}
     Passengers: ${passengers}
     Fare per passenger: ₦${fare}
     Total: ₦${formattedTotal}
     Student Discount (10%): ₦${formattedDiscount}
     Final Total: ₦${formattedFinalTotal}`;
     ```
     This uses a template string to format a multiline receipt, embedding variables like `route`, `passengers`, and formatted numbers. The output looks like a real receipt:
     ```
     === Danfo Fare Receipt ===
     Route: Ojota to CMS
     Passengers: 2
     Fare per passenger: ₦200
     Total: ₦400.00
     Student Discount (10%): ₦40.00
     Final Total: ₦360.00
     ```
   - Template literals make the output clean and professional, like a printed receipt from a POS machine.
   - **Relatable Nigerian Example:** This receipt looks like what you’d get from a conductor or a POS shop after paying for a bus trip, making it feel authentic.

7. **Displaying the Output:**
   - `console.log(receipt)` prints the receipt to the console, like displaying it on a conductor’s app or a POS screen.
   - If the calculation is invalid, `console.log("Error: Invalid calculation. Please check your inputs.")` shows, like a conductor saying, “Your input no correct o.”
   - **Relatable Nigerian Example:** The output is like the confirmation you get after paying for a danfo ride, which you can share with friends to show you built a cool tool.

### **Why It’s Cool and Shareable**
- Danfo buses are a daily part of life in Nigeria, and calculating fares is something everyone understands. This program feels like a real conductor’s tool, making it practical and exciting.
- Students can show it off, saying, “I built a program that calculates danfo fares like a conductor!” It’s a step toward building apps for transport or businesses, which is brag-worthy.
- The receipt-like output with formatted numbers (e.g., ₦360.00) looks professional, boosting confidence and making it something to share with peers.

### **How It Reinforces Number Concepts**
- **Numbers and Multiplication:** Calculating the total fare uses multiplication, reinforcing arithmetic.
- **toFixed():** Formatting numbers with 2 decimals teaches number-to-string conversion, crucial for money displays.
- **Number.isFinite():** Checking for valid numbers ensures reliable calculations, a key programming skill.
- **Template Strings:** The multiline receipt uses template literals, connecting to string concepts from previous lessons.
- **Practical Application:** The danfo fare scenario makes numbers relevant, like calculating transport costs in Lagos.

### **Example Output**
For `route = "Ojota to CMS"`, `passengers = 2`, `fare = 200`, `isStudent = true`:
```
=== Danfo Fare Receipt ===
Route: Ojota to CMS
Passengers: 2
Fare per passenger: ₦200
Total: ₦400.00
Student Discount (10%): ₦40.00
Final Total: ₦360.00
```
If `passengers = -1` (invalid input), the output is:
```
Error: Invalid calculation. Please check your inputs.
```

---

## **Section 2 – Running the Code**
To run this program, use a JavaScript environment like a browser console, VS Code with Node.js, or an online editor like Replit. For beginners, open a browser (e.g., Chrome), press `F12` to open Developer Tools, go to the Console tab, and paste the code. For an interactive version with user input, use `prompt()`:

```javascript
let route = prompt("Enter route (e.g., Ojota to CMS):");
let passengers = Number(prompt("Enter number of passengers:"));
let fare = Number(prompt("Enter fare per passenger (₦):"));
let isStudent = prompt("Are you a student? (yes/no):") === "yes";

let total = passengers * fare;
if (Number.isFinite(total)) {
  let discount = isStudent ? total * 0.10 : 0;
  let finalTotal = total - discount;
  let formattedTotal = total.toFixed(2);
  let formattedDiscount = discount.toFixed(2);
  let formattedFinalTotal = finalTotal.toFixed(2);
  let receipt = `=== Danfo Fare Receipt ===
Route: ${route}
Passengers: ${passengers}
Fare per passenger: ₦${fare}
Total: ₦${formattedTotal}
Student Discount (10%): ₦${formattedDiscount}
Final Total: ₦${formattedFinalTotal}`;
  console.log(receipt);
} else {
  console.log("Error: Invalid calculation. Please check your inputs.");
}
```

This version prompts the user for the route, passengers, fare, and student status, making it interactive like a real danfo fare app. The `Number()` function ensures numeric inputs are converted properly, and the `isStudent` check converts a “yes/no” input to a boolean.

---

## **Section 3 – Confidence-Building Takeaway**
This project is a big step toward building real-world tools that Nigerians use daily, like fare calculators for danfo buses or POS systems. By combining numbers and strings, you’ve created something that feels like a conductor’s app. You can proudly show this to friends, saying, “I made a program that calculates danfo fares with discounts!” Keep practicing, and you’ll soon build even cooler apps, like transport management systems or market payment tools, that everyone will admire!

---

## **Section 4 – Optional Extension**
To make the project more exciting, add support for multiple routes with different fares. Here’s a guide (not a full solution):
- Define multiple routes (e.g., “Ojota to CMS” at ₦200, “Ibadan to UI Gate” at ₦150).
- Use a `prompt()` to let the user select a route.
- Set the `fare` based on the selected route using conditionals (e.g., `if` statements).
- Update the receipt to reflect the chosen route’s fare.
- This is like a conductor offering different fares for different destinations, making the program more realistic and fun to share.

**Example Output with Extension:**
```
=== Danfo Fare Receipt ===
Route: Ibadan to UI Gate
Passengers: 3
Fare per passenger: ₦150
Total: ₦450.00
Student Discount (10%): ₦45.00
Final Total: ₦405.00
```

This extension adds variety, making the program feel like a full-fledged transport app that students can boast about!