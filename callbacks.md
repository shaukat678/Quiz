#---

## Q81 – Callback Function

```js id="cb81x1"
function greet(name, callback) {
  callback(name);
}

greet("Ali", function(user) {
  console.log("Hello " + user);
});
```

Output?

* [ ] `"Hello Ali"`
* [ ] `"Ali"`
* [ ] `undefined`
* [ ] Error

---

## Q82 – Callback Return Value

```js id="cb82x2"
function calc(a, b, callback) {
  return callback(a, b);
}

const result = calc(2, 3, (x, y) => x * y);

console.log(result);
```

Output?

* [ ] `5`
* [ ] `6`
* [ ] `23`
* [ ] Error

---

## Q83 – setTimeout Loop Bug

```js id="cb83x3"
for (var i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 0);
}
```

Output?

* [ ] `0 1 2`
* [ ] `3 3 3`
* [ ] `undefined undefined undefined`
* [ ] Error

---

## Q84 – let in Loop

```js id="cb84x4"
for (let i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 0);
}
```

Output?

* [ ] `3 3 3`
* [ ] `0 1 2`
* [ ] `undefined`
* [ ] Error

---

## Q85 – Nested Loops

```js id="cb85x5"
for (let i = 1; i <= 2; i++) {
  for (let j = 1; j <= 2; j++) {
    console.log(i, j);
  }
}
```

Output?

* [ ] `1 1`, `1 2`, `2 1`, `2 2`
* [ ] `1 2`, `2 1`
* [ ] Infinite loop
* [ ] Error

---

## Q86 – while Loop

```js id="cb86x6"
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

## Q87 – Callback Inside map

```js id="cb87x7"
const nums = [1, 2, 3];

const result = nums.map(function(num) {
  return num + 2;
});

console.log(result);
```

Output?

* [ ] `[1,2,3]`
* [ ] `[3,4,5]`
* [ ] `[2,3,4]`
* [ ] Error

---

## Q88 – Infinite Loop Bug

```js id="cb88x8"
let i = 0;

while (i < 5) {
  console.log(i);
}
```

Choose the correct answer:

* [ ] Prints `0 1 2 3 4`
* [ ] Infinite loop
* [ ] Error
* [ ] Prints nothing

---

## Q89 – forEach Callback

```js id="cb89x9"
const arr = [1, 2, 3];

arr.forEach(function(num, index) {
  console.log(index, num);
});
```

Output?

* [ ] `1 2 3`
* [ ] `0 1`, `1 2`, `2 3`
* [ ] `[0,1,2]`
* [ ] Error

---

## Q90 – break in Loop

```js id="cb90x0"
for (let i = 1; i <= 5; i++) {
  if (i === 3) break;

  console.log(i);
}
```

Output?

* [ ] `1 2`
* [ ] `1 2 3`
* [ ] `1 2 3 4 5`
* [ ] Error

---

## Q91 – continue in Loop

```js id="cb91x1"
for (let i = 1; i <= 5; i++) {
  if (i === 3) continue;

  console.log(i);
}
```

Output?

* [ ] `1 2 4 5`
* [ ] `1 2 3 4 5`
* [ ] `3`
* [ ] Error

---

## Q92 – Callback Execution Order

```js id="cb92x2"
console.log("Start");

setTimeout(() => {
  console.log("Callback");
}, 0);

console.log("End");
```

Correct output order?

* [ ] `Start Callback End`
* [ ] `Callback Start End`
* [ ] `Start End Callback`
* [ ] `End Start Callback`

---

## Q93 – do...while Loop

```js id="cb93x3"
let i = 5;

do {
  console.log(i);
  i++;
} while (i < 5);
```

Output?

* [ ] Nothing
* [ ] `5`
* [ ] Infinite loop
* [ ] Error

---

## Q94 – reduce Callback

```js id="cb94x4"
const nums = [1, 2, 3];

const total = nums.reduce((acc, curr) => {
  return acc + curr;
}, 0);

console.log(total);
```

Output?

* [ ] `123`
* [ ] `6`
* [ ] `0`
* [ ] Error

---

## Q95 – Looping Object

```js id="cb95x5"
const obj = {
  a: 1,
  b: 2
};

for (let key in obj) {
  console.log(key, obj[key]);
}
```

Output?

* [ ] `a 1`, `b 2`
* [ ] `1 2`
* [ ] `a b`
* [ ] Error
