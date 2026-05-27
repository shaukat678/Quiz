# Tricky React Questions — useState, useEffect, Props, Components & Virtual DOM

## Q121 – Async State Update

```jsx id="rt121x1"
const [count, setCount] = useState(0);

function handleClick() {
  setCount(count + 1);

  console.log(count);
}
```

If button is clicked once, what prints in console?

* [ ] `0`
* [ ] `1`
* [ ] `undefined`
* [ ] Error

---

## Q122 – Multiple State Updates

```jsx id="rt122x2"
const [count, setCount] = useState(0);

function update() {
  setCount(count + 1);
  setCount(count + 1);
}
```

After one click, count most likely becomes:

* [ ] `1`
* [ ] `2`
* [ ] `0`
* [ ] Error

---

## Q123 – Correct State Update

```jsx id="rt123x3"
const [count, setCount] = useState(0);

function update() {
  setCount(prev => prev + 1);
  setCount(prev => prev + 1);
}
```

After one click, count becomes:

* [ ] `1`
* [ ] `2`
* [ ] `0`
* [ ] Error

---

## Q124 – Infinite useEffect Loop

```jsx id="rt124x4"
const [count, setCount] = useState(0);

useEffect(() => {
  setCount(count + 1);
});
```

Choose the correct answer:

* [ ] Runs once
* [ ] Infinite re-render loop
* [ ] Count becomes `1`
* [ ] Error immediately

---

## Q125 – Empty Dependency Array

```jsx id="rt125x5"
useEffect(() => {
  console.log("Mounted");
}, []);
```

How many times does this run?

* [ ] Every render
* [ ] Only once
* [ ] Twice every second
* [ ] Infinite times

---

## Q126 – Missing Return in map

```jsx id="rt126x6"
const nums = [1, 2, 3];

const result = nums.map(num => {
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

## Q127 – Props Mutation

```jsx id="rt127x7"
function Child(props) {
  props.name = "Ahmed";

  return <h1>{props.name}</h1>;
}
```

Choose the best answer:

* [ ] Props should not be mutated directly
* [ ] This is best React practice
* [ ] React requires prop mutation
* [ ] Props are state variables

---

## Q128 – Key Problem

```jsx id="rt128x8"
{
  users.map((user, index) => (
    <li key={index}>{user.name}</li>
  ));
}
```

Choose the correct statement:

* [ ] Using index as key can cause UI bugs
* [ ] Index keys are always best
* [ ] React ignores keys
* [ ] Keys are only for CSS

---

## Q129 – State Mutation Bug

```jsx id="rt129x9"
const [user, setUser] = useState({
  name: "Ali"
});

user.name = "Ahmed";

setUser(user);
```

Choose the best answer:

* [ ] Direct state mutation is bad practice
* [ ] This always forces re-render correctly
* [ ] React recommends mutating state
* [ ] Error always occurs

---

## Q130 – useEffect Cleanup Timing

```jsx id="rt130y0"
useEffect(() => {
  console.log("Effect");

  return () => {
    console.log("Cleanup");
  };
}, [count]);
```

When does cleanup run?

* [ ] Before next effect run
* [ ] Only when app closes
* [ ] Before first render
* [ ] Never

---

## Q131 – Component Re-render

```jsx id="rt131y1"
function Child() {
  console.log("Child Render");

  return <h1>Child</h1>;
}
```

Choose the correct statement:

* [ ] Child can re-render when parent re-renders
* [ ] Components render only once forever
* [ ] React blocks re-render automatically
* [ ] JSX prevents rendering twice

---

## Q132 – Virtual DOM Trick

Choose the correct statement(s):

* [ ] React updates only changed parts in DOM efficiently
* [ ] React replaces full webpage every second
* [ ] Virtual DOM comparison is called reconciliation
* [ ] Virtual DOM improves UI performance

---

## Q133 – Controlled Input

```jsx id="rt133y2"
const [name, setName] = useState("");

<input value={name} onChange={(e) => setName(e.target.value)} />
```

This input is called:

* [ ] Uncontrolled component
* [ ] Controlled component
* [ ] Static component
* [ ] Callback component

---

## Q134 – Stale Closure

```jsx id="rt134y3"
const [count, setCount] = useState(0);

function handleClick() {
  setTimeout(() => {
    console.log(count);
  }, 2000);
}
```

If count changes before timeout finishes, callback may print:

* [ ] Older value of count
* [ ] Always latest value
* [ ] Error
* [ ] Promise object

---

## Q135 – React Fragment

```jsx id="rt135y4"
return (
  <>
    <h1>Hello</h1>
    <p>React</p>
  </>
);
```

Why is `<> </>` used?

* [ ] To group multiple elements without extra DOM node
* [ ] To create CSS class
* [ ] To replace components
* [ ] To make API calls
