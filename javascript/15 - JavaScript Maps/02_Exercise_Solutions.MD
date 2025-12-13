## 💡 Solution Phase: Warehouse Inventory System

This section provides the complete, step-by-step solutions for the "Warehouse Inventory System" exercise from Phase 2. Every line of code is explained to reinforce the Map concepts we covered.

-----

### Exercise: Warehouse Inventory System - Solutions

### **Step 1: Setup**

**Instruction:** Create a Map named `inventoryStock` initialized with three items: `"Cable"` (250 units), `"Screw"` (1000 units), and `"Sensor"` (85 units).

**Code Solution:**

```javascript
const inventoryStock = new Map([
  ["Cable", 250],
  ["Screw", 1000],
  ["Sensor", 85]
]);

console.log("--- Step 1: Initial Inventory Setup ---");
console.log("Inventory Map:", inventoryStock);

// Self-Check Question Answer
console.log(`Initial Size: ${inventoryStock.size}`);
// Expected Output: Initial Size: 3
```

**Explanation:**

  * `const inventoryStock = new Map(...)`: We use the `new Map()` constructor and initialize it immediately by passing an array containing the key-value pairs.
  * `["Cable", 250]`: Each inner array represents one entry, where `"Cable"` is the **key** and `250` is the **value**.
  * **Reinforcement:** This setup confirms that Maps can be easily created from existing data structures (like arrays of arrays) and that the `.size` property provides an instant count of the entries.

-----

### **Step 2: Shipment Arrival (Updating)**

**Instruction:** 120 more units of `"Cable"` arrive. Update the stock quantity.

**Code Solution:**

```javascript
// A. Get the current stock quantity for "Cable"
let currentCableStock = inventoryStock.get("Cable"); // Gets 250

// B. Calculate the new stock quantity
let newCableStock = currentCableStock + 120; // 250 + 120 = 370

// C. Update the Map using set()
inventoryStock.set("Cable", newCableStock);

console.log("\n--- Step 2: Shipment Arrival ---");
console.log(`Current Cable Stock: ${inventoryStock.get("Cable")}`);
// Expected Output: Current Cable Stock: 370

// Self-Check Question Answer:
// The method used to update is `Map.set()`.
```

**Explanation:**

  * `inventoryStock.get("Cable")`: We first read the existing value (250).
  * `inventoryStock.set("Cable", newCableStock)`: We use the **`.set()`** method. Since the key `"Cable"` already exists, `set()` **overwrites** the old value (`250`) with the new value (`370`).
  * **Reinforcement:** This demonstrates that `.set()` is a powerful, dual-purpose method for both adding new entries and updating existing ones.

-----

### **Step 3: Order Fulfillment (Deleting)**

**Instruction:** The item `"Screw"` is sold out and removed from the active inventory list.

**Code Solution:**

```javascript
// Remove the "Screw" entry
let deleteScrewStatus = inventoryStock.delete("Screw");

console.log("\n--- Step 3: Order Fulfillment ---");
console.log(`Did 'Screw' deletion succeed? ${deleteScrewStatus}`);
console.log("Current Map entries:", inventoryStock);

// Self-Check Question Answer:
let deleteNailStatus = inventoryStock.delete("Nail");
console.log(`If you try to delete 'Nail' (non-existent), delete returns: ${deleteNailStatus}`);
// Expected Output (for non-existent): false
```

**Explanation:**

  * `inventoryStock.delete("Screw")`: This method finds the key `"Screw"`, removes the entire key-value pair, and returns `true` to confirm the deletion.
  * The Map now only contains `"Cable"` and `"Sensor"`.
  * **Self-Check:** Attempting to delete `"Nail"` fails silently (doesn't cause an error) and returns `false`, confirming that the key was not found and no deletion occurred.

-----

### **Step 4: Check Existence (Using `has()` and `get()` )**

**Instruction:** Write a conditional statement that checks if `"Sensor"` is in stock. If it is, print its quantity. If not, print "Out of Stock."

**Code Solution:**

```javascript
const itemToCheck = "Sensor";

console.log("\n--- Step 4: Check Existence ---");
if (inventoryStock.has(itemToCheck)) {
  const quantity = inventoryStock.get(itemToCheck);
  console.log(`${itemToCheck} is in stock. Quantity: ${quantity}`);
} else {
  console.log(`${itemToCheck} is Out of Stock.`);
}
// Expected Output: Sensor is in stock. Quantity: 85

// Self-Check Question Answer:
if (inventoryStock.has("sensor")) { // Checking for lowercase "sensor"
  console.log("The case-sensitive check for 'sensor' (lowercase) is TRUE");
} else {
  console.log("The case-sensitive check for 'sensor' (lowercase) is FALSE. Maps are case-sensitive.");
}
// Expected Output: The case-sensitive check for 'sensor' (lowercase) is FALSE.
```

**Explanation:**

  * `inventoryStock.has(itemToCheck)`: This method is used first. It checks for the *exact* key and returns a boolean.
  * If `true`, we proceed to `inventoryStock.get(itemToCheck)` to safely retrieve the value.
  * **Self-Check:** Maps are **case-sensitive**. Searching for `"sensor"` (lowercase) fails because the key in the Map is `"Sensor"` (uppercase 'S'). This is a crucial difference from some database systems and a common beginner pitfall.

-----

### **Step 5: Daily Count (Iterating over Entries with `forEach`)**

**Instruction:** Use a loop to print every item name and its remaining quantity, one per line.

**Code Solution:**

```javascript
console.log("\n--- Step 5: Daily Count Report (forEach) ---");
inventoryStock.forEach((quantity, itemName) => {
  // Reminder: forEach callback receives (value, key, map)
  console.log(`Item: ${itemName} | Stock: ${quantity}`);
});
/* Expected Output:
Item: Cable | Stock: 370
Item: Sensor | Stock: 85
*/

// Self-Check Question Answer:
// We should choose `Map.forEach()` or a `for...of` loop with `Map.entries()` because they both provide access to the **key** (item name) and the **value** (quantity) simultaneously.
```

**Explanation:**

  * `inventoryStock.forEach(...)`: This is the cleanest way to iterate when you need both the key and the value for processing or display.
  * The order of arguments in the callback function is fixed: **`(value, key, map)`**. It is important to remember that the **value** comes first.
  * **Reinforcement:** The output order (`Cable`, then `Sensor`) confirms that Maps preserve the **original insertion order** (even after deletion).

-----

### **Step 6: System Maintenance (Iterating over Keys with `keys()`)**

**Instruction:** All items must be marked for quarterly inspection. Use the `.keys()` method and a `for...of` loop to iterate through all remaining items and print: `[ItemName] is scheduled for inspection.`

**Code Solution:**

```javascript
console.log("\n--- Step 6: System Maintenance Schedule (keys()) ---");
for (const itemName of inventoryStock.keys()) {
  console.log(`${itemName} is scheduled for inspection.`);
}
/* Expected Output:
Cable is scheduled for inspection.
Sensor is scheduled for inspection.
*/

// Self-Check Question Answer:
console.log("\nSelf-Check: What if we used .values()?");
for (const value of inventoryStock.values()) {
  console.log(`Value found: ${value}`);
}
/* Expected Output (for values()):
Value found: 370
Value found: 85
*/
```

**Explanation:**

  * `inventoryStock.keys()`: This method returns an iterator containing only the keys (`"Cable"`, `"Sensor"`).
  * `for (const itemName of ...)`: The `for...of` loop consumes the iterator, assigning each key to the `itemName` variable.
  * **Self-Check:** If we used `inventoryStock.values()`, the loop would iterate over the quantities (`370`, `85`) instead of the names, making the output report meaningless for scheduling the *items*. This highlights the importance of choosing the right iterator for the task.