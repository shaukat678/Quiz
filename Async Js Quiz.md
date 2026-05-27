# Simple JavaScript Event Loop & Async Questions

## Q96 – setTimeout Basics

```js id="ev96a1"
console.log("A");

setTimeout(() => {
  console.log("B");
}, 1000);

console.log("C");
```

Choose the correct output order:

* [ ] `A B C`
* [ ] `A C B`
* [ ] `B A C`
* [ ] `C B A`

---

## Q97 – Zero Delay Timeout

```js id="ev97a2"
console.log("Start");

setTimeout(() => {
  console.log("Timeout");
}, 0);

console.log("End");
```

Output order?

* [ ] `Start Timeout End`
* [ ] `Timeout Start End`
* [ ] `Start End Timeout`
* [ ] `End Timeout Start`

---

## Q98 – Promise Basics

```js id="ev98a3"
Promise.resolve().then(() => {
  console.log("Promise");
});

console.log("JS");
```

Output?

* [ ] `Promise JS`
* [ ] `JS Promise`
* [ ] Only `Promise`
* [ ] Error

---

## Q99 – Async Function

```js id="ev99a4"
async function test() {
  return "Hello";
}

test().then(console.log);
```

Output?

* [ ] `"Hello"`
* [ ] `Promise`
* [ ] `undefined`
* [ ] Error

---

## Q100 – await Keyword

```js id="ev100a5"
async function run() {
  const result = await Promise.resolve(5);

  console.log(result);
}

run();
```

Output?

* [ ] `Promise`
* [ ] `5`
* [ ] `undefined`
* [ ] Error

---

## Q101 – Multiple setTimeouts

```js id="ev101a6"
setTimeout(() => console.log("A"), 0);

setTimeout(() => console.log("B"), 0);

console.log("C");
```

Choose the correct output order:

* [ ] `A B C`
* [ ] `C A B`
* [ ] `B A C`
* [ ] `C B A`

---

## Q102 – Promise vs setTimeout

```js id="ev102a7"
setTimeout(() => {
  console.log("Timeout");
}, 0);

Promise.resolve().then(() => {
  console.log("Promise");
});

console.log("End");
```

Output?

* [ ] `Timeout Promise End`
* [ ] `End Timeout Promise`
* [ ] `End Promise Timeout`
* [ ] `Promise End Timeout`

---

## Q103 – Async Return

```js id="ev103a8"
async function data() {
  return 10;
}

console.log(data());
```

Choose the correct answer:

* [ ] `10`
* [ ] `Promise`
* [ ] `undefined`
* [ ] Error

---

## Q104 – Callback Queue

```js id="ev104a9"
console.log("1");

setTimeout(() => {
  console.log("2");
}, 0);

console.log("3");
```

Output?

* [ ] `1 2 3`
* [ ] `1 3 2`
* [ ] `2 1 3`
* [ ] `3 2 1`

---

## Q105 – Promise Chain

```js id="ev105b0"
Promise.resolve(1)
  .then(num => num + 1)
  .then(num => console.log(num));
```

Output?

* [ ] `1`
* [ ] `2`
* [ ] `undefined`
* [ ] Error
