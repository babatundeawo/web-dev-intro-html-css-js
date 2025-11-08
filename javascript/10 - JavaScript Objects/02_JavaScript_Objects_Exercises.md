# 🚀 **Solutions & Explanations: JavaScript Objects Exercises**

---

## **Exercise 1: Build a Contact Card System**

### **Objective**
Create a reusable `contact` object with properties and methods to manage personal contacts in a **mobile phone app**.

---

### **Solution**

```js
const contact = {
  fullName: "",
  phone: "",
  email: "",
  tags: [],
  isFavorite: false,

  // Returns a favorite label if applicable
  getLabel() {
    return this.isFavorite ? "⭐ Favorite" : "";
  },

  // Adds a tag to the tags array
  addTag(tag) {
    if (typeof tag === "string" && tag.trim() !== "") {
      this.tags.push(tag.trim());
    }
  }
};

// Test the contact
contact.fullName = "Alex Rivera";
contact.phone = "+1-555-0199";
contact.email = "alex.rivera@example.com";
contact.isFavorite = true;
contact.addTag("Work");
contact.addTag("Mobile Dev");

console.log(contact.getLabel() + " " + contact.fullName);
// Output: ⭐ Favorite Alex Rivera

console.log(contact.tags);
// Output: ["Work", "Mobile Dev"]
```

---

### **Step-by-Step Explanation**

| Step | Code | Why It Matters |
|------|------|----------------|
| 1 | `fullName: "", phone: "", ...` | Initialize properties with default empty values for safety |
| 2 | `tags: []` | Array to store multiple tags (e.g., "Friend", "Family") |
| 3 | `getLabel() { return this.isFavorite ? "⭐ Favorite" : ""; }` | **Ternary operator** for clean conditional logic. Uses `this` to access own property |
| 4 | `addTag(tag)` with validation | Prevents invalid tags (`null`, `""`). Uses `trim()` to clean input |
| 5 | `this.tags.push(...)` | Mutates the array **in place** — efficient and expected behavior |

> **Real-World Context**: Apps like **Apple Contacts** or **Google Contacts** use similar structures. Tags help filter: "Show all Work contacts".

---

## **Exercise 2: Dynamic Property Access**

### **Objective**
Write a safe function to get field type from a form config using **dynamic keys**.

---

### **Solution**

```js
const formConfig = {
  "user-name": "text",
  "user-age": "number",
  "user-email": "email"
};

function getFieldType(config, fieldName) {
  return config.hasOwnProperty(fieldName) ? config[fieldName] : "unknown";
}

// Test cases
console.log(getFieldType(formConfig, "user-age"));     // "number"
console.log(getFieldType(formConfig, "user-email"));   // "email"
console.log(getFieldType(formConfig, "user-phone"));   // "unknown"
```

---

### **Step-by-Step Explanation**

| Step | Code | Why It Matters |
|------|------|----------------|
| 1 | `config.hasOwnProperty(fieldName)` | **Safely checks** if key exists. Avoids inherited properties |
| 2 | `config[fieldName]` | **Bracket notation required** — `fieldName` is a variable |
| 3 | Ternary returns value or `"unknown"` | Prevents `undefined` errors in UI |

> **Common Mistake Avoided**:
> ```js
> config[fieldName] // → undefined if missing
> config.fieldName  // → looks for literal "fieldName"
> ```

> **Real-World Use**: Form builders like **Typeform**, **React Hook Form**, or **Airtable** use dynamic keys to map user input to field types.

---

## **Exercise 3: Modify Nested Data**

### **Objective**
Update shopping cart quantities and remove items when `qty <= 0`.

---

### **Solution**

```js
const cart = {
  items: [
    { id: 1, name: "Laptop", price: 999, qty: 1 },
    { id: 2, name: "Mouse", price: 25, qty: 2 }
  ]
};

function updateQuantity(cart, itemId, newQty) {
  const item = cart.items.find(item => item.id === itemId);
  
  if (item) {
    if (newQty <= 0) {
      // Remove item entirely
      cart.items = cart.items.filter(item => item.id !== itemId);
      console.log(`Item ${itemId} removed from cart.`);
    } else {
      item.qty = newQty;
      console.log(`Item ${itemId} quantity updated to ${newQty}.`);
    }
  } else {
    console.log(`Item ${itemId} not found in cart.`);
  }

  return cart;
}

// Test the function
updateQuantity(cart, 2, 3);  // Updates Mouse to qty 3
updateQuantity(cart, 1, 0);  // Removes Laptop
updateQuantity(cart, 99, 5); // Not found

console.log(cart.items);
// Output: [{ id: 2, name: "Mouse", price: 25, qty: 3 }]
```

---

### **Step-by-Step Explanation**

| Step | Code | Why It Matters |
|------|------|----------------|
| 1 | `find()` | Locates item by `id` without looping manually |
| 2 | `newQty <= 0` → `filter()` | **Removes** item completely — clean cart state |
| 3 | `item.qty = newQty` | Direct mutation (allowed since object is `const`, not frozen) |
| 4 | `return cart` | Enables method chaining in real apps |

> **Real-World Context**: **Amazon**, **Shopify**, and **Walmart** carts use similar logic. Removing at `qty === 0` prevents "ghost" items.

---

## ✅ **Mastery Validation**

| Check | Status |
|------|--------|
| All exercises completed | ✅ |
| Dynamic keys used safely | ✅ |
| Nested data mutated correctly | ✅ |
| Real-world patterns applied | ✅ |
| `this`, arrays, and objects used properly | ✅ |

---

## 🌟 **One-Line Takeaway**

> **Master objects by treating them as living data models — mutable, nested, and method-rich — just like real-world entities in apps.**

---

**Next Challenge**: Convert these objects into **ES6 Classes** with `constructor`, `static` methods, and private fields (`#`).

*You're now ready to build professional-grade JavaScript apps!* 🚀