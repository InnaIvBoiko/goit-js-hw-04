# goit-js-hw-04

## Description

Homework for Topic 6: Arrays and Object Methods.
Practice JavaScript fundamentals: objects, arrays, methods, and `this`.

## Project Structure

```
goit-js-hw-04/
├── js/
│   ├── task-1.js
│   ├── task-2.js
│   └── task-3.js
├── .gitignore
├── .prettierrc.json
├── index.html
└── README.md
```

## How to Run

Open `index.html` in the browser and check the DevTools console for output.

## Tasks

### Task 1 — Packing Goods

**File:** `task-1.js`

**Function:** `isEnoughCapacity(products, containerSize)` — calculates whether all goods will fit in a container during packing.

Parameters:

- `products` — an object where keys are product names and values are their quantities. For example, `{ apples: 2, grapes: 4 }`.
- `containerSize` — a number, the maximum number of product units the container can hold.

The function should return the result of checking whether all products fit in the container. It counts the total number of products in the `products` object and returns `true` if it is less than or equal to `containerSize`, and `false` otherwise.

```js
console.log(isEnoughCapacity({ apples: 2, grapes: 3, carrots: 1 }, 8)); // true
console.log(isEnoughCapacity({ apples: 4, grapes: 6, lime: 16 }, 12)); // false
console.log(isEnoughCapacity({ apples: 1, lime: 5, tomatoes: 3 }, 14)); // true
console.log(isEnoughCapacity({ apples: 18, potatoes: 5, oranges: 2 }, 7)); // false
```

**Mentor checklist:**

- Function `isEnoughCapacity(products, containerSize)` is declared
- `isEnoughCapacity({ apples: 2, grapes: 3, carrots: 1 }, 8)` returns `true`
- `isEnoughCapacity({ apples: 4, grapes: 6, lime: 16 }, 12)` returns `false`
- `isEnoughCapacity({ apples: 1, lime: 5, tomatoes: 3 }, 14)` returns `true`
- `isEnoughCapacity({ apples: 18, potatoes: 5, oranges: 2 }, 7)` returns `false`

---

### Task 2 — Calorie Calculation

**File:** `task-2.js`

**Function:** `calcAverageCalories(days)` — returns the average daily calorie intake consumed by an athlete during the week.

Parameters:

- `days` — an array of objects. Each object describes a day of the week and the number of `calories` consumed by the athlete on that day.

```js
console.log(
  calcAverageCalories([
    { day: "monday", calories: 3010 },
    { day: "tuesday", calories: 3200 },
    { day: "wednesday", calories: 3120 },
    { day: "thursday", calories: 2900 },
    { day: "friday", calories: 3450 },
    { day: "saturday", calories: 3280 },
    { day: "sunday", calories: 3300 },
  ])
); // 3180

console.log(
  calcAverageCalories([
    { day: "monday", calories: 2040 },
    { day: "tuesday", calories: 2270 },
    { day: "wednesday", calories: 2420 },
    { day: "thursday", calories: 1900 },
    { day: "friday", calories: 2370 },
    { day: "saturday", calories: 2280 },
    { day: "sunday", calories: 2610 },
  ])
); // 2270

console.log(calcAverageCalories([])); // 0
```

**Mentor checklist:**

- Function `calcAverageCalories(days)` is declared
- First example call returns `3180`
- Second example call returns `2270`
- `calcAverageCalories([])` returns `0`

---

### Task 3 — Player Profile

**File:** `task-3.js`

The `profile` object describes a user profile on a gaming platform. Its properties store the profile name `username` and the number of active hours `playTime` spent in the game.

```js
const profile = {
  username: "Jacob",
  playTime: 300,
};
```

Add the following methods to the `profile` object:

- `changeUsername(newName)` — accepts a string (new name) as the `newName` parameter and changes the value of the `username` property. Returns nothing.
- `updatePlayTime(hours)` — accepts a number (hours) as the `hours` parameter and increases the `playTime` property value by that amount. Returns nothing.
- `getInfo()` — returns a string in the format `<Username> has <amount> active hours!`, where `<Username>` is the profile name and `<amount>` is the number of game hours.

```js
console.log(profile.getInfo()); // "Jacob has 300 active hours!"

profile.changeUsername("Marco");
console.log(profile.getInfo()); // "Marco has 300 active hours!"

profile.updatePlayTime(20);
console.log(profile.getInfo()); // "Marco has 320 active hours!"
```

**Mentor checklist:**

- Variable `profile` is declared
- Value of `profile` is an object with properties `username`, `playTime`, `getInfo`, `changeUsername`, and `updatePlayTime`
- `getInfo`, `changeUsername`, and `updatePlayTime` are functions
- `this` is used to access object properties within its methods

---

## Submission

- Link to the repository with source files
- Link to the live page on GitHub Pages
- Attached repository file in `.zip` format

## Requirements

- Code formatted with Prettier
- No errors or warnings in the browser console
- Project structure must match the specified schema exactly
