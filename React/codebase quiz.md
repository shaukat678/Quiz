# React Debugging Quiz — Find the Bugs

## Q171 – State Mutation Bug

```jsx
import React, { useState } from "react";

export default function App() {
  const [user, setUser] = useState({
    name: "Ali",
    age: 20
  });

  function updateName() {
    user.name = "Ahmed";

    setUser(user);
  }

  return (
    <div>
      <h1>{user.name}</h1>

      <button onClick={updateName}>
        Update
      </button>
    </div>
  );
}
```

### What is the main bug?

* [ ] Direct state mutation
* [ ] `useState` cannot store objects
* [ ] `setUser` is invalid
* [ ] `button` cannot use `onClick`

---

### What is the correct fix?

* [ ] `setUser({ ...user, name: "Ahmed" })`
* [ ] `user = "Ahmed"`
* [ ] `setUser(name)`
* [ ] `useRef` instead of `useState`

---

# Q172 – Infinite useEffect Loop

```jsx
import React, { useEffect, useState } from "react";

export default function App() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    setCount(count + 1);
  });

  return <h1>{count}</h1>;
}
```

### What problem occurs?

* [ ] Infinite re-render loop
* [ ] JSX syntax error
* [ ] `useEffect` never runs
* [ ] State never changes

---

### Why does it happen?

* [ ] Missing dependency array
* [ ] `count` cannot be state
* [ ] `useEffect` only works with APIs
* [ ] `setCount` cannot run inside effect

---

# Q173 – Missing Key Prop

```jsx
import React from "react";

export default function App() {
  const users = [
    { id: 1, name: "Ali" },
    { id: 2, name: "Sara" }
  ];

  return (
    <ul>
      {users.map(user => (
        <li>{user.name}</li>
      ))}
    </ul>
  );
}
```

### What is missing?

* [ ] `key` prop
* [ ] `useEffect`
* [ ] `useRef`
* [ ] `Fragment`

---

### Best fix?

* [ ] `<li key={user.id}>{user.name}</li>`
* [ ] `<li id={user.id}>{user.name}</li>`
* [ ] `<li value={user.id}>{user.name}</li>`
* [ ] No fix needed

---

# Q174 – Wrong useEffect Dependency

```jsx
import React, { useEffect, useState } from "react";

export default function App() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    console.log(count);
  }, []);

  return (
    <button onClick={() => setCount(count + 1)}>
      Add
    </button>
  );
}
```

### What is the issue?

* [ ] Effect will not log updated count values
* [ ] `count` cannot be inside effect
* [ ] `setCount` is invalid
* [ ] JSX syntax error

---

### Correct fix?

* [ ] Add `count` in dependency array
* [ ] Remove `console.log`
* [ ] Use `useRef`
* [ ] Remove `useEffect`

---

# Q175 – Incorrect Props Mutation

```jsx
function Child(props) {
  props.name = "Ahmed";

  return <h1>{props.name}</h1>;
}

export default function App() {
  return <Child name="Ali" />;
}
```

### What is wrong?

* [ ] Props should not be mutated
* [ ] Components cannot use props
* [ ] `return` is invalid
* [ ] JSX does not allow `h1`

---

### Best practice?

* [ ] Treat props as read-only
* [ ] Always mutate props
* [ ] Store props in loop
* [ ] Convert props into string

---

# Q176 – Wrong useRef Usage

```jsx
import React, { useRef } from "react";

export default function App() {
  const countRef = useRef(0);

  function update() {
    countRef.current++;

    console.log(countRef.current);
  }

  return (
    <button onClick={update}>
      Click
    </button>
  );
}
```

### What is true about this code?

* [ ] Updating ref does not re-render UI
* [ ] `useRef` behaves exactly like state
* [ ] `useRef` causes infinite render
* [ ] `current` keyword is invalid

---

### When should `useRef` be preferred?

* [ ] For mutable values without re-render
* [ ] For all state updates
* [ ] For API fetching only
* [ ] For replacing props

---

# Q177 – Bad Rendering Optimization

```jsx
function Child({ onClick }) {
  console.log("Child Render");

  return <button onClick={onClick}>Click</button>;
}

export default function App() {
  const handleClick = () => {
    console.log("Clicked");
  };

  return <Child onClick={handleClick} />;
}
```

### Why might Child re-render unnecessarily?

* [ ] New function reference created every render
* [ ] `console.log` causes rendering
* [ ] `button` triggers render loop
* [ ] JSX cannot pass functions

---

### Best optimization?

* [ ] `useCallback`
* [ ] `useRef`
* [ ] `useEffect`
* [ ] `Fragment`

---

# Q178 – Side Effect Inside Render

```jsx
export default function App() {
  fetch("/api/data");

  return <h1>Hello</h1>;
}
```

### What is the issue?

* [ ] Side effect running during render
* [ ] `fetch` is invalid in React
* [ ] JSX syntax error
* [ ] Components cannot call APIs

---

### Correct approach?

* [ ] Move fetch inside `useEffect`
* [ ] Use `useMemo`
* [ ] Use `useRef`
* [ ] Remove API call

---

# Q179 – Stale Closure Bug

```jsx
import React, { useState } from "react";

export default function App() {
  const [count, setCount] = useState(0);

  function handleClick() {
    setTimeout(() => {
      console.log(count);
    }, 2000);
  }

  return (
    <button onClick={() => {
      setCount(count + 1);
      handleClick();
    }}>
      Add
    </button>
  );
}
```

### Possible issue?

* [ ] Timeout may log old count value
* [ ] `setTimeout` does not work in React
* [ ] State updates are synchronous
* [ ] JSX syntax error

---

### Why does this happen?

* [ ] Closure captures older state value
* [ ] `setState` is broken
* [ ] React blocks timers
* [ ] `console.log` is async

---

# Q180 – Wrong Array Update

```jsx
import React, { useState } from "react";

export default function App() {
  const [items, setItems] = useState([1, 2, 3]);

  function addItem() {
    items.push(4);

    setItems(items);
  }

  return (
    <button onClick={addItem}>
      Add
    </button>
  );
}
```

### Main bug?

* [ ] Array state mutation
* [ ] Arrays cannot be state
* [ ] `push()` is invalid
* [ ] `setItems` cannot accept arrays

---

### Correct fix?

* [ ] `setItems([...items, 4])`
* [ ] `items = 4`
* [ ] `setItems(push)`
* [ ] `useRef` instead of state
