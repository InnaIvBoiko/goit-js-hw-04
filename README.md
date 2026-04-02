# goit-js-hw-04

## Description

Homework for Topic 4: Arrays.
Practice JavaScript fundamentals: arrays, loops, and functions.

## Project Structure

```
goit-js-hw-04/
├── js/
│   ├── task-1.js
│   ├── task-2.js
│   └── task-3.js
├── index.html
└── README.md
```

## How to Run

Open `index.html` in the browser and check the DevTools console for output.

## Tasks

### Task 1 — Slug Generator

**File:** `task-1.js`

A **slug** is a human-readable unique identifier used in web development to create readable URLs.

For example, instead of `mysite.com/posts/1q8fh74tx`, a slug based on the article title produces a friendlier URL: `mysite.com/posts/arrays-for-begginers`.

A slug is always a lowercase string with words separated by hyphens.

**Function:** `slugify(title)` — takes an article title and returns a slug created from that string.

- The `title` parameter will be a string with words separated only by spaces.
- All slug characters must be lowercase.
- All slug words must be separated by hyphens.

```js
console.log(slugify("Arrays for begginers")); // "arrays-for-begginers"
console.log(slugify("English for developer")); // "english-for-developer"
console.log(slugify("Ten secrets of JavaScript")); // "ten-secrets-of-javascript"
console.log(slugify("How to become a JUNIOR developer in TWO WEEKS")); // "how-to-become-a-junior-developer-in-two-weeks"
```

**Mentor checklist:**

- Function `slugify(title)` is declared
- All example calls return the correct slug strings

---

### Task 2 — Array Composition

**File:** `task-2.js`

**Function:** `makeArray(firstArray, secondArray, maxLength)` — takes two arrays and a number. The function creates a new array containing all elements from `firstArray` followed by all elements from `secondArray`.

- If the new array's length exceeds `maxLength`, return a copy of the array with only `maxLength` elements.
- Otherwise, return the entire new array.

```js
console.log(makeArray(["Mango", "Poly"], ["Ajax", "Chelsea"], 3)); // ["Mango", "Poly", "Ajax"]
console.log(makeArray(["Mango", "Poly", "Houston"], ["Ajax", "Chelsea"], 4)); // ["Mango", "Poly", "Houston", "Ajax"]
console.log(makeArray(["Mango"], ["Ajax", "Chelsea", "Poly", "Houston"], 3)); // ["Mango", "Ajax", "Chelsea"]
console.log(makeArray(["Earth", "Jupiter"], ["Neptune", "Uranus"], 2)); // ["Earth", "Jupiter"]
console.log(makeArray(["Earth", "Jupiter"], ["Neptune", "Uranus"], 4)); // ["Earth", "Jupiter", "Neptune", "Uranus"]
console.log(makeArray(["Earth", "Jupiter"], ["Neptune", "Uranus", "Venus"], 0)); // []
```

**Mentor checklist:**

- Function `makeArray(firstArray, secondArray, maxLength)` is declared
- All example calls return the correct arrays
- Calling `makeArray()` with random arrays and a random number returns the correct result

---

### Task 3 — Filtering an Array of Numbers

**File:** `task-3.js`

**Function:** `filterArray(numbers, value)` — takes an array of numbers and a value. Returns a new array containing only the numbers from `numbers` that are greater than `value`.

Inside the function:

1. Create an empty array to collect matching numbers.
2. Use a loop to iterate over each element of the `numbers` array.
3. Use an `if` statement inside the loop to check each element and add it to the new array.
4. Return the new array with matching numbers.

```js
console.log(filterArray([1, 2, 3, 4, 5], 3)); // [4, 5]
console.log(filterArray([1, 2, 3, 4, 5], 4)); // [5]
console.log(filterArray([1, 2, 3, 4, 5], 5)); // []
console.log(filterArray([12, 24, 8, 41, 76], 38)); // [41, 76]
console.log(filterArray([12, 24, 8, 41, 76], 20)); // [24, 41, 76]
```

**Mentor checklist:**

- Function `filterArray(numbers, value)` is declared
- All example calls return the correct arrays
- Calling `filterArray()` with a random array and number returns the correct result

---

## Requirements

- Code formatted with Prettier
- No errors or warnings in the browser console
- Project structure must match the specified schema exactly
