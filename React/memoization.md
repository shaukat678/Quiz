# Tricky React Questions — `useMemo` & `useCallback`

## Q136 – useMemo Basics

```jsx id="rm136a1"
const value = useMemo(() => {
  return 2 + 2;
}, []);
```

What is `value`?

* [ ] Function
* [ ] `4`
* [ ] `undefined`
* [ ] Promise

---

## Q137 – useMemo Purpose

Choose the correct statement(s):

* [ ] `useMemo` memoizes computed values
* [ ] `useMemo` improves performance in expensive calculations
* [ ] `useMemo` is mainly used for API requests
* [ ] `useMemo` recalculates when dependencies change

---

## Q138 – Missing Dependency

```jsx id="rm138a2"
const total = useMemo(() => {
  return price * quantity;
}, [price]);
```

Choose the best answer:

* [ ] `quantity` should also be dependency
* [ ] Code is always perfect
* [ ] `useMemo` does not need dependencies
* [ ] Error immediately occurs

---

## Q139 – useCallback Basics

```jsx id="rm139a3"
const handleClick = useCallback(() => {
  console.log("Clicked");
}, []);
```

What does `useCallback` return?

* [ ] A memoized function
* [ ] A number
* [ ] JSX
* [ ] Promise

---

## Q140 – useCallback Purpose

Choose the correct statement(s):

* [ ] `useCallback` memoizes functions
* [ ] Helps prevent unnecessary re-renders
* [ ] Mostly useful when passing callbacks to child components
* [ ] `useCallback` replaces `useState`

---

## Q141 – Dependency Array Trick

```jsx id="rm141a4"
const fn = useCallback(() => {
  console.log(count);
}, []);
```

Choose the correct answer:

* [ ] Callback may use stale `count` value
* [ ] Callback always gets latest value automatically
* [ ] Dependency array is unnecessary
* [ ] Error occurs immediately

---

## Q142 – useMemo Recalculation

```jsx id="rm142a5"
const result = useMemo(() => {
  console.log("Calculating");

  return num * 2;
}, [num]);
```

When will `"Calculating"` run?

* [ ] On every render only
* [ ] Only when `num` changes
* [ ] Never
* [ ] Only once forever

---

## Q143 – useCallback with Child Component

```jsx id="rm143a6"
const handleClick = () => {
  console.log("Hi");
};

<Child onClick={handleClick} />
```

Why might developers use `useCallback` here?

* [ ] To avoid creating new function on every render
* [ ] To stop JSX rendering
* [ ] To replace props
* [ ] To make API faster

---

## Q144 – useMemo Return Value

```jsx id="rm144a7"
const data = useMemo(() => {
  return { name: "Ali" };
}, []);
```

Choose the correct statement:

* [ ] Same object reference can be reused
* [ ] New object always created every render
* [ ] `useMemo` returns function only
* [ ] Error

---

## Q145 – useCallback vs useMemo

Choose the correct statement(s):

* [ ] `useCallback` memoizes functions
* [ ] `useMemo` memoizes values
* [ ] Both accept dependency arrays
* [ ] Both are performance optimization hooks

---

## Q146 – Wrong useMemo Usage

```jsx id="rm146a8"
const result = useMemo(() => {
  fetchData();
}, []);
```

Choose the best answer:

* [ ] `useEffect` is usually better for side effects
* [ ] Perfect use of `useMemo`
* [ ] `useMemo` is made for API calls
* [ ] `fetchData` cannot run here

---

## Q147 – Expensive Calculation

```jsx id="rm147a9"
const sorted = useMemo(() => {
  return items.sort();
}, [items]);
```

Why use `useMemo` here?

* [ ] To avoid expensive recalculation on every render
* [ ] To create state
* [ ] To stop rendering completely
* [ ] To mutate props safely

---

## Q148 – React.memo + useCallback

Choose the correct statement(s):

* [ ] `React.memo` can prevent unnecessary child renders
* [ ] Passing new function references may still re-render child
* [ ] `useCallback` can help with stable function references
* [ ] `React.memo` automatically memoizes state

---

## Q149 – Empty Dependency Array

```jsx id="rm149b0"
const fn = useCallback(() => {
  console.log("JS");
}, []);
```

Choose the best answer:

* [ ] Same function reference reused between renders
* [ ] New function created every render
* [ ] Callback runs automatically
* [ ] Error

---

## Q150 – Performance Optimization

Choose the correct statement(s):

* [ ] Overusing `useMemo` can hurt readability
* [ ] `useCallback` should be used only when beneficial
* [ ] Memoization is mainly a performance optimization
* [ ] Every React app needs `useMemo` everywhere
