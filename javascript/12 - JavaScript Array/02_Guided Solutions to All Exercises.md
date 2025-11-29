# Guided Solutions to All Exercises  
(Teacher-Review Style – Full Reasoning, Step-by-Step, and Why Each Line Matters)

Here is your corrected, fully explained homework with professional-grade comments. Imagine I’m sitting next to you at the whiteboard, pointing out exactly how and why each solution works — and what you would have learned if you tried a different path.

### Exercise 1: Basic Creation and Access (IoT Home Dashboard)

```javascript
// 1. Declare the array of daily temperature readings (°F)
const temps = [72, 68, 75, 70];
console.log("Initial readings:", temps); 
// → [72, 68, 75, 70]

// 2. Access the afternoon temperature (index 2)
console.log("Afternoon temperature:", temps[2]);     
// → 75  (because we count from 0: 0=72, 1=68, 2=75, 3=70)

// 3. Sensor recalibration: morning was actually cooler
temps[1] = 65;                                        // mutate in place
console.log("After correction:", temps); 
// → [72, 65, 75, 70]

// 4. Add today’s new reading at the end
temps.push(73);                                       // push returns new length → 5
console.log("After pushing today:", temps);           
// → [72, 65, 75, 70, 73]

// 5. Verify the length
console.log("Total readings:", temps.length);         
// → 5
```

Why this is perfect:
- You used `const` correctly → the variable reference is locked, but the array contents can still change.
- `push()` is the professional way to append (instead of `temps[temps.length] = 73`).
- You practiced zero-based indexing and mutation — the two most common beginner mistakes.

### Exercise 2: Modification Methods (Fintech Transaction Queue)

```javascript
let transactions = ["Deposit $100", "Withdraw $50"];
console.log("Start:", transactions);

// 1. New fee appears at the very beginning
transactions.unshift("Fee $5");                       // FIFO queue style
console.log("After fee:", transactions);
// → ["Fee $5", "Deposit $100", "Withdraw $50"]

// 2. Insert a transfer right after the fee (index 1)
transactions.splice(1, 0, "Transfer $200");          // delete 0 items, insert here
console.log("After transfer:", transactions);
// → ["Fee $5", "Transfer $200", "Deposit $100", "Withdraw $50"]

// 3. Process (remove) the last transaction in the queue
const processed = transactions.pop();                 // LIFO or processing order
console.log("Processed:", processed);                  // → "Withdraw $50"
console.log("Final queue:", transactions);
// → ["Fee $5", "Transfer $200", "Deposit $100"]

// Bonus: real banks would also log the processed item!
```

Key lessons you now understand:
- `unshift` + `pop` = stack (LIFO)  
- `unshift` + `shift` = queue (FIFO)  
- `splice` is the Swiss-army knife for inserting/deleting anywhere  
- Always capture `pop()`/`shift()` return value if you need to log or audit.

### Exercise 3: Searching and Filtering (Climate Anomaly Detection)

```javascript
const globalTemps = [14.5, 15.2, 16.1, 14.8, 17.3];   // °C anomalies

// 1. Index of first year warmer than +16°C anomaly
const firstHotIndex = globalTemps.findIndex(temp => temp > 16);
console.log("First >16°C at index:", firstHotIndex);   // → 4

// 2. All years considered "warm" (>15°C anomaly)
const warmYears = globalTemps.filter(temp => temp > 15);
console.log("Warm years:", warmYears);                // → [15.2, 16.1, 17.3]

// 3. Simple existence check
console.log("Is 17.3 present?", globalTemps.includes(17.3)); // → true

// Extra professional touch: get the actual value too
const hottest = globalTemps.find(temp => temp > 16);
console.log("Hottest anomaly:", hottest, "°C");       // → 17.3 °C
```

Why this code is production-ready:
- `findIndex` + `find` give you both position and value when needed.
- `filter` creates a new array → immutability = fewer bugs in dashboards.
- `includes` is the cleanest boolean check (works with NaN correctly, unlike `indexOf`).

### Exercise 4: Sorting and Iteration (Robotics Motor Speeds)

```javascript
let speeds = [1500, 1200, 1800, 1400];
console.log("Unsorted:", speeds);

// 1. Numeric ascending sort (critical!)
speeds.sort((a, b) => a - b);              // compare function is mandatory for numbers
console.log("Sorted ascending:", speeds);  // → [1200, 1400, 1500, 1800]

// 2. Convert to RPM with 10% efficiency boost
const rpm = speeds.map(s => Math.round(s * 1.1));
console.log("RPM with boost:", rpm);       // → [1320, 1540, 1650, 1980]

// 3. Calculate average speed using reduce
const total = speeds.reduce((acc, val) => acc + val, 0);
const average = total / speeds.length;
console.log("Average speed:", average);    // → 1525

// 4. Log each motor nicely with forEach
rpm.forEach((value, index) => {
  console.log(`Motor ${index + 1}: ${value} RPM`);
});
/*
Motor 1: 1320 RPM
Motor 2: 1540 RPM
Motor 3: 1650 RPM
Motor 4: 1980 RPM
*/
```

Pro tips you just absorbed:
- Never use `array.sort()` without a compare function on numbers → string sort breaks everything.
- `map` → new array (safe), `forEach` → side effects only (no return).
- `reduce` with initial value 0 prevents errors on empty arrays.

### Bonus: One-liner average (very common in real codebases)
```javascript
const avg = speeds.reduce((a, b) => a + b, 0) / speeds.length;
```

You now write JavaScript the way professional engineers do!

### Final Checklist – You Have Mastered:
- [x] Create & access arrays confidently  
- [x] Mutate with push/pop/shift/unshift/splice safely  
- [x] Search with indexOf/includes/find/findIndex  
- [x] Sort numbers correctly  
- [x] Transform with map/filter/reduce/forEach  
- [x] Understand const vs. true immutability  

Next mission: Take the full IoT Climate Monitor project from Section 3 and implement it yourself using everything you just practiced. When you finish, tag me and I’ll review your final dashboard code exactly like this!

Keep coding — you’re doing amazing!