# JavaScript Quiz – Code Bugs & Output Prediction

## 1) `let`, `var`, `const` (2 Questions)

### Q1

```js
for (var i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 100);
}
```

What will be printed?

* [ ] `0 1 2`
* [ ] `3 3 3`
* [ ] `undefined undefined undefined`
* [ ] Error

---

### Q2

```js
const user = {
  name: "Ali"
};

user.name = "Ahmed";

console.log(user.name);
```

Choose the correct statement(s):

* [ ] Output is `"Ahmed"`
* [ ] Output is `"Ali"`
* [ ] Error because `const` cannot change
* [ ] Object properties can still be modified

---

# 2) Data Types (4 Questions)

### Q3

```js
console.log(typeof null);
```

Pick the correct answer:

* [ ] `"null"`
* [ ] `"object"`
* [ ] `"undefined"`
* [ ] `"boolean"`

---

### Q4

```js
console.log([] == false);
```

What is the output?

* [ ] `true`
* [ ] `false`
* [ ] `undefined`
* [ ] Error

---

### Q5

```js
console.log("5" - 2);
```

Choose the correct answer:

* [ ] `"52"`
* [ ] `3`
* [ ] `NaN`
* [ ] Error

---

### Q6

```js
console.log(typeof NaN);
```

Output?

* [ ] `"NaN"`
* [ ] `"number"`
* [ ] `"undefined"`
* [ ] `"object"`

---

# 3) Objects & Destructuring (4 Questions)

### Q7

```js
const user = {
  name: "Sara",
  age: 20
};

const { name, age } = user;

console.log(name);
```

Output?

* [ ] `"Sara"`
* [ ] `"user"`
* [ ] `20`
* [ ] Error

---

### Q8

```js
const obj = {
  a: 1,
  b: 2
};

const { a, c } = obj;

console.log(c);
```

What happens?

* [ ] `1`
* [ ] `2`
* [ ] `undefined`
* [ ] Error

---

### Q9

```js
const person = {
  name: "Ali"
};

console.log(person.city);
```

Output?

* [ ] `null`
* [ ] `undefined`
* [ ] Error
* [ ] `"city"`

---

### Q10

```js
const user = {
  name: "Ahmed",
  skills: {
    js: true
  }
};

const {
  skills: { js }
} = user;

console.log(js);
```

Output?

* [ ] `true`
* [ ] `false`
* [ ] `"js"`
* [ ] Error

---

# 4) Arrays, map, reduce, forEach (10 Questions)

### Q11

```js
const arr = [1, 2, 3];

const result = arr.map(num => num * 2);

console.log(result);
```

Choose the output:

* [ ] `[1,2,3]`
* [ ] `[2,4,6]`
* [ ] `[3,6,9]`
* [ ] `undefined`

---

### Q12

```js
const arr = [1, 2, 3];

arr.forEach(num => num * 2);

console.log(arr);
```

Output?

* [ ] `[2,4,6]`
* [ ] `[1,2,3]`
* [ ] `undefined`
* [ ] Error

---

### Q13

```js
const nums = [1, 2, 3];

const total = nums.reduce((acc, curr) => acc + curr, 0);

console.log(total);
```

Output?

* [ ] `6`
* [ ] `123`
* [ ] `0`
* [ ] Error

---

### Q14

```js
const arr = [10];

console.log(arr[1]);
```

Output?

* [ ] `10`
* [ ] `0`
* [ ] `undefined`
* [ ] Error

---

### Q15

```js
const arr = [1, 2, 3];

const result = arr.map(num => {
  num * 2;
});

console.log(result);
```

Output?

* [ ] `[2,4,6]`
* [ ] `[undefined, undefined, undefined]`
* [ ] `[]`
* [ ] Error

---

### Q16

```js
const arr = ["a", "b", "c"];

console.log(arr.length);
```

Output?

* [ ] `2`
* [ ] `3`
* [ ] `undefined`
* [ ] Error

---

### Q17

```js
const nums = [1, 2, 3];

const result = nums.reduce((a, b) => a * b);

console.log(result);
```

Output?

* [ ] `5`
* [ ] `6`
* [ ] `9`
* [ ] Error

---

### Q18

```js
const arr = [1, 2, 3];

const result = arr.forEach(num => num + 1);

console.log(result);
```

Output?

* [ ] `[2,3,4]`
* [ ] `[1,2,3]`
* [ ] `undefined`
* [ ] Error

---

### Q19

```js
const arr = [1, 2, 3];

const result = arr.map((num, index) => index);

console.log(result);
```

Output?

* [ ] `[1,2,3]`
* [ ] `[0,1,2]`
* [ ] `[3,2,1]`
* [ ] Error

---

### Q20

```js
const arr = [5, 10, 15];

const result = arr.filter(num => num > 8);

console.log(result);
```

Output?

* [ ] `[5]`
* [ ] `[10,15]`
* [ ] `[5,10]`
* [ ] `15`

---

# 5) For & While Loops (5 Questions)

### Q21

```js
for (let i = 1; i <= 3; i++) {
  console.log(i);
}
```

Output?

* [ ] `1 2 3`
* [ ] `0 1 2`
* [ ] `1 2`
* [ ] Infinite loop

---

### Q22

```js
let i = 0;

while (i < 3) {
  console.log(i);
  i++;
}
```

Output?

* [ ] `1 2 3`
* [ ] `0 1 2`
* [ ] Infinite loop
* [ ] Error

---

### Q23

```js
for (let i = 0; i < 5; i += 2) {
  console.log(i);
}
```

Output?

* [ ] `0 2 4`
* [ ] `1 3 5`
* [ ] `0 1 2`
* [ ] Error

---

### Q24

```js
let i = 5;

while (i > 0) {
  i--;
}

console.log(i);
```

Output?

* [ ] `5`
* [ ] `1`
* [ ] `0`
* [ ] `-1`

---

### Q25

```js
for (;;) {
  console.log("JS");
}
```

Choose the correct answer:

* [ ] Runs once
* [ ] Syntax Error
* [ ] Infinite loop
* [ ] Prints nothing

---

# 6) Loops on Arrays & Objects (5 Questions)

### Q26

```js
const arr = [10, 20, 30];

for (let value of arr) {
  console.log(value);
}
```

Output?

* [ ] `0 1 2`
* [ ] `10 20 30`
* [ ] `undefined`
* [ ] Error

---

### Q27

```js
const obj = {
  a: 1,
  b: 2
};

for (let key in obj) {
  console.log(key);
}
```

Output?

* [ ] `1 2`
* [ ] `a b`
* [ ] `undefined`
* [ ] Error

---

### Q28

```js
const arr = ["x", "y"];

for (let index in arr) {
  console.log(index);
}
```

Output?

* [ ] `x y`
* [ ] `0 1`
* [ ] `undefined`
* [ ] Error

---

### Q29

```js
const obj = {
  name: "Ali"
};

console.log(Object.keys(obj));
```

Output?

* [ ] `["Ali"]`
* [ ] `["name"]`
* [ ] `"name"`
* [ ] Error

---

### Q30

```js
const arr = [1, 2];

for (let num of arr) {
  console.log(num * 2);
}
```

Output?

* [ ] `1 2`
* [ ] `2 4`
* [ ] `0 1`
* [ ] Error

---

# 7) Functions & Callback Functions (10 Questions)

### Q31

```js
function sum(a, b) {
  return a + b;
}

console.log(sum(2, 3));
```

Output?

* [ ] `23`
* [ ] `5`
* [ ] `undefined`
* [ ] Error

---

### Q32

```js
const greet = function() {
  return "Hello";
};

console.log(greet());
```

Output?

* [ ] `"Hello"`
* [ ] `Hello`
* [ ] `undefined`
* [ ] Error

---

### Q33

```js
(() => {
  console.log("JS");
})();
```

What happens?

* [ ] Nothing
* [ ] `"JS"`
* [ ] Error
* [ ] Infinite loop

---

### Q34

```js
function test() {
  console.log(a);
  var a = 5;
}

test();
```

Output?

* [ ] `5`
* [ ] `undefined`
* [ ] Error
* [ ] `null`

---

### Q35

```js
function outer() {
  let count = 0;

  return function() {
    count++;
    return count;
  };
}

const counter = outer();

console.log(counter());
```

Output?

* [ ] `0`
* [ ] `1`
* [ ] `2`
* [ ] Error

---

### Q36

```js
function sayHi(name, callback) {
  callback(name);
}

sayHi("Ali", function(user) {
  console.log(user);
});
```

Output?

* [ ] `"Ali"`
* [ ] `undefined`
* [ ] Error
* [ ] `"user"`

---

### Q37

```js
const nums = [1, 2, 3];

const result = nums.map(function(num) {
  return num + 1;
});

console.log(result);
```

Output?

* [ ] `[1,2,3]`
* [ ] `[2,3,4]`
* [ ] `[3,4,5]`
* [ ] Error

---

### Q38

```js
function demo(a = 5) {
  return a;
}

console.log(demo());
```

Output?

* [ ] `undefined`
* [ ] `0`
* [ ] `5`
* [ ] Error

---

### Q39

```js
function check() {
  return;
  console.log("JS");
}

console.log(check());
```

Output?

* [ ] `"JS"`
* [ ] `null`
* [ ] `undefined`
* [ ] Error

---

### Q40

```js
function x() {
  return function y() {
    return "Hello";
  };
}

console.log(x()());
```

Output?

* [ ] `"Hello"`
* [ ] `y`
* [ ] `undefined`
* [ ] Error

# JavaScript Theory Questions (10)

## Q41 – Difference Between `let`, `var`, and `const`

Choose the correct statement(s):

* [ ] `var` is block scoped
* [ ] `let` is block scoped
* [ ] `const` value can always be changed
* [ ] `var` can be redeclared

---

## Q42 – Array Methods

Which methods return a **new array**?

* [ ] `map()`
* [ ] `filter()`
* [ ] `forEach()`
* [ ] `reduce()`

---

## Q43 – Objects

Choose the correct statement(s):

* [ ] Objects store data in key-value pairs
* [ ] Arrays are objects in JavaScript
* [ ] Object keys must always be numbers
* [ ] You can access object values using dot notation

---

## Q44 – `===` vs `==`

Choose the correct statement(s):

* [ ] `===` checks value only
* [ ] `==` performs type conversion
* [ ] `===` checks value and type
* [ ] `==` is always safer than `===`

---



## Q46 – Loops

Choose the correct statement(s):

* [ ] `for...of` is mainly used for arrays
* [ ] `for...in` is commonly used for object keys
* [ ] `while` loop always runs once
* [ ] Infinite loops are possible in JavaScript

---

## Q47 – Callbacks

What is a callback function?

* [ ] A function passed as an argument
* [ ] A loop inside a function
* [ ] A function executed later
* [ ] A JavaScript error

---

## Q48 – Data Types

Which are primitive data types in JavaScript?

* [ ] `string`
* [ ] `number`
* [ ] `boolean`
* [ ] `object`

---

## Q49 – `map()` vs `forEach()`

Choose the correct statement(s):

* [ ] `map()` returns a new array
* [ ] `forEach()` returns a new array
* [ ] `forEach()` is mainly used for iteration
* [ ] `map()` is useful for transforming data

---

## Q50 – Hoisting

Choose the correct statement(s):

* [ ] `var` is hoisted
* [ ] Function declarations are hoisted
* [ ] `let` behaves exactly like `var`
* [ ] Accessing `let` before declaration can cause error


# Intermediate JavaScript Theory Questions (10)

## Q51 – Closures

Choose the correct statement(s) about closures:

* [ ] A closure can remember variables from its outer scope
* [ ] Closures are only possible with loops
* [ ] Closures help in data hiding
* [ ] Every function in JavaScript creates a closure

---

## Q52 – Event Loop

Choose the correct statement(s):

* [ ] JavaScript is single-threaded
* [ ] The event loop handles asynchronous tasks
* [ ] `setTimeout()` runs immediately
* [ ] Callbacks from APIs are pushed into the callback queue

---



## Q54 – Higher Order Functions

Choose the correct statement(s):

* [ ] A higher-order function can accept another function as argument
* [ ] `map()` is a higher-order function
* [ ] Functions cannot return other functions
* [ ] Higher-order functions improve code reusability

---

## Q55 – Pass By Value vs Reference

Choose the correct statement(s):

* [ ] Primitive values are copied by value
* [ ] Objects are copied by reference
* [ ] Changing one referenced object may affect another variable
* [ ] Arrays are primitive data types

---

## Q56 – Scope

Choose the correct statement(s):

* [ ] Variables declared with `let` have block scope
* [ ] Variables declared with `var` ignore function scope
* [ ] Inner functions can access outer variables
* [ ] Global variables can be accessed anywhere

---

## Q57 – Array Methods

Which statements are correct?

* [ ] `filter()` returns elements that match a condition
* [ ] `reduce()` can convert an array into a single value
* [ ] `map()` changes the original array automatically
* [ ] `find()` returns the first matching element

---

## Q58 – Hoisting & Temporal Dead Zone

Choose the correct statement(s):

* [ ] `var` variables are initialized with `undefined`
* [ ] `let` and `const` exist in Temporal Dead Zone before declaration
* [ ] Accessing `const` before declaration may cause error
* [ ] Function declarations are hoisted completely

---

## Q59 – Asynchronous JavaScript

Choose the correct statement(s):

* [ ] Promises handle asynchronous operations
* [ ] `async/await` works with promises
* [ ] `await` can pause function execution
* [ ] JavaScript waits for every API before running next line

---


