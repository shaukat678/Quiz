# Intermediate JavaScript Coding Questions (Miscellaneous)

## Q61

```js id="p9x0a1"
console.log(1 + "2" + 3);
```

Choose the correct output:

* [ ] `6`
* [ ] `"123"`
* [ ] `"33"`
* [ ] `NaN`

---

## Q62

```js id="w4k3zb"
console.log([] + []);
```

Output?

* [ ] `[]`
* [ ] `0`
* [ ] `""`
* [ ] Error

---

## Q63

```js id="y6mn2t"
console.log(true + true);
```

Output?

* [ ] `true`
* [ ] `2`
* [ ] `1`
* [ ] `NaN`

---

## Q64

```js id="n2vz9p"
const user = {
  name: "Ali",
  greet() {
    return this.name;
  }
};

const fn = user.greet;

console.log(fn());
```

Choose the correct answer:

* [ ] `"Ali"`
* [ ] `undefined`
* [ ] `"user"`
* [ ] Error

---

## Q65

```js id="m8r1qe"
function test() {
  console.log(a);
  let a = 10;
}

test();
```

Output?

* [ ] `10`
* [ ] `undefined`
* [ ] Reference Error
* [ ] `null`

---

## Q66

```js id="h5k2do"
const arr = [1, 2, 3];

delete arr[1];

console.log(arr);
```

Choose the correct answer:

* [ ] `[1,2,3]`
* [ ] `[1, empty, 3]`
* [ ] `[1,3]`
* [ ] Error

---

## Q67

```js id="r4u8ln"
console.log(typeof []);
```

Output?

* [ ] `"array"`
* [ ] `"object"`
* [ ] `"list"`
* [ ] `"undefined"`

---

## Q68

```js id="e7xq3c"
const obj1 = { a: 1 };
const obj2 = { a: 1 };

console.log(obj1 === obj2);
```

Output?

* [ ] `true`
* [ ] `false`
* [ ] `undefined`
* [ ] Error

---

## Q69

```js id="v1q7ps"
const nums = [1, 2, 3];

const result = nums.map(num => num * 2)
                   .filter(num => num > 2);

console.log(result);
```

Output?

* [ ] `[2,4,6]`
* [ ] `[4,6]`
* [ ] `[1,2,3]`
* [ ] Error

---

## Q70

```js id="j6d9yu"
function outer() {
  let count = 0;

  return function() {
    return ++count;
  };
}

const a = outer();
const b = outer();

console.log(a());
console.log(a());
console.log(b());
```

Choose the correct output:

* [ ] `1 2 1`
* [ ] `1 1 1`
* [ ] `1 2 3`
* [ ] Error

---

## Q71

```js id="s8k4nr"
console.log(0.1 + 0.2 === 0.3);
```

Output?

* [ ] `true`
* [ ] `false`
* [ ] `undefined`
* [ ] Error

---

## Q72

```js id="t3f8qw"
const user = {
  name: "Sara"
};

Object.freeze(user);

user.name = "Ali";

console.log(user.name);
```

Choose the correct statement(s):

* [ ] Output is `"Sara"`
* [ ] Output is `"Ali"`
* [ ] `Object.freeze()` prevents modification
* [ ] Error always occurs

---

## Q73

```js id="b1w9el"
const arr = [1, 2, 3];

arr.length = 1;

console.log(arr);
```

Output?

* [ ] `[1]`
* [ ] `[1,2,3]`
* [ ] `[]`
* [ ] Error

---

## Q74

```js id="o5n2xa"
console.log(Boolean("false"));
```

Output?

* [ ] `false`
* [ ] `true`
* [ ] `undefined`
* [ ] Error

---

## Q75

```js id="f6m0rk"
setTimeout(() => console.log("A"), 0);

console.log("B");
```

Choose the correct output order:

* [ ] `A B`
* [ ] `B A`
* [ ] Only `A`
* [ ] Only `B`

---

## Q76

```js id="q7v3hj"
const arr = [1, 2, 3];

const result = arr.reduce((acc, curr) => {
  acc.push(curr * 2);
  return acc;
}, []);

console.log(result);
```

Output?

* [ ] `[1,2,3]`
* [ ] `[2,4,6]`
* [ ] `6`
* [ ] Error

---

## Q77

```js id="d4y8tp"
function x() {
  return
  {
    name: "JS"
  };
}

console.log(x());
```

Output?

* [ ] `{ name: "JS" }`
* [ ] `undefined`
* [ ] Error
* [ ] `"JS"`

---

## Q78

```js id="u0n2mw"
const person = {
  name: "Ali",
  sayHi: () => {
    console.log(this.name);
  }
};

person.sayHi();
```

Output?

* [ ] `"Ali"`
* [ ] `undefined`
* [ ] `"person"`
* [ ] Error

---

## Q79

```js id="g2k6zr"
console.log([1,2,3] + [4,5]);
```

Output?

* [ ] `[1,2,3,4,5]`
* [ ] `"1,2,34,5"`
* [ ] `15`
* [ ] Error

---

## Q80

```js id="l9s1qx"
const obj = {
  a: 1
};

const copy = obj;

copy.a = 99;

console.log(obj.a);
```

Output?

* [ ] `1`
* [ ] `99`
* [ ] `undefined`
* [ ] Error
