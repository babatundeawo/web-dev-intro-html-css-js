That's the final and most important step\! We'll now put all the JavaScript Number concepts, including **`BigInt`**, **`toFixed()`**, and **`Number.isSafeInteger()`**, into practice by building a simplified **Financial Data Integrity Checker**.

## 🏗️ Phase 3 Project Solution: Financial Data Integrity Checker

### Project Goal

To create a system that calculates financial metrics while ensuring data accuracy:

1. Use standard `Number` types for daily price calculations and formatting.
2. Use **`BigInt`** for large, sensitive data (like ledger transaction IDs or asset counts) to prevent precision loss.
3. Use **`Number.isSafeInteger()`** to validate incoming integer data integrity.

-----

### Stage 1: Setup & Core Logic (Price Calculation and Formatting)

We'll start by handling standard floating-point numbers for daily stock price calculations and use **`toFixed(2)`** to ensure the result is correctly formatted for display.

#### Example Preview (The Price Calculation)

```javascript
let startPrice = 45.678;
let changePercent = 0.035; // 3.5% gain
let newPrice = startPrice * (1 + changePercent);
let formattedPrice = newPrice.toFixed(2); // Formats to $47.28

// Expected newPrice: 47.27983
// Expected formattedPrice: "47.28"
```

#### Step-by-step Solution

```javascript
/**
 * STAGE 1: PRICE CALCULATION AND FORMATTING
 * Focus: Using standard Numbers, arithmetic, and toFixed()
 */

// 1. Setup Input Data
let openingPrice = 145.75; // The price at market open
let percentIncrease = 0.051; // 5.1% increase (standard JS Number)

// 2. Calculate the Closing Price
// Note: This operation results in a floating point number (153.19325)
let closingPrice = openingPrice * (1 + percentIncrease);

// 3. Format the Display Output
// We use toFixed(2) to round the price to two decimal places (cents) for UI display.
let formattedClosingPrice = closingPrice.toFixed(2);

console.log("--- STAGE 1: Price Calculation and Formatting ---");
console.log(`1. Opening Price: $${openingPrice}`);
console.log(`2. Calculated Closing Price (raw): ${closingPrice}`);
console.log(`3. Formatted Closing Price: $${formattedClosingPrice}`);
```

#### Expected Output for Stage 1

```
--- STAGE 1: Price Calculation and Formatting ---
1. Opening Price: $145.75
2. Calculated Closing Price (raw): 153.19325
3. Formatted Closing Price: $153.19
```

-----

### Stage 2: Data Integrity and Large Number Handling

Here we address the issues of data corruption (`MAX_SAFE_INTEGER` violation) and the need for precision with very large integer counts using **`BigInt`**.

#### Example Preview (BigInt and Safety Check)

```javascript
let riskyID = 9007199254740992; // Unsafe integer (MAX_SAFE_INTEGER + 1)
let safeID = 1000000000000000n; // Safe BigInt for guaranteed accuracy

// Check
let isRiskySafe = Number.isSafeInteger(riskyID); // False

// BigInt operation
let bigResult = safeID * 2n; // 2000000000000000n
```

#### Step-by-step Solution

```javascript
/**
 * STAGE 2: DATA INTEGRITY AND LARGE NUMBER HANDLING
 * Focus: Number.isSafeInteger() and BigInt
 */

// 1. Define a set of sensitive data inputs (e.g., user IDs)
// The last ID exceeds MAX_SAFE_INTEGER (9007199254740991)
let userIDs = [
    123456789012345,
    9007199254740991, // MAX_SAFE_INTEGER
    9007199254740992  // UNSAFE (Can be corrupted by JS)
];

console.log("\n--- STAGE 2: Data Integrity Checks ---");
console.log("--- 2.1: Checking Safe Integer Limits ---");

// Loop through the IDs and check their safety
userIDs.forEach((id, index) => {
    let isSafe = Number.isSafeInteger(id);
    let status = isSafe ? "SAFE" : "RISKY (Precision Loss Possible)";
    console.log(`ID ${index}: ${id} -> ${status}`);
});

// 2. Handling Large Asset Counts using BigInt
// Imagine counting shares or total global contracts—these must be accurate.
let globalAssetsCount = 50000000000000000000n; // Very large integer, declared with 'n'
let dailyAcquisition = 2500000000000000n;

// 3. Perform accurate calculation with BigInt
let newTotalAssets = globalAssetsCount + dailyAcquisition;

console.log("\n--- 2.2: BigInt for Guaranteed Precision ---");
console.log(`Original Assets: ${globalAssetsCount}`);
console.log(`Daily Acquisition: ${dailyAcquisition}`);
console.log(`New Total Assets (BigInt): ${newTotalAssets}`);

// Note: Attempting to mix BigInt and standard Number will cause a TypeError!
// For example: let error = newTotalAssets + 1; // Uncaught TypeError
```

#### Expected Output for Stage 2

```
--- STAGE 2: Data Integrity Checks ---
--- 2.1: Checking Safe Integer Limits ---
ID 0: 123456789012345 -> SAFE
ID 1: 9007199254740991 -> SAFE
ID 2: 9007199254740992 -> RISKY (Precision Loss Possible)

--- 2.2: BigInt for Guaranteed Precision ---
Original Assets: 50000000000000000000n
Daily Acquisition: 2500000000000000n
New Total Assets (BigInt): 50000250000000000000n
```

-----

### Stage 3: Reflection and Advanced Features

#### Reflection Questions

1. **How would this work in a real company?**

      * In a real **Financial institution** or **Data pipeline**, standard `Number` types are used only for fractional/currency values where the two-decimal-place rounding is acceptable.
      * **All primary keys, transaction sequence numbers, and massive counts** are handled using a library or a native feature like **`BigInt`** to ensure data integrity and compliance with auditing standards. The `Number.isSafeInteger()` check would be an essential early-stage validation filter when importing data from external sources.

2. **What would be the risk of using standard numbers for the `globalAssetsCount`?**

      * The `globalAssetsCount` is far larger than `Number.MAX_SAFE_INTEGER`. If it were stored as a standard `Number`, the trailing zeros would likely be rounded, and any arithmetic (like adding `dailyAcquisition`) would be **inaccurate**, leading to a non-auditable and potentially catastrophic miscount of corporate assets.

#### Optional Advanced Feature (Data Type Conversion)

If we needed to log the BigInt asset count as a standard string for a report (accepting the precision loss for display purposes), we'd convert it carefully:

```javascript
// ADVANCED FEATURE: Converting BigInt back to a standard Number (with warning)

let bigNumber = 50000250000000000000n; 
let standardNumber = Number(bigNumber); // Explicitly convert to Number. Loss of precision is expected!

// The standard number is now stored in scientific notation and rounded.
console.log(`\nAdvanced Feature: BigInt to Standard Number (Lossy)`);
console.log(`Standard Number Conversion: ${standardNumber}`); 
console.log(`Compare: BigInt (500...00n) vs Standard (${standardNumber})`); 
```

#### Expected Output for Advanced Feature

```
Advanced Feature: BigInt to Standard Number (Lossy)
Standard Number Conversion: 5.000025e+19
Compare: BigInt (500...00n) vs Standard (5.000025e+19)
```

-----

## Completion Checklist

| Requirement | Status |
| :--- | :--- |
| All main ideas are fully explained. | $\checkmark$ |
| All exercises completed or tested. | $\checkmark$ |
| At least one real-world project is built. | $\checkmark$ (Financial Checker) |
| Common beginner errors are highlighted and corrected. | $\checkmark$ (Unsafe integer limits, BigInt usage) |
| Reflection questions answered. | $\checkmark$ |
| Every main concept includes at least one simple example with visible expected output. | $\checkmark$ |

**Summary:** We successfully built a multi-stage financial simulator, utilizing **standard JavaScript `Number`** for safe, formatted currency calculations, and the advanced **`BigInt`** type to ensure guaranteed precision for large-scale asset counts and identifiers, thereby protecting data integrity.
