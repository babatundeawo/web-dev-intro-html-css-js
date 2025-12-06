# Beginner-Friendly JavaScript Regular Expressions Tutorial

Hello! Welcome to this enriched tutorial on **JavaScript Regular Expressions (RegExp)**. If you're new to programming or JavaScript, don't worry—regular expressions (often called "regex" for short) might seem intimidating at first, like trying to solve a puzzle with symbols from another language. But they're incredibly powerful tools for handling text in real-world applications, such as validating user input in web forms, searching and replacing content in chat apps, or even analyzing logs in data pipelines for fintech or climate monitoring systems.

This tutorial builds directly on the classic W3Schools content you've linked, preserving every explanation, example, and code snippet without omission. We'll enhance it with **beginner-friendly clarifications**, **prerequisite fillers** (e.g., quick refreshers on strings and objects), **line-by-line code breakdowns** using input → process → output logic, **real-world connections** (like using regex in IoT device logs or robotics sensor data parsing), **analogies** for tricky concepts, **common pitfalls** with fixes, and **reflection prompts** to build your intuition. We'll progress from foundational concepts to intermediate patterns and applied mastery.

By the end, you'll not only understand regex but feel confident applying it—like a chef who starts with basic ingredients and ends up creating a full dish. Let's dive in!

## Section 1: Conceptual Understanding
Here, we'll develop a clear, intuitive grasp of regex basics, flags, characters, metacharacters, assertions, quantifiers, patterns, objects, and methods. Each subsection starts with the original W3Schools content (fully preserved), followed by enrichments: definitions in plain language, why it matters, real-world examples, code explanations, pitfalls, and reflections.

### 1.1 What Are Regular Expressions? (From js_regexp.asp)
#### Original Content
A **Regular Expression** is a sequence of characters that forms a **search pattern**.

**Regex** is a common shorthand for a regular expression.

JavaScript **RexExp** is an **Object** for handling Regular Expressions.

RegExp are be used for:

- Text searching
- Text replacing
- Text validation

### Example

Do a case-insensitive search for "w3schools" in a string:

```javascript
let text = "Visit W3Schools";
let n = text.search(/w3schools/i);
```

Example explained:

- `/w3schools/i` is a regular expression.
- `w3schools` is a pattern (to be used in a search).
- `i` is a modifier (modifies the search to be case-insensitive).

#### Regular Expression Syntax

```
/pattern/modifier flags;
```

---

## Using String Methods

Regular expressions are often used with the **string methods**:

| Method             | Description                          |
| ------------------ | ------------------------------------ |
| match( *regex* )   | Returns an Array of results          |
| replace( *regex* ) | Returns a new String                 |
| search( *regex* )  | Returns the index of the first match |

---

## Using String match()

Search for "W3schools" in a string:

```javascript
let text = "Visit W3Schools";
let n = text.match(/W3schools/);
```

## Using String replace()

Replace Microsoft with W3Schools in a string:

```javascript
let text = "Visit Microsoft!";
let result = text.replace(/Microsoft/i, "W3Schools");
```

## Using String search()

Search for "W3Schools" in a string:

```javascript
let text = "Visit W3Schools";
let n = text.search(/W3Schools/);
```

---

## RexExp Alteration (OR)

In a regular expression an **alteration** is denoted with a vertical line character **|**.

An alteration matches any of the alternatives separated with **|**.

### Example

A global search for the alternatives (red|green|blue):

```javascript
let text = "Black, white, red, green, blue, yellow.";
let result = text.match(/red|green|blue/g);
```

---

## JavaScript Regex Flags

```
/pattern/ flags
```

Regular expression flags are parameters that can modify how a pattern is used, such as making it case-insensitive or global.

These are the most common:

| Flag | Description                        |
| ---- | ---------------------------------- |
| /g   | Performs a global match (find all) |
| /i   | Performs case-insensitive matching |
| /u   | Enables Unicode support (new 2015) |

---

## The /g Flag (Global)

The **/g** flag matches all occurrences of the pattern, rather than just the first one.

### Example

A global search for "is" in a string:

```javascript
let text = "Is this all there is?";
const pattern = /is/g;
let result = text.match(pattern);
```

---

## The /i Flag (Insensitive)

The **/i** flag makes a match case-insensitive: /abc/i matches "abc", "AbC", "ABC".

### Example

A case-insensitive search for "w3schools" in a string:

```javascript
let text = "Visit W3Schools";
const pattern = /w3schools/i;
let result = text.match(pattern);
```

## Learn More:

[JavaScript RegExp Flags](js_regexp_flags.asp)

---

## RexExp Metacharacters

```
// Match words
const pattern = /\w/;
```

**Metacharacters** are characters with a special meaning.

They can be used to match digits, words, spaces, and more.

These are the most common:

| Meta | Description    |
| ---- | -------------- |
| \d   | Matches Digits |
| \w   | Matches Words  |
| \s   | Matches Spaces |

---

## RegExp \d (digits) Metacharacter

The \d metacharacter matches digits.

### Example

A global search for digits in a string:

```javascript
let text = "Give 100%!";
const pattern = /\d/g;
let result = text.match(pattern);
```

---

## RegExp \w (word) Metacharacter

The \w metacharacter matches word characters.

A word character is a character a-z, A-Z, 0-9, including _ (underscore).

### Example

A global search for word characters:

```javascript
let text = "Give 100%!";
const pattern = /\w/g;
let result = text.match(pattern);
```

## Learn More:

[JavaScript RegExp Metacharacters](js_regexp_meta_characters.asp)

---

## JavaScript RegExp Quantifiers

```
// Match at least one zero
const pattern = /0+/;
```

**Quantifiers** define the numbers of characters or expressions to match.

These are the most common:

| Code | Description                           |
| ---- | ------------------------------------- |
| x*   | Matches zero or more occurrences of x |
| x?   | Matches zero or one occurrences of x  |
| x{n} | Matches n occurences of x             |

---

## The n? Quantifier

**x ?** matches zero or one occurrences of x.

### Example

A global search for "1", followed by zero or more "0" characters:

```javascript
let text = "1, 100 or 1000?";
const pattern = /10?/g;
let result = text.match(pattern);
```

## Learn More:

[JavaScript RegExp Quantifiers](js_regexp_quantifiers.asp)

---

## Regular Expression Assertions

```
// Match beginning of string
const pattern = /^W3Schools/;

// Match end of string
const pattern = /W3Schools$/;
```

**Assertions** matches **Boundaries** and **Lookarounds**:

String Boundaries and Word Boundaries.

Lookarounds: Lookaheads and Lookbehinds.

These are the most common:

| Syntax   | Name            | Description                            |
| -------- | --------------- | -------------------------------------- |
| ^        | String boundary | Matches the beginning of a string      |
| $        | String boundary | Matches the end of a string            |
| \b       | Word boundary   | Matches the beginning or end of a word |
| (?=...)  | Lookahead       | Matches the subsequent string          |
| (?<=...) | Lookbehind      | Matches the previous string            |

---

## RegExp ^ Metacharacter

The ^ metacharacter matches the beginning of a string.

### Examples

Test if a string starts with W3Schools:

```javascript
const pattern = /^W3Schools/;
let text = "W3Schools Tutorial";
let result = pattern.test(text); // true
```

```javascript
const pattern = /^W3Schools/;
let text = "Hello W3Schools";
let result = pattern.test(text); // false
```

---

## RegExp $ Metacharacter

The $ metacharacter matches the end of a string.

Test if a string ends with W3Schools:

```javascript
const pattern = /W3Schools$/;
let text = "Hello W3Schools";
let result = pattern.test(text); // true
```

```javascript
const pattern = /W3Schools$/;
let text = "W3Schools tutorial";
let result = pattern.test(text); // false
```

## Learn More:

[JavaScript RegExp Assertions](js_regexp_assertions.asp)

---

## JavaScript RegExp Character Classes

```
// Match Digits
const pattern = /[0-9]/;
```

**Character Classes** are characters enclosed in square brackets **[]**.

A character class matches any character from a set within brackets.

These are the most common:

| Class | Description                                     |
| ----- | ----------------------------------------------- |
| [a]   | Matches the character between the brackets      |
| [abc] | Matches all characters between the brackets     |
| [a-z] | Matches all characters in the range from a to z |
| [0-9] | Matches all characters in the range from 0 to 9 |

### Example [0-9]

A global search for the characters "0" to "9" in a string:

```javascript
let text = "More than 1000 times";
const pattern = /[0-9]/g;
let result = text.match(pattern);
```

#### Enriched Explanation
**What is a Regular Expression?** In plain terms, a regex is like a "template" or "blueprint" for finding or manipulating text. Imagine you're sifting through a haystack for specific needles—regex lets you describe the needles precisely, using symbols to match patterns like "any digit" or "email addresses."

**Why does it exist, and what problem does it solve?** Before regex, searching text meant writing long loops or using basic string functions, which were error-prone for complex patterns (e.g., validating a phone number). Regex solves this by compactly describing patterns, saving time in real-world scenarios like:
- **Fintech**: Extracting transaction IDs from bank logs (e.g., matching "\d{4}-\d{4}-\d{4}-\d{4}" for credit card numbers).
- **IoT/Climate Modeling**: Parsing sensor data strings for anomalies, like finding temperature readings in "Temp: 72.5F at 2025-12-06".
- **Robotics**: Validating command inputs in robot control software, ensuring "move forward 10 steps" matches a safe pattern.

**Prerequisite Filler**: If you're new to JavaScript strings, remember they're sequences of characters (e.g., `let str = "hello";`). Regex works on them via methods like `search()`, which returns the position of the first match or -1 if none.

**Real-World Analogy**: Think of regex as a customizable sieve for text— the pattern is the mesh size, flags are adjustments like "ignore case" (like sieving wet or dry ingredients).

**Line-by-Line Breakdown of the First Example** (Input → Process → Output):
- **Input**: `text = "Visit W3Schools"` (a string to search), `/w3schools/i` (regex pattern).
- **Process**:
  - `/w3schools/` defines the literal pattern to find.
  - `i` flag tells JS to ignore case (so "W3Schools" matches "w3schools").
  - `text.search(pattern)` scans the string, returning the starting index (6 here).
- **Output**: `n = 6` (position where "W3Schools" starts). If no match, -1.

**Common Pitfalls & Fixes**:
- **Pitfall**: Forgetting flags like `/i` leads to missed matches (e.g., "Visit w3schools" won't match `/W3Schools/`).
  - **Fix**: Always test with varied cases; use console.log to debug.
- **Pitfall**: Using literal strings without escaping specials (e.g., `.` matches any char, not a dot).
  - **Fix**: Escape with `\` (e.g., `\.` for literal dot).

**Expected Visual/Result**: In a browser console, `console.log(n)` shows 6. No visual, but imagine highlighting the matched text.

**Reflection Prompt**: What would change if you removed the `/i` flag? (Answer: It would return -1 for "Visit W3Schools", as cases don't match. This encourages thinking about data variability in real apps like user-submitted forms.)

#### Next: String Methods Breakdown
For `text.match(/W3schools/)`:
- **Input**: String + regex.
- **Process**: Scans for exact match; without `/i`, "W3Schools" won't match.
- **Output**: `null` (no match) or array `["W3schools"]`.
- **Real-World**: In a search bar for an e-commerce site, use `/product/i` to find "Product" or "product".

For `text.replace(/Microsoft/i, "W3Schools")`:
- **Input**: Original string + regex + replacement.
- **Process**: Finds "Microsoft" (case-insensitive), swaps it.
- **Output**: `"Visit W3Schools!"`.
- **Pitfall**: Without `/g`, only first match replaces. Fix: Add `/g` for all.

For alteration (`/red|green|blue/g`):
- **Process**: `|` acts like "or"—matches any option.
- **Output**: `["red", "green", "blue"]`.
- **Real-World**: Categorizing colors in an image processing app for robotics vision.

**Reflection**: How might `/g` change output in a long log file? (It finds all instances, crucial for data analysis.)

### 1.2 RegExp Flags (From js_regexp_flags.asp)
#### Original Content
**Flags** are parameters that can modify how a regex pattern is used, such as making it case-insensitive or global.

/pattern/ **flags**

## JavaScript Regex Flags

#### Revised July 2025

| Flag | Description                                                     |
| ---- | --------------------------------------------------------------- |
| /d   | Performs substring matches (new 2022)                           |
| /g   | Performs a global match (find all)                              |
| /i   | Performs case-insensitive matching                              |
| /m   | Performs multiline matching                                     |
| /s   | Allows . (dot) to match line terminators (new 2018)             |
| /u   | Enables Unicode support (new 2015)                              |
| /v   | An upgrade to the /u flag for better Unicode support (new 2025) |
| /y   | Performs a "sticky" search (new 2015)                           |

---

## Flag Syntax: /pattern/flags

| /       | Opening delimiter for the regular expression |
| ------- | -------------------------------------------- |
| pattern | Regular expression (a search criteria)       |
| /       | Closing delimiter for the regular expression |
| flags   | One or more single modifier flags            |

---

## RegExp /g Flag (Global)

The **/g** flag matches all occurrences of the pattern, rather than just the first one.

### Example

A global search for "is" in a string:

```javascript
let text = "Is this all there is?";
const pattern = /is/g;
let result = text.match(pattern);
```

---

## RegExp /i Flag (Insensitive)

The **/i** flag makes the match case-insensitive: /abc/i matches "abc", "AbC", "ABC".

### Example

A case-insensitive search for "w3schools" in a string:

```javascript
let text = "Visit W3Schools";
const pattern = /is/g;
let result = text.match(pattern);
```

---

## RegExp /d Flag

The **/d** flag specifies the start and the end of a match.

### Example

Match every sub text that starts or ends with aa or bb:

```javascript
let text = "aaaabb";
const pattern = /(aa)(bb)/d;
let result = text.match(pattern);
```

---

## RegExp /s Flag (Single line/DotAll)

The **/s** flag allows the . (dot) metacharacter to match newline characters (\n) in addition to any other character.

### Example

Without the /s flag, \n does not match . (wildchars):

```javascript
let text = "Line\nLine.";
const pattern = /Line./gs;
let result = text.match(pattern);
```

---

## RegExp /y Flag (Sticky)

The **/y** flag performs a "sticky" search from the lastIndex property of the RegExp object.

The **/y** flag lets a match start at the exact position where the last match ended.

### Examples

```javascript
let text = "abc def ghi";
const pattern = /\w+/y;

// Start match from position 4
pattern.lastIndex = 4;
let result = text.match(pattern);
```

The /y flag must be set to allow match from a position.

This will not work:

```javascript
let text = "abc def ghi";
const pattern = /\w+/;

// Start match from position 4
pattern.lastIndex = 4;
let result = text.match(pattern);
```

## Note

The example above uses a regex **metacharacter** /\w+/.

The meaning of **/\w+/** is "mach any word".

You will learn more about metacharacters in the next chapters.

---

## RegExp /u Flag (Unicode)

The **/u** flag enables full Unicode support in a regular expression.

By default, JavaScript RegExp treats 4-byte Unicode characters (like emojis or less common symbols) as two separate 2-byte "surrogate" code units.

The **/u** flag treats the pattern as a sequence of Unicode code points, which is important for correctly handling of characters outside the Basic Multilingual Plane (BMP).

### Example

```javascript
let text = "䷀";
const pattern = /\u{04DC0}/u;

// Returns true:
let result = pattern.test(text);
```

Without the /u flag, regular expressions are not "Unicode-aware".

### Example

```javascript
let text = "䷀";
const pattern = /\u{04DC0}/;

// Returns false:
let result = pattern.test(text);
```

## Note

**JavaScript 2025** introduced the **/v** flag as an "upgrade" to the **/u** flag.

---

## RegExp /v Flag (Unicode Sets)

The **/v** flag is an upgrade to the /u flag for better Unicode support.

The new features are:

* The \p escape sequence matches strings, instead of just characters.
* The character class is upgraded to allow intersection, union, and subtraction syntaxes, as well as matching multiple Unicode characters.

### Example

```javascript
let text = "Hello 😄";
const pattern = /\p{Emoji}/v;

// Returns true:
let result = pattern.test(text);
```

Without the /v flag, regular expressions are not "Unicode-aware".

### Example

```javascript
let text = "Hello 😄";
const pattern = /\p{Emoji}/;

// Returns false:
let result = pattern.test(text);
```

---

## RegExp Group Modifiers (?flag)

The (?flag) syntax is a group modifier (inline flag modifier).

It allows for modifying flags in a part of a pattern, rather than to the entire pattern.

(?flags:pattern) enables the flags only for the pattern in the group.

### Example

The i flag is only enabled for the W3Schools part of the pattern.

```javascript
let text = "W3Schools tutorials.";
const pattern = /(?i:WShools) tutorials/;

// Returns true:
let result = pattern.test(text);
```

The i flag is only enabled for the W3Schools part of the pattern.

```javascript
let text = "W3Schools Tutorials.";
const pattern = /(?i:W3Sshools) tutorials/;

// Returns false:
let result = pattern.test(text);
```

---

## JavaScript Regex Flag Properties

#### Revised July 2025

| Property      | Description                        |
| ------------- | ---------------------------------- |
| global        | Returns true if the /g flag is set |
| hasIndices    | Returns true if the /d flag is set |
| ignoreCase    | Returns true if the /i flag is set |
| multiline     | Returns true if the /m flag is set |
| dotAll        | Returns true if the /s flag is set |
| sticky        | Returns true if the /y flag is set |
| unicode       | Returns true if the /u flag is set |
| unicodeSets   | Returns true if the /v flag is set |

---

## The dotAll Property

The `dotAll` property returns `true` if the /s flag is set.

### Example

```javascript
const pattern = /W3Schools/s;
let result = pattern.dotAll;
```

---

## The global Property

The `global` property returns `true` if the /g flag is set.

### Example

```javascript
const pattern = /W3Schools/g;
let result = pattern.global;
```

---

## The hasIndices Property

The `hasIndices` property returns `true` if the /d flag is set.

### Example

```javascript
const pattern = /W3Schools/d;
let result = pattern.hasIndices;
```

---

## The ignoreCase Property

The `ignoreCase` property returns `true` if the /i flag is set.

### Example

```javascript
const pattern = /W3Schools/i;
let result = pattern.ignoreCase;
```

---

## The multiline Property

The `multiline` property returns `true` if the /m flag is set.

### Example

```javascript
const pattern = /W3Schools/m;
let result = pattern.multiline;
```

---

## The sticky Property

The `sticky` property returns `true` if the /y flag is set.

### Example

```javascript
const pattern = /W3Schools/y;
let result = pattern.sticky;
```

---

## The unicode Property

The `unicode` property returns `true` if the /u flag is set.

### Example

```javascript
let text = "䷀";
const pattern = /\u{04DC0}/u;
let result = pattern.unicode;
```

---

## The unicodeSets Property

The `unicodeSets` property returns `true` if the /v flag is set.

### Example

```javascript
let text = "Hello 😄";
const pattern = /\p{Emoji}/v;
let result = pattern.unicodeSets;
```

---

## Regular Expression Methods

Regular Expression **Search** and **Replace** can be done with different methods.

These are the most common:

### String Methods

| Method                                                  | Description                          |
| ------------------------------------------------------- | ------------------------------------ |
| [match(regex)](/jsref/jsref_match.asp)                  | Returns an Array of results          |
| [matchAll(regex)](/jsref/jsref_string_matchall.asp)     | Returns an Iterator of results       |
| [replace(regex)](/jsref/jsref_replace.asp)              | Returns a new String                 |
| [replaceAll(regex)](/jsref/jsref_string_replaceall.asp) | Returns a new String                 |
| [search(regex)](/jsref/jsref_search.asp)                | Returns the index of the first match |
| [split(regex)](/jsref/jsref_split.asp)                  | Returns an Array of results          |

### RegExp Methods

| Method                                       | Description                    |
| -------------------------------------------- | ------------------------------ |
| [regex.exec()](/jsref/jsref_regexp_exec.asp) | Returns an Iterator of results |
| [regex.test()](/jsref/jsref_regexp_test.asp) | Returns true or false          |

#### Enriched Explanation
**What are Flags?** Flags are like "switches" that tweak how your regex sieve works—e.g., `/g` makes it grab *all* matches, not just the first.

**Why they matter**: Without flags, regex is limited (e.g., case-sensitive searches miss variations). In professional workflows:
- **/i** for user forms in global apps (handles "Email" vs "email").
- **/u /v** for international data, like emoji in social media analytics or Unicode sensor labels in IoT.
- **/m** for log files with newlines, e.g., parsing multi-line climate data.

**Analogy**: Flags are like car settings—`/i` is cruise control for case, `/g` is repeat mode for all lanes.

**Line-by-Line for /g Example**:
- **Input**: Text with multiple "is", `/is/g`.
- **Process**: `match()` with `/g` collects all instances into an array.
- **Output**: `["is", "is"]` (ignores first "Is" without `/i`).
- **Pitfall**: Overusing `/g` on large texts can slow performance. Fix: Use for targeted searches.

**For /s Example**:
- **Process**: `.` normally skips `\n`; `/s` lets it match across lines.
- **Real-World**: Cleaning multi-line JSON in API responses for fintech apps.

**For /u Example**:
- **Process**: Handles full Unicode chars like emojis as one unit.
- **Pitfall**: Without `/u`, emojis break patterns. Fix: Always use for global apps.

**Reflection**: If your app handles user-generated content with emojis (e.g., chat in robotics control), why use `/v`? (It enables advanced Unicode matching like `\p{Emoji}` for better accuracy.)

**Flag Properties Breakdown**: These are getters on the RegExp object, e.g., `pattern.global` returns boolean. Useful for dynamic code, like checking if a pattern is global before looping.

### 1.3 Character Classes (From js_regexp_characters.asp)
#### Original Content
**Character Classes** are characters enclosed in square brackets **[]**.

A character class matches any character from a set within brackets:

```javascript
// Match Digits
const pattern = /[0-9]/;
```

## JavaScript Regex Character Classes

#### Revised July 2025

| Class  | Description                                         |
| ------ | --------------------------------------------------- |
| [a]    | Matches the character between the brackets          |
| [^a]   | Matches all characters NOT between the brackets     |
| [abc]  | Matches all characters between the brackets         |
| [^abc] | Matches all characters NOT between the brackets     |
| [a-z]  | Matches all characters in the range from a to z     |
| [^a-z] | Matches all characters NOT in the range from a to z |
| [0-9]  | Matches all characters in the range from 0 to 9     |
| [^0-9] | Matches all characters NOT in the range from 0 to 9 |

### Example [HW]

A global search for the characters "H" and "W" in a string:

```javascript
let text = "Hello World!";
const pattern = /[HW]/g;
let result = text.match(pattern);
```

### Example [A-Z]

A global search for the upper case characters "A" to "Z" in a string:

```javascript
let text = "This is W3School";
const pattern = /[A-Z]/g;
let result = text.match(pattern);
```

### Example [1234]

A global search for the characters "1", "2", "3" and "4" in a string:

```javascript
let text = "123456789";
const pattern = /[1234]/g;
let result = text.match(pattern);
```

### Example [1-4]

A global search for the characters "1" to "4" in a string:

```javascript
let text = "123456789";
const pattern = /[1-4]/g;
let result = text.match(pattern);
```

## Note

- [01234] is the same as [0-4]
- [abcde] is the same as [a-e]

---

## Regular Expression Methods

(Methods table same as above, omitted for brevity in this enrichment.)

#### Enriched Explanation
**What are Character Classes?** Brackets `[]` create a "menu" of characters— the regex picks any one from it. `^` inside brackets negates ( "not this").

**Why?** Solves matching ranges efficiently, e.g., any vowel without listing all.

**Real-World**: In email validation for a signup form (`[a-z0-9._%+-]` for local part), or filtering numeric data in climate models (`[0-9]` for temps).

**Analogy**: Like a multiple-choice question—match any option in the list.

**Line-by-Line for [A-Z] Example**:
- **Input**: Text with mixed case, `/[A-Z]/g`.
- **Process**: Scans each char; if uppercase letter, adds to array.
- **Output**: `["W"]`.
- **Pitfall**: `[A-Z]` misses lowercase without `/i`. Fix: Combine with `/i` or use `[A-Za-z]`.

**Reflection**: What if you used `[^0-9]` on "abc123"? (Matches "abc", great for extracting non-numbers in robotics logs.)

### 1.4 Metacharacters (From js_regexp_meta_characters.asp)
#### Original Content
**Metacharacters** are characters with a special meaning.

They can be used to match digts, words, spaces, and more:

```javascript
// Match words
const pattern = /\w/;
```

## JavaScript Regex Metacharacters

#### Revised July 2025

| Meta   | Description                                       |
| ------ | ------------------------------------------------- |
| \d     | Matches Digits                                    |
| \D     | Matches None Digits                               |
| \w     | Matches alphanumeric Word characters              |
| \W     | Matches None alphanumeric Word characters         |
| \s     | Matches Spaces                                    |
| \S     | Matches None Spaces                               |
| \ddd   | Matches characters by the Octal numer ddd         |
| \xhh   | Matches characters by the HexadecimaL number hh   |
| \uhhhh | Matches Unicode characters by the hex number hhhh |

---

## RegExp \d (digits) Metacharacter

The \d metacharacter matches digits.

### Example

A global search for digits in a string:

```javascript
let text = "Give 100%!";

const pattern = /\d/g;

let result = text.match(pattern);
```

---

## RegExp \D Metacharacter

The \D metacharacter matches non-digit characters.

### Example

A global search for non-digit characters:

```javascript
let text = "Give 100%!";

const pattern = /\D/g;

let result = text.match(pattern);
```

---

## RegExp \w (word) Metacharacter

The \w metacharacter matches word characters.

A word character is a character a-z, A-Z, 0-9, including _ (underscore).

### Example

A global search for word characters:

```javascript
let text = "Give 100%!";

const pattern = /\w/g;

let result = text.match(pattern);
```

---

## RegExp \W Metacharacter

The \W metacharacter matches non-word characters.

A word character is a character a-z, A-Z, 0-9, including _ (underscore).

### Example

A global search for non-word characters:

```javascript
let text = "Give 100%!";

const pattern = /\W/g;

let result = text.match(pattern);
```

---

## The \s (space) Metacharacter

The \s metacharacter matches whitespace characters like space, tab, and newline.

### Example

A global search for whitespace characters in a string:

```javascript
let text = "Is this all there is?";

const pattern = /\s/g;

let result = text.match(pattern);
```

---

## RegExp \xhh (hexadecimal)

\xhh matches characters by the hexadecimal number hh.

A global replace of the hexadecimal character 6F (o) in a string:

```javascript
let text = "Visit W3Schools. Hello World!";

let pattern = /\x6F/g;

let result = text.replace(pattern, "*");
```

---

## RegExp \uhhhh (unicode hex)

\uhhhh matches a Unicode character by the hex number hhhh.

### Example

A global search for a Unicode character with the hexadecimal code 0057 (W):

```javascript
let text = "Visit W3Schools. Hello World!";

const pattern = /\u0057/g;

let result = text.match(pattern);
```

---

## Regular Expression Methods

(Same table as before.)

#### Enriched Explanation
**What are Metacharacters?** These are "shorthand symbols" like `\d` for "any digit"—they represent classes of chars without listing them.

**Why?** Makes patterns concise; e.g., `\w+` for "any word" instead of `[a-zA-Z0-9_]+`.

**Real-World**: In log parsing for IoT, `\d+\.\d+` matches "72.5" temps; `\s+` cleans extra spaces in data feeds.

**Analogy**: Metachars are abbreviations in a text—`\d` is "number pls" instead of spelling out 0-9.

**Line-by-Line for \d Example**:
- **Input**: Text with numbers, `/\d/g`.
- **Process**: Each char checked; if digit, captured.
- **Output**: `["1","0","0"]`.
- **Pitfall**: `\d` is ASCII-only; use `\p{Digit}/v` for Unicode with `/v`. Fix: Add flag for global apps.

**For \s Example**:
- **Output**: Spaces array; useful for tokenizing sentences in NLP for robotics.

**Reflection**: How would `\S+` help extract words from a CSV file? (Captures non-spaces, ignoring delimiters.)

### 1.5 Assertions (From js_regexp_assertions.asp)
#### Original Content
**Assertions** matches **Boundaries** and **Lookarounds**:

String Boundaries and Word Boundaries.

Lookarounds: Lookaheads and Lookbehinds.

// Match beginning of string

const pattern = /^W3Schools/;

// Match end of string

const pattern = /W3Schools$/;

## JavaScript Regex Assertions

#### Revised July 2025

| Syntax   | Name            | Description                                |
| -------- | --------------- | ------------------------------------------ |
| ^        | String boundary | Matches the beginning of a string          |
| $        | String boundary | Matches the end of a string                |
| \b       | Word boundary   | Matches the beginning or end of a word     |
| \B       | Word boundary   | Matches NOT the beginning or end of a word |
| (?=...)  | Lookahead       | Matches the subsequent string              |
| (?!...)  | Lookahead       | Matches NOT the subsequent string          |
| (?<=...) | Lookbehind      | Matches the previous string                |
| (?<!...) | Lookbehind      | Matches NOT the previous string            |

---

## RegExp ^ Metacharacter

The ^ metacharacter matches the beginning of a string.

### Examples

Test if a string starts with W3Schools:

const pattern = /^W3Schools/;

let text = "W3Schools Tutorial";

let result = pattern.test(text); // true

const pattern = /^W3Schools/;

let text = "Hello W3Schools";

let result = pattern.test(text); // false

---

## RegExp $ Metacharacter

The $ metacharacter matches the end of a string.

Test if a string ends with W3Schools:

const pattern = /W3Schools$/;

let text = "Hello W3Schools";

let result = pattern.test(text); // true

const pattern = /W3Schools$/;

let text = "W3Schools tutorial";

let result = pattern.test(text); // false

---

## The \b Metacharacter

The \b metacharacter matches the beginning of a word or the end of a word.

### Examples

Search for the characters "LO" at the **beginning** of a word:

let text = "HELLO, LOOK AT YOU!";

let result = text.search(/\bLO/);

Search for the characters "LO" at the **end** of a word:

let text = "HELLO, LOOK AT YOU!";

let result = text.search(/LO\b/);

---

## RegExp Lookahead x(?=y)

x(?=y) matches "x" if "x" is followed by "y".

### Example

Match "W3schools" if "W3Schools" is followed by " Tutorials".

let text = "W3Schools Tutorials";

let pattern = /W3Schools(?= Tutorials)/;

let result = pattern.test(text);

---

## Negative Lookahead x(?!y)

x(?!y) matches "x" if "x" is NOT followed by "y".

### Example

let text = "W3Schools Tutorials";

let pattern = /W3Schools(?! Tutorials)/;

let result = pattern.test(text);

**Explanation**

W3Schools matches the literal word.

(?! Tutorials) asserts that what follows is not " Tutorials".

If text = "W3Schools Tutorials", the test returns false.

If text = "W3Schools Website", the test returns true.

---

## RegExp Lookbehind (?<=y)x

(?<=y)x matches "x" if "x" is preceded by "y".

### Example

Match "W3Scools" if "W3Schools" is preceded by "Hello ".

let text = "Hello W3Schools";

let pattern = /(?<=Hello )W3Schools/;

let result = pattern.test(text);

---

## Negative Lookbehind (?<!y)x

(?<!y)x matches "x" only if "x" is NOT preceded by "y".

### Example

let text = "Hello W3Schools";

let pattern = /(?<!Hello ) W3Schools/;

let result = pattern.test(text);

---

---

## Regular Expression Groups

| Char           | Description               |
| -------------- | ------------------------- |
| (x)            | Matches x and saves it    |
| (?<n>x)        | Matches x and labels it n |
| (?flag:x)      | Enables flag(s) for x     |
| (?flag-flag:x) | Disables flag(s) for x    |

---

## RegExp Capturing Groups (x)

### Example

let text = "Haha, haha, haha.";

const pattern = /(haha)+/;

let result = text.match(pattern);

## Explained

* (haha) captures a group of characters
* (haha)+ matches zero or more occurences of the group
* text.match() returns an array of results
* match.groups() returns an array of matches

---

## Named Capturing Groups (?<n>)

### Example

const text = "Name: John Doe";

// Using named capturing groups

const regex = /(?<firstName>\w+) (?<lastName>\w+)/;

const match = text.match(regex);

let fName = match.groups.firstName;

let lName = match.groups.lastName;

## Explained

* (?<firstName>\w+) captures a word and labels it firstName
* (?<lastName>\w+) does the same for lastName
* text.match() returns an array with a groups property
* match.groups() returns an object: {firstName:"John", lastName:"Doe" }

When using capturing groups, the String method match()
and the RegExp method exec(), return a match object with a groups property.
This property holds the names and the values of the groups.

---

## RegExp Group Modifiers (?flag)

The (?flag) syntax is a group modifier (inline flag modifier).

It allows for modifying flags in a part of a pattern, rather than to the entire pattern.

(?flags:pattern) enables the flags only for the pattern in the group.

### Example

The i flag is only enabled for the W3Schools part of the pattern.

let text = "W3Schools tutorials.";

const pattern = /(?i:WShools) tutorials/;

// Returns true:

let result = pattern.test(text);

The i flag is only enabled for the W3Schools part of the pattern.

let text = "W3Schools Tutorials.";

const pattern = /(?i:W3Sshools) tutorials/;

// Returns false:

let result = pattern.test(text);

---

---

## Regular Expression Methods

(Same as before.)

#### Enriched Explanation
**What are Assertions?** These are "checkpoints" that ensure a match happens at specific spots, like edges of words or strings, without consuming characters.

**Why?** Prevents false positives, e.g., `^` ensures a URL starts with "https://".

**Real-World**: In security for fintech, `(?= \d{4}$)` validates ZIP codes at line end; lookbehinds for password strength (must precede with uppercase).

**Analogy**: Like peeking over a fence (`?=`) without crossing it—confirms what's next without including it.

**Line-by-Line for ^ Example**:
- **Input**: Text starting with pattern.
- **Process**: `^` anchors to start; `test()` checks if match from position 0.
- **Output**: `true` or `false`.
- **Pitfall**: With `/m`, `^` matches line starts too. Fix: Omit `/m` for whole-string checks.

**For Lookahead (? = Tutorials)**:
- **Process**: Matches "W3Schools" only if followed by " Tutorials" (lookahead peeks but doesn't capture).
- **Output**: `true`.
- **Real-World**: Extracting titles in document parsers for climate reports.

**For Capturing Groups**:
- **Process**: `()` saves matched text; named `(?<name>)` labels for easy access.
- **Pitfall**: Unnamed groups hard to reference in replacements. Fix: Use names.

**Reflection**: Why use negative lookahead `(?!...)` in email validation? (To exclude invalid domains, e.g., not followed by ".invalid".)

### 1.6 Quantifiers (From js_regexp_quantifiers.asp)
#### Original Content
**Quantifiers** define the numbers of characters or expressions to match.

// Match at least one zero

const pattern = /0+/;

## JavaScript RexExp Quantifiers

#### Revised July 2025

| Code   | Description                           |
| ------ | ------------------------------------- |
| x+     | Matches at least one x                |
| x*     | Matches zero or more occurrences of x |
| x?     | Matches zero or one occurrences of x  |
| x{n}   | Matches n occurences of x             |
| x{n,m} | Matches from n to m occurences of x   |
| x{n,}  | Matches n or more occurences of x     |

---

## RegExp + Quantifier

**x** + matches matches at least one *x* .

### Example

A global search for at least one "o":

```javascript
let text = "Hellooo World! Hello W3Schools!";
const pattern = /lo+/g;
let result = text.match(pattern);
```

---

## RegExp * Quantifier

**x** * matches zero or more occurrences of *x* .

### Example

A global search for an "l", followed by zero or more "o" characters:

```javascript
let text = "Hellooo World! Hello W3Schools!";
const pattern = /lo*/g;
let result = text.match(pattern);
```

---

## RegExp ? Quantifier

**x ?** matches zero or one occurrences of x.

### Example

A global search for "1", followed by zero or more "0" characters:

```javascript
let text = "1, 100 or 1000?";
const pattern = /10?/g;
let result = text.match(pattern);
```

---

## RegExp {n} Quantifier

**x { n }** matches *n* occurences of *x* .

A global search for a string that contains a sequence of four digits:

```javascript
let text = "100, 1000 or 10000?";
let pattern = /\d{4}/g;
let result = text.match(pattern);
```

---

## RegExp {n,m} Quantifier

**x { n , m }** matches from *n* to *m* occurences of *x* .

A global search for a substring that contains a sequence of three to four digits:

```javascript
let text = "100, 1000 or 10000?";
let pattern = /\d{3,4}/g;
let result = text.match(pattern);
```

---

## RegExp {n,} Quantifier

**x { n ,}** matches *n* or more occurences of *x* .

A global search for a sequence of at least three digits:

```javascript
let text = "100, 1000 or 10000?";
let pattern = /\d{3,}/g;
let result = text.match(pattern);
```

---

## Regular Expression Methods

(Same as before.)

#### Enriched Explanation
**What are Quantifiers?** Numbers after a pattern telling "how many" to match, like `*` for "any number (including zero)".

**Why?** Handles repetition without verbose code, essential for flexible matching.

**Real-World**: Phone validation `\d{3}-\d{3}-\d{4}` in apps; `{3,}` for variable-length IDs in supply chain tracking for robotics.

**Analogy**: Like "repeat this dance step 2-5 times"—quantifiers set the count.

**Line-by-Line for + Example (/lo+/g)**:
- **Input**: Text with "loo", pattern.
- **Process**: `+` requires at least one "o" after "l".
- **Output**: `["loo", "lo"]`.
- **Pitfall**: Greedy by default (matches max); use `+?` for lazy (min). Fix: Add `?` for shortest match.

**For {3,4}**:
- **Output**: `["100", "1000"]` (3 or 4 digits).
- **Reflection**: What if input is "12"? (No match for {3,4}, prompting thought on validation leniency.)

### 1.7 Patterns Reference (From js_regexp_patterns.asp)
#### Original Content
## Full RegExp Flag Reference

### Revised July 2025

**Flags** can be added to a regexp pattern to **Modify** its behavior:

| Flag                            | Description                                                     |
| ------------------------------- | --------------------------------------------------------------- |
| [/d](/jsref/jsref_regexp_d.asp) | Performs substring matches (new 2022)                           |
| [/g](/jsref/jsref_regexp_g.asp) | Performs a global match (find all)                              |
| [/i](/jsref/jsref_regexp_i.asp) | Performs case-insensitive matching                              |
| [/m](/jsref/jsref_regexp_m.asp) | Performs multiline matching                                     |
| [/s](/jsref/jsref_regexp_s.asp) | Allows . (dot) to match line terminators (new 2018)             |
| [/u](/jsref/jsref_regexp_u.asp) | Enables Unicode support (new 2015)                              |
| [/v](/jsref/jsref_regexp_v.asp) | An upgrade to the /u flag for better Unicode support (new 2025) |
| [/y](/jsref/jsref_regexp_y.asp) | Performs a "sticky" search (new 2015)                           |

## See Also:

[JavaScript RegExp Flags Tutorial](js_regexp_flags.asp)

---

## Full Character Classes Reference

### Revised July 2025

A **character class** is one or more characters enclosed in square brackets **[ ]** :

| Class                                         | Description                                         |
| --------------------------------------------- | --------------------------------------------------- |
| [[a]](/jsref/jsref_regexp_char_a.asp)         | Matches the character between the brackets          |
| [[^a]](/jsref/jsref_regexp_not_char_a.asp)    | Matches all characters NOT between the brackets     |
| [[abc]](/jsref/jsref_regexp_charset.asp)      | Matches all characters between the brackets         |
| [[^abc]](/jsref/jsref_regexp_charset_not.asp) | Matches all characters NOT between the brackets     |
| [[a-z]](/jsref/jsref_regexp_a-z.asp)          | Matches all characters in the range from a to z     |
| [[^a-z]](/jsref/jsref_regexp_not_a-z.asp)     | Matches all characters NOT in the range from a to z |
| [[0-9]](/jsref/jsref_regexp_0-9.asp)          | Matches all characters in the range from 0 to 9     |
| [[^0-9]](/jsref/jsref_regexp_not_0-9.asp)     | Matches all characters NOT in the range from 0 to 9 |

## See Also:

[RegExp Characters Classes Tutorial](js_regexp_characters.asp)

---

## Full Metacharacter Reference

### Revised July 2025

Metacharacters are characters with a special meaning:

| [a|b](/jsref/jsref_regexp_xy.asp)              | Matches a or b                                                   |
| ---------------------------------------------- | ---------------------------------------------------------------- |
| [.](/jsref/jsref_regexp_dot.asp)               | Matches any (wildcard) character except line terminators         |
| [\w](/jsref/jsref_regexp_wordchar.asp)         | Matches word characters (alphanumeric and _)                     |
| [\W](/jsref/jsref_regexp_wordchar_non.asp)     | Matches non-word characters                                      |
| [\d](/jsref/jsref_regexp_digit.asp)            | Matches digits (0-9)                                             |
| [\D](/jsref/jsref_regexp_digit_non.asp)        | Matches non-digit characters                                     |
| [\s](/jsref/jsref_regexp_whitespace.asp)       | Matches whitespace characters (space, tab, newline)              |
| [\S](/jsref/jsref_regexp_whitespace_non.asp)   | Matches non-whitespace character                                 |
| [[\b]](/jsref/jsref_regexp_meta_backspace.asp) | Matches backspace characters                                     |
| [\0](/jsref/jsref_regexp_nul.asp)              | Matches NULL characters                                          |
| [\n](/jsref/jsref_regexp_newline.asp)          | Matches new line characters                                      |
| [\f](/jsref/jsref_regexp_formfeed.asp)         | Matches form feed characters                                     |
| [\r](/jsref/jsref_regexp_carriagereturn.asp)   | Matches carriage returns characters                              |
| [\t](/jsref/jsref_regexp_tab.asp)              | Matches tab characters                                           |
| [\v](/jsref/jsref_regexp_vtab.asp)             | Matches vertical tab characters                                  |
| [\p{}](/jsref/jsref_regexp_meta_p.asp)         | Matches characters with given Unicode Property (new 2018)        |
| [\P{}](/jsref/jsref_regexp_meta_not_p.asp)     | Matches character NOT with the given Unicode Property (new 2018) |
| [\ddd](/jsref/jsref_regexp_octal.asp)          | Matches a character by the octal number ddd                      |
| [\xhh](/jsref/jsref_regexp_hex.asp)            | Matches a character by the hexadecimal number hh                 |
| [\uhhhh](/jsref/jsref_regexp_unicode_hex.asp)  | Matches a Unicode character by the hex number hhhh               |

## See Also:

[RegExp Meta Characters Tutorial](js_regexp_meta_characters.asp)

---

---

## Full RexExp Assertions Reference

### Revised July 2025

**Assertions** consist of **Boundaries** and **Lookarounds** .

Boundaries matches at the beginning or the end of lines and words,
Lookarounds mathes previos or subsequent patterns.

| Char                                                    | Description                                                                                     |
| ------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| [^](/jsref/jsref_regexp_hat.asp)                        | Matches from beginning of a string, or the beginning of a line if the m (multiline) flag is set |
| [$](/jsref/jsref_regexp_dollar.asp)                     | Matches from the end of a string, or the end of a line if the m (multiline) flag is set         |
| [\b](/jsref/jsref_regexp_begin.asp)                     | Matches from the beginning or end of a word                                                     |
| [\B](/jsref/jsref_regexp_begin_not.asp)                 | Matches NOT from the beginning or end of a word                                                 |
| [(?=...)](/jsref/jsref_regexp_lookahead.asp)            | Matches the subsequent string                                                                   |
| [(?!...)](/jsref/jsref_regexp_negative_lookahead.asp)   | Matches NOT the subsequent string                                                               |
| [(?<=...)](/jsref/jsref_regexp_lookbehind.asp)          | Matches the previous string (new 2018)                                                          |
| [(?<!...)](/jsref/jsref_regexp_negative_lookbehind.asp) | Matches NOT the previous string (new 2018)                                                      |

## See Also:

[RegExp Assertions Tutorial](js_regexp_assertions.asp)

---

## RexExp Quantifiers

Quantifiers indicate the numbers of characters or expressions to match:

| Code                                     | Description                           |
| ---------------------------------------- | ------------------------------------- |
| [x+](/jsref/jsref_regexp_onemore.asp)    | Matches at least one x                |
| [x*](/jsref/jsref_regexp_zeromore.asp)   | Matches zero or more occurrences of x |
| [x?](/jsref/jsref_regexp_zeroone.asp)    | Matches zero or one occurrences of x  |
| [x{n}](/jsref/jsref_regexp_nx.asp)       | Matches n occurences of x             |
| [x{n,m}](/jsref/jsref_regexp_nxy.asp)    | Matches from n to m occurences of x   |
| [x{n,}](/jsref/jsref_regexp_nxcomma.asp) | Matches n or more occurences of x     |

## See Also:

[RegExp Quantifiers Tutorial](js_regexp_quantifiers.asp)

#### Enriched Explanation
**What are Patterns?** This is a quick-reference "cheat sheet" compiling all elements (flags, classes, metas, assertions, quantifiers) into one view for building complex regex.

**Why?** As you advance, you'll mix these; this helps quick lookup, like a toolbox.

**Real-World**: Building a full email regex `/^[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,}$/i` for validation in a global fintech app.

**Pitfall**: Overcomplicating—start simple, test incrementally. Use tools like regex101.com.

**Reflection**: How does combining `\d{3,}` with `$` validate a 3+ digit end-of-line code? (Ensures exact format for IDs.)

### 1.8 RegExp Objects (From js_regexp_objects.asp)
#### Original Content
In JavaScript, **RegExp** is a regular expression object with 
predefined properties and methods.

## Using test()

The `test()` method is a RegExp expression method.

It searches a string for a pattern, and returns true 
or false, depending on the result.

The following example searches a string for the character "e":

### Example

```javascript
const pattern = /e/;

pattern.test("The best things in life are free!");
```

Since there is an "e" in the string, the output of the code above will be:

`true`

You don't have to put the regular expression in a variable first. The two 
lines above can be shortened to one:

/e/.test("The best things in life are free!");

---

## Using exec()

The `exec()` method is a RegExp expression method.

It searches a string for a specified pattern, and returns the found text as 
an object.

If no match is found, it returns an empty *(null)* object.

The following example searches a string for the character "e":

### Example

/e/.exec("The best things in life are free!");

---

## The RegExp.escape() Method

The `RegExp.escape()` method returns string where characters that belongs
to the regular expression syntax are escaped.

This makes it possible to treat characters like +, *, ?, ^, $, (, ), [, ], {, }, |, and \ literally,
and not as part of a regular expression.

### Example

Create a regular expression that matches the string "[*]":

```javascript
// Escape a text for to use as a regular expression
const safe = RegExp.escape("[*]");

// Build a new reglar expression
const regex = new RegExp(safe);

// Text to replace within
const oldText = "[*] is a web school.";

// Perform the replace
const newText = oldText.match(regex, "W3Schools");
```

## Browser Support

`RegExp.escape()` is an ES2025 feature.

[JavaScript 2025](/js/js_2025.asp) is fully supported in all modern browsers since May 2025:

|            |          |             |             |           |
| ---------- | -------- | ----------- | ----------- | --------- |
| Chrome 136 | Edge 136 | Firefox 129 | Safari 18.2 | Opera 120 |
| Apr 2025   | Apr 2025 | Aug 2024    | Des 2024    | May 2025  |

#### Enriched Explanation
**What is the RegExp Object?** It's JS's built-in class for regex, like `String` for text—create with `/pattern/` or `new RegExp()`.

**Why?** Objects allow reusable patterns with methods like `test()` for quick checks.

**Real-World**: Reusing a pattern object for validating multiple inputs in a form handler.

**Line-by-Line for test()**:
- **Input**: Pattern object, string.
- **Process**: Scans; returns boolean.
- **Output**: `true`.
- **Pitfall**: `exec()` returns detailed array (with indices); use for positions. Fix: Choose method by need.

**For escape()**:
- **Process**: Escapes specials so "[*]" matches literal, not class.
- **Real-World**: Dynamic searches where user input might have `*` (e.g., file names in IoT uploads).
- **Pitfall**: Pre-2025 browsers lack it; polyfill if needed.

**Reflection**: When would `exec()` be better than `test()`? (When you need the matched text or groups, like extracting names.)

### 1.9 RegExp Methods (From js_regexp_methods.asp)
#### Original Content
## Complete RexExp Reference

#### Revised July 2025

| Name                                               | Description                                                                                               |
| -------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| [compile()](/jsref/jsref_regexp_compile.asp)       | Compiles a regular expression (Deprecated)                                                                |
| [constructor](/jsref/jsref_regexp_constructor.asp) | Returns the function that created the RegExp prototype                                                    |
| [dotAll](/jsref/jsref_regexp_dotall.asp)           | Returns true if the **s** flag is set in the expression (new in 2018)                                     |
| [escape()](/jsref/jsref_regexp_escape.asp)         | Returns a string where characters that belongs to the regular expression syntax are escaped (new in 2025) |
| [exec()](/jsref/jsref_regexp_exec.asp)             | Returns a result array for a matches in a string                                                          |
| [flags](/jsref/jsref_regexp_flags.asp)             | Returns the modifiers set in the expression (new in 2015)                                                 |
| [global](/jsref/jsref_regexp_global.asp)           | Returns true if the **g** flag is set in the expression                                                   |
| [hasIndices](/jsref/jsref_regexp_hasindices.asp)   | Returns true if the **d** flag is set (new in 2022)                                                       |
| [ignoreCase](/jsref/jsref_regexp_ignorecase.asp)   | Returns true if the **i** flag is set                                                                     |
| [lastIndex](/jsref/jsref_regexp_lastindex.asp)     | Specifies the index at which to start the next match                                                      |
| [multiline](/jsref/jsref_regexp_multiline.asp)     | Returns true if the **m** modifier is set                                                                 |
| [source](/jsref/jsref_regexp_source.asp)           | Returns the text of the RegExp pattern                                                                    |
| [sticky](/jsref/jsref_regexp_sticky.asp)           | Returns true if the **y** flag is set (new in 2015)                                                       |
| [test()](/jsref/jsref_regexp_test.asp)             | Tests for a match in a string. Returns true or false                                                      |
| [toString()](/jsref/jsref_regexp_tostring.asp)     | Returns the string value of the regular expression                                                        |
| [unicode](/jsref/jsref_regexp_unicode.asp)         | Returns true if the **u** flag is set (new in 2018)                                                       |
| [unicodeSets](/jsref/jsref_regexp_unicodesets.asp) | Returns true if the **v** flag is set (new in 2023)                                                       |

---

## RegExp String Methods

| Method                                                      | Description                          |
| ----------------------------------------------------------- | ------------------------------------ |
| [match(regexp)](/jsref/jsref_match.asp)                     | Returns an Array of results          |
| [matchAll(regexp)](/jsref/jsref_string_matchall.asp)        | Returns an Iterator of results       |
| [replace(regexp, s)](/jsref/jsref_replace.asp)              | Returns a new String                 |
| [replaceAll(regexp, s)](/jsref/jsref_string_replaceall.asp) | Returns a new String                 |
| [search(regexp)](/jsref/jsref_search.asp)                   | Returns the index of the first match |
| [split(regexp)](/jsref/jsref_split.asp)                     | Returns an Array of results          |

#### Enriched Explanation
**What are Methods?** Functions on RegExp or String objects for applying patterns.

**Why?** Standardize operations; e.g., `matchAll()` (ES2020) for all matches as iterator.

**Real-World**: `split(/\s+/)` tokenizes commands in robotics scripts; `replaceAll()` sanitizes data in bulk.

**Pitfall**: Deprecated `compile()`—avoid, use literal notation. `lastIndex` resets on non-global.

**Reflection**: Why use `matchAll()` over `match()` with `/g`? (Iterator for large data, memory-efficient.)

## Section 2: Applied Exercises
Now, reinforce with hands-on practice. Each exercise has an **objective**, **scenario** (real-world context), **step-by-step instructions**, **hints**, and **self-check checkpoints**. Focus on reasoning: Why this pattern? Experiment with "what-if" variations.

### Exercise 1: Basic Search with Flags (Foundation)
**Objective**: Use `/i` and `/g` to search and count case-insensitive occurrences.

**Scenario**: You're building a simple climate data analyzer. Users input logs like "Temp: 72F on 2025-12-06, temp: 68f later." Count "temp" mentions ignoring case.

**Step-by-Step**:
1. Create `let log = "Temp: 72F on 2025-12-06, temp: 68f later.";`
2. Define pattern `/temp/gi`.
3. Use `log.match(pattern)` to get array.
4. Log `result.length` for count.

**Hints**: `/gi` combines flags. Without `/g`, only first match.

**Self-Check**: Output `["Temp", "temp"]`, length 2. Run in console.

**What-If Challenge**: What if log has "TEMPERATURE"? Adjust pattern to `\btemp\b/gi` (uses assertion for word boundary). Why? (Prevents partial matches.)

### Exercise 2: Character Classes & Metachars (Intermediate)
**Objective**: Extract digits and non-digits using classes/metas.

**Scenario**: Parse IoT sensor output "SensorID: S123_Error: High temp 85.2C" for numeric values (fintech-like asset tracking).

**Step-by-Step**:
1. `let data = "SensorID: S123_Error: High temp 85.2C";`
2. Pattern for digits: `/\d+/g`.
3. `data.match(pattern)` for numbers.
4. For non-digits: `/\D+/g`, match and join.

**Hints**: `\d+` uses quantifier for 1+ digits. Test with `console.log`.

**Self-Check**: Numbers: `["123", "85", "2"]`. Non-digits: Words/errors.

**What-If**: Add decimals? Use `/\d+\.\d+/g`. Why dot? (Literal with `\.`.)

### Exercise 3: Assertions & Quantifiers (Applied)
**Objective**: Validate with boundaries and counts.

**Scenario**: Robotics command validator: "move 5 steps forward" must start with "move", end with "forward", 1-3 digits.

**Step-by-Step**:
1. `let cmd = "move 05 steps forward";`
2. Pattern: `/^move \d{1,3} steps forward$/`.
3. `let pat = new RegExp(...); pat.test(cmd)`.
4. Try invalid: "Move 4steps backward".

**Hints**: `^ $` anchor whole string. `{1,3}` limits digits.

**Self-Check**: Valid: `true`; Invalid (case): `false`—add `/i`.

**What-If**: Variable steps? Use lookahead `(?= steps)`. Experiment: Does it match without consuming?

Link to Tools: Test in browser dev tools, like professional debugging.

## Section 3: Project Simulation
Apply cumulative knowledge in a mini-project: **Log Parser for Climate IoT Data**. Build a JS script that reads simulated logs, extracts temps, validates formats, and replaces units.

**Project Scenario**: You're simulating a climate monitoring dashboard. Input is multi-line log strings from sensors (e.g., "2025-12-06: Temp 72.5 F\n2025-12-06: Error: Temp -invalid"). Extract valid temps (XX.X format), count them, replace "F" to "C" (simple formula), and flag invalids. Use real-ish data: Assume logs from a CSV-like string.

**Milestones** (Progressive: Setup → Expansion → Visualization):

1. **Setup & Core Logic** (Foundation: Flags, Metas, Quantifiers):
   - **Deliverables**: Function `parseLogs(logString)` using `/g`, `\d+\.\d+`, assertions.
     - Extract temps: `/Temp \d{1,3}\.\d F/g` (case-insensitive with `/i`).
     - Validate: Use lookbehind `(?<=Temp )` + quantifiers.
     - Output: Array of valid temps (e.g., [72.5]), count, invalids flagged.
   - **Expected Output**: For input `"Temp 72.5 F\nTemp abc F"`, return `{valid: [72.5], count: 1, invalids: ["abc"]}`.
   - **Hints**: Start with `match()`, add `filter()` for validation. Partial: Just extract first.
   - **Reflection**: Compare to pro tools like ELK stack—how does regex scale for big data?

2. **Feature Expansion or Integration** (Intermediate: Assertions, Groups):
   - **Deliverables**: Add named groups `(?<temp>\d+\.\d)` for easy access. Integrate conversion: For each valid temp, compute C = (F-32)*5/9.
     - Use `replace()` with callback: `log.replace(/Temp (?<t>\d+\.\d) F/gi, (match, groups) => `Temp ${convert(groups.t)} C`)`.
     - Handle multi-line with `/m`.
   - **Expected Output**: Converted log string, e.g., "Temp 22.5 C".
   - **Hints**: `groups.t` accesses named. Test edge: Negative temps.
   - **Reflection**: Discuss scalability—regex fast for small logs, but for millions, consider libraries like XRegExp. Trade-offs?

3. **Visualization or Deployment** (Mastery: Objects, Methods):
   - **Deliverables**: Create RegExp object `const tempPat = /.../gi;`. Use `exec()` in loop for positions. "Deploy" by logging to console or simple HTML table (bonus: use `matchAll()` iterator).
     - Evaluation: Accuracy (all temps found?), Creativity (add emoji flag with `/v`?), Clarity (comments), Documentation (explain pattern).
   - **Expected Output**: Table like | Date | Temp C | Valid? | ; e.g., via `console.table(results)`.
   - **Hints**: `lastIndex` for sticky if streaming logs. Optional: Simulate file read with string.
   - **Advanced Extension**: Add Unicode for international symbols (e.g., °C with `/u`). Or, integrate with fetch() for real API logs.

**Overall Evaluation Criteria**:
- **Accuracy**: 100% temps extracted/converted.
- **Creativity**: Custom patterns for errors.
- **Clarity**: Readable code/comments.
- **Documentation**: Inline explanations.

**Partial Hints**: Stuck on groups? Recall: Named for easy `groups.name`. Test incrementally.

**Reflection Prompts**: Compare your parser to professional practices (e.g., Pandas in Python for climate data)—what's regex's strength (speedy text ops)? Scalability trade-offs (regex vs full parser)?

## Final Part: Completion Checklist & Core Takeaway
- [x] All major concepts explained in full detail (basics to advanced refs).
- [x] All exercises completed/testable (run in console).
- [x] At least one real-world project implemented (log parser with milestones).
- [x] Common pitfalls identified and corrected (e.g., greedy quantifiers, flags).
- [x] Reflection questions discussed/answered (active thinking encouraged).
- **One-Sentence Core Takeaway**: Regular expressions empower you to elegantly search, validate, and transform text patterns, turning chaotic data into actionable insights for apps like IoT monitors or fintech validators.
- **Next Topic Suggestion**: Dive into JavaScript async/await for fetching real logs, or advanced projects like building a regex-based search engine. What sparks your interest? Let's build on this!