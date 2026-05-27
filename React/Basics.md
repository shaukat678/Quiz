# React Quiz Questions — useState, useEffect, Components, Props & Virtual DOM

## Q106 – useState Basics

```jsx id="r106a1"
import React, { useState } from "react";

function App() {
  const [count, setCount] = useState(0);

  return (
    <button onClick={() => setCount(count + 1)}>
      {count}
    </button>
  );
}
```

What happens when button is clicked once?

* [ ] Count becomes `0`
* [ ] Count becomes `1`
* [ ] Error
* [ ] Component reloads page

---

## Q107 – Props

```jsx id="r107a2"
function User(props) {
  return <h1>{props.name}</h1>;
}

function App() {
  return <User name="Ali" />;
}
```

Output?

* [ ] `User`
* [ ] `Ali`
* [ ] `props`
* [ ] Error

---

## Q108 – Component Reuse

```jsx id="r108a3"
function Card() {
  return <h1>Hello</h1>;
}

function App() {
  return (
    <>
      <Card />
      <Card />
    </>
  );
}
```

Output?

* [ ] `Hello`
* [ ] `Hello Hello`
* [ ] Error
* [ ] Nothing

---

## Q109 – useEffect Runs

```jsx id="r109a4"
import React, { useEffect } from "react";

function App() {
  useEffect(() => {
    console.log("Effect");
  });

  return <h1>JS</h1>;
}
```

Choose the correct statement:

* [ ] `useEffect` runs only once
* [ ] `useEffect` runs after every render
* [ ] `useEffect` runs before render
* [ ] Error

---

## Q110 – useEffect Dependency Array

```jsx id="r110a5"
useEffect(() => {
  console.log("Mounted");
}, []);
```

What does this mean?

* [ ] Runs after every render
* [ ] Runs only once after component mounts
* [ ] Runs before component loads
* [ ] Infinite loop

---

## Q111 – State Update

```jsx id="r111a6"
const [count, setCount] = useState(5);

setCount(10);
```

New value of `count` becomes:

* [ ] `5`
* [ ] `10`
* [ ] `15`
* [ ] `undefined`

---

## Q112 – Props are

Choose the correct statement(s):

* [ ] Props are read-only
* [ ] Props are used to pass data to components
* [ ] Child component can directly modify props
* [ ] Props help component reusability

---

## Q113 – React Component Name

```jsx id="r113a7"
function hello() {
  return <h1>Hello</h1>;
}

export default hello;
```

Choose the best answer:

* [ ] Component names should usually start with uppercase
* [ ] This code will definitely crash
* [ ] Lowercase component names are recommended
* [ ] JSX does not allow functions

---

## Q114 – Virtual DOM

Choose the correct statement(s):

* [ ] Virtual DOM is a copy of Real DOM
* [ ] React compares Virtual DOM changes efficiently
* [ ] Virtual DOM directly updates browser every second
* [ ] Virtual DOM improves performance

---

## Q115 – Event Handling

```jsx id="r115a8"
function App() {
  function handleClick() {
    console.log("Clicked");
  }

  return <button onClick={handleClick}>Click</button>;
}
```

What happens on button click?

* [ ] `"Clicked"` prints in console
* [ ] Page refreshes automatically
* [ ] Error
* [ ] Nothing happens

---

## Q116 – Multiple State Updates

```jsx id="r116a9"
const [count, setCount] = useState(0);

setCount(count + 1);
setCount(count + 1);
```

Choose the best answer:

* [ ] Count always becomes `2`
* [ ] Count may become `1`
* [ ] Error
* [ ] Count becomes `0`

---

## Q117 – Conditional Rendering

```jsx id="r117b0"
function App() {
  const isLogin = true;

  return (
    <>
      {isLogin && <h1>Welcome</h1>}
    </>
  );
}
```

Output?

* [ ] `Welcome`
* [ ] Nothing
* [ ] `true`
* [ ] Error

---

## Q118 – useEffect Cleanup

```jsx id="r118b1"
useEffect(() => {
  console.log("Start");

  return () => {
    console.log("Cleanup");
  };
}, []);
```

Choose the correct statement:

* [ ] Cleanup runs when component unmounts
* [ ] Cleanup runs before effect
* [ ] Cleanup never runs
* [ ] Error

---

## Q119 – Keys in React

```jsx id="r119b2"
{
  items.map(item => (
    <li key={item.id}>{item.name}</li>
  ));
}
```

Why are `key` props used?

* [ ] For styling
* [ ] To help React identify list items efficiently
* [ ] To store state permanently
* [ ] To create loops

---

## Q120 – Parent to Child Data

```jsx id="r120b3"
function Child(props) {
  return <h2>{props.msg}</h2>;
}

function App() {
  return <Child msg="Hello React" />;
}
```

Output?

* [ ] `props`
* [ ] `Hello React`
* [ ] `undefined`
* [ ] Error
