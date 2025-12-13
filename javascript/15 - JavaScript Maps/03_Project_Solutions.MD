## 🚀 Solution Phase: Data Center Resource Allocation Project

This section provides the complete code for the "Data Center Resource Allocation" project from Phase 3, along with detailed explanations of how each stage uses JavaScript Maps, especially leveraging **objects as keys**.

-----

### Project: Data Center Resource Allocation - Solutions

### **Stage 1: Setup & Core Logic**

**Objective:** Define two department objects and create the main `resourceLedger` Map with initial hours allocated, using the objects as the unique keys.

**Code Solution:**

```javascript
// A. Define the unique department keys (objects)
const deptFinance = { name: 'Finance', budget: 'High', id: 'FIN001' };
const deptHR = { name: 'Human Resources', budget: 'Low', id: 'HR002' };
const deptIT = { name: 'IT Infrastructure', budget: 'Medium', id: 'IT003' };

// B. Create the Resource Ledger Map 
const resourceLedger = new Map();

// C. Set initial hours using the objects as keys
resourceLedger.set(deptFinance, 250);
resourceLedger.set(deptHR, 100);
resourceLedger.set(deptIT, 50);

console.log("--- Stage 1: Initial Allocation Setup ---");
console.log(`Finance allocation: ${resourceLedger.get(deptFinance)} hours`);
console.log(`HR allocation: ${resourceLedger.get(deptHR)} hours`);

// Expected Output:
// Finance allocation: 250 hours
// HR allocation: 100 hours
```

**Explanation:**

1.  **Defining Object Keys:** We create three distinct JavaScript objects (`deptFinance`, `deptHR`, `deptIT`). Each object is unique in memory, which is essential because Map keys are compared by **reference**.
2.  **Creating the Map:** `const resourceLedger = new Map();` initializes our central data structure.
3.  **Setting with Objects:** `resourceLedger.set(deptFinance, 250);` uses the actual `deptFinance` object as the key. This means that to retrieve or modify this entry, you must use **this exact same object**.
4.  **Retrieval:** `resourceLedger.get(deptFinance)` successfully fetches `250` because we passed the correct key object reference.

-----

### **Stage 2: Allocation Management (The Brain)**

**Objective:** Implement a robust function to safely add, subtract, or remove allocations based on changes in usage.

**Code Solution:**

```javascript
/**
 * Modifies the resource allocation for a given department.
 * @param {object} departmentKey - The unique department object used as the key.
 * @param {number} hoursChange - The amount of hours to add (positive) or subtract (negative).
 */
function modifyAllocation(departmentKey, hoursChange) {
  // 1. Check if the allocation exists using the department object as the key
  if (resourceLedger.has(departmentKey)) {
    let currentHours = resourceLedger.get(departmentKey);
    let newHours = currentHours + hoursChange;

    if (newHours > 0) {
      // 2. Update the allocation
      resourceLedger.set(departmentKey, newHours);
      console.log(`\t✅ Updated ${departmentKey.name}: ${newHours} hours.`);
    } else {
      // 3. If hours drop to zero or below, remove the allocation
      resourceLedger.delete(departmentKey);
      console.log(`\t🗑️ Allocation for ${departmentKey.name} removed (Hours reached zero).`);
    }
  } else {
    // 4. Handle non-existent key
    console.log(`\t❌ Error: Allocation for ${departmentKey.name} (ID: ${departmentKey.id}) not found.`);
  }
}

console.log("\n--- Stage 2: Allocation Management ---");

// 1. Transaction: Finance needs more compute time (Add 50 hours)
modifyAllocation(deptFinance, 50);

// 2. Transaction: IT has used up its initial budget (Subtract 50 hours)
modifyAllocation(deptIT, -50);

// 3. Transaction: Attempt to modify a non-existent department (Fails gracefully)
const deptUnknown = { name: 'Marketing', budget: 'Low', id: 'MKT004' };
modifyAllocation(deptUnknown, 10);

// Expected Output:
// ✅ Updated Finance: 300 hours.
// 🗑️ Allocation for IT Infrastructure removed (Hours reached zero).
// ❌ Error: Allocation for Marketing (ID: MKT004) not found.
```

**Explanation:**

1.  **Safety Check (`.has()`):** The line `if (resourceLedger.has(departmentKey))` is crucial. It ensures we only proceed if the **exact key object** is present. If we tried to modify an allocation that doesn't exist, the system would fail or create a new entry accidentally.
2.  **Getting and Calculating:** We use `.get()` to retrieve the current hour count, perform the simple addition/subtraction, and store the result in `newHours`.
3.  **Removal Logic (`.delete()`):** The `else` block implements business logic: if a department uses up all its time (`newHours <= 0`), its entry is immediately and permanently removed from the Map using `.delete()`. This cleans up the ledger.
4.  **Error Handling:** When we call `modifyAllocation(deptUnknown, 10)`, the `.has()` check returns `false` because `deptUnknown` is a **new object reference**, even though it has an ID. The system correctly identifies it as unauthorized or unallocated.

-----

### **Stage 3: Reporting**

**Objective:** Generate a report that lists the total number of allocations and prints a line for each department's status.

**Code Solution:**

```javascript
// A. Total Allocations 
console.log("\n--- Stage 3: Reporting ---");
console.log(`Total Active Allocations Remaining: ${resourceLedger.size}`);
// Expected Output: Total Active Allocations Remaining: 2 (Finance and HR remain)

// B. Full Report using forEach
console.log("\n--- Current Resource Status Report ---");
resourceLedger.forEach((hours, departmentObject) => {
  // We access properties directly from the key object
  console.log(`[${departmentObject.id}] Department: ${departmentObject.name} | Hours: ${hours}`);
});
/* Expected Output:
[FIN001] Department: Finance | Hours: 300
[HR002] Department: Human Resources | Hours: 100
*/

// C. Advanced Feature: Seeing the Keys (Order of Addition)
// We use the spread operator (`...`) to convert the iterator into an array for easy printing.
const activeDepartments = [...resourceLedger.keys()].map(key => key.name);
console.log("\nActive Allocations (Order of Addition):", activeDepartments);
// Expected Output: Active Allocations (Order of Addition): [ 'Finance', 'Human Resources' ]

// D. Reflection Task: How to clear the ledger for the next fiscal year
// resourceLedger.clear();
// console.log(`Ledger cleared. New size: ${resourceLedger.size}`);
```

**Explanation:**

1.  **Total Allocations (`.size`):** We quickly check the `resourceLedger.size` property. Notice it is `2` because the `deptIT` allocation was removed in Stage 2.
2.  **Full Report (`.forEach()`):** This is the most effective iteration method. The callback function provides:
      * `hours` (the value, e.g., 300)
      * `departmentObject` (the key, e.g., `{ name: 'Finance', ... }`)
        We can then access properties like `departmentObject.id` and `departmentObject.name` directly from the key object to create a detailed report.
3.  **Order Preservation (`.keys()`):** Using `.keys()` and printing the department names confirms that Maps maintain the order in which the entries were *originally added* (`Finance` then `HR`), even after other entries (`IT`) are deleted.

### **Reflection Tasks Review**

1.  **How would this resource ledger work in a real company?**

      * **In a real company:** This Map acts as an **Authorization and Configuration Store**. The `departmentObject` wouldn't just be created locally; it would likely be retrieved from a secure user management service. Using the actual secure object reference as the Map key ensures that only a process holding that genuine, authoritative object can access or change the allocation. This adds a layer of security and integrity beyond simple string IDs.

2.  **What if the `departmentObject` keys were instead stored as JSON strings?**

      * If we used `JSON.stringify(deptFinance)` as the key, the integrity is lost. Any part of the application that could reconstruct the exact JSON string (`'{"name":"Finance", "budget":"High", "id":"FIN001"}'`) could access the data, even without holding the original object reference. The power of Map's object-key feature is that it binds the value to a unique memory location, preventing this type of "key spoofing."