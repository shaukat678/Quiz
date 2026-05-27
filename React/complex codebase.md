# React Debugging Challenge — Complex Codebase with Bugs

## Q181 – Dashboard Component Debugging

```jsx id="cx181a1"
import React, {
  useEffect,
  useMemo,
  useState,
  useCallback
} from "react";

function UserList({ users, onSelect }) {
  console.log("UserList Render");

  return (
    <div>
      {users.map((user, index) => (
        <button
          key={index}
          onClick={() => onSelect(user)}
        >
          {user.name}
        </button>
      ))}
    </div>
  );
}

export default function Dashboard() {
  const [users, setUsers] = useState([
    { id: 1, name: "Ali", score: 10 },
    { id: 2, name: "Sara", score: 20 }
  ]);

  const [selectedUser, setSelectedUser] = useState(null);

  const [count, setCount] = useState(0);

  useEffect(() => {
    console.log("Fetching Users");

    setCount(count + 1);
  }, []);

  const sortedUsers = useMemo(() => {
    console.log("Sorting");

    return users.sort((a, b) => b.score - a.score);
  }, [users]);

  const handleSelect = (user) => {
    setSelectedUser(user);
  };

  function updateScore() {
    users[0].score += 10;

    setUsers(users);
  }

  return (
    <div>
      <h1>Dashboard</h1>

      <p>Count: {count}</p>

      <button onClick={updateScore}>
        Update Score
      </button>

      <UserList
        users={sortedUsers}
        onSelect={handleSelect}
      />

      {selectedUser && (
        <h2>
          Selected: {selectedUser.name}
        </h2>
      )}
    </div>
  );
}
```

---

# Questions

### Q1 – What is the biggest issue in `updateScore()`?

* [ ] Direct state mutation
* [ ] `useMemo` cannot sort arrays
* [ ] `score` cannot be updated
* [ ] `setUsers` only accepts strings

---

### Q2 – Why is this problematic?

```js
users.sort((a, b) => b.score - a.score)
```

* [ ] `sort()` mutates original array
* [ ] `sort()` only works on strings
* [ ] `useMemo` blocks sorting
* [ ] Arrays cannot be sorted in React

---

### Q3 – Better fix for sorting?

* [ ] `[...users].sort(...)`
* [ ] `users.push(...)`
* [ ] `JSON.stringify(users)`
* [ ] `useEffect(sort)`

---

### Q4 – What issue exists in this effect?

```js
useEffect(() => {
  setCount(count + 1);
}, []);
```

* [ ] Uses stale `count` value
* [ ] Causes infinite loop
* [ ] `useEffect` cannot update state
* [ ] `count` should be ref

---

### Q5 – Why may `UserList` re-render unnecessarily?

* [ ] `handleSelect` gets recreated every render
* [ ] `users.map()` is invalid
* [ ] `selectedUser` blocks rendering
* [ ] `console.log` causes loop

---

### Q6 – Best optimization for `handleSelect`?

* [ ] `useCallback`
* [ ] `useRef`
* [ ] `useMemo`
* [ ] `useEffect`

---

### Q7 – What is wrong with this key?

```jsx
key={index}
```

* [ ] Index keys may cause UI bugs
* [ ] React does not allow keys
* [ ] Keys must be random
* [ ] Keys only work with objects

---

### Q8 – Better key choice?

* [ ] `key={user.id}`
* [ ] `key={Math.random()}`
* [ ] `key={user}`
* [ ] No key needed

---

### Q9 – What happens when `updateScore()` runs?

* [ ] React may not detect proper state change
* [ ] App always crashes
* [ ] `useMemo` stops working forever
* [ ] Component automatically unmounts

---

### Q10 – Why can stale UI happen here?

* [ ] Same array reference reused
* [ ] React blocks object updates
* [ ] `sort()` deletes state
* [ ] `selectedUser` resets DOM

---

### Q11 – Which line is a side effect?

* [ ] `console.log("Fetching Users")`
* [ ] `return users.sort(...)`
* [ ] `<h1>Dashboard</h1>`
* [ ] `selectedUser && ...`

---

### Q12 – Which hook is mainly for side effects?

* [ ] `useEffect`
* [ ] `useMemo`
* [ ] `useCallback`
* [ ] `useState`

---

### Q13 – What is `useMemo` mainly optimizing here?

* [ ] Expensive sorting calculation
* [ ] API requests
* [ ] State updates
* [ ] JSX rendering syntax

---

### Q14 – Which statement is true about `useMemo`?

* [ ] It memoizes computed values
* [ ] It replaces `useState`
* [ ] It prevents all renders
* [ ] It directly updates DOM

---

### Q15 – Which statement is true about React rendering?

* [ ] Parent re-render can trigger child re-render
* [ ] React refreshes full page every state update
* [ ] Components render only once
* [ ] Virtual DOM prevents all renders

---

### Q16 – Which React concept improves UI update efficiency?

* [ ] Virtual DOM
* [ ] CSS Modules
* [ ] `console.log`
* [ ] HTML Templates

---

### Q17 – What is best fix for `updateScore()`?

* [ ]

```js
setUsers(users.map((u, i) =>
  i === 0
    ? { ...u, score: u.score + 10 }
    : u
));
```

* [ ]

```js
users[0].score += 10;
```

* [ ]

```js
setUsers(users);
```

* [ ]

```js
users.push(10);
```

---

### Q18 – Which optimization can help prevent unnecessary child renders?

* [ ] `React.memo`
* [ ] `setTimeout`
* [ ] `useRef.current`
* [ ] `JSON.parse`

---

### Q19 – Which issue is related to immutability?

* [ ] Directly modifying arrays/objects in state
* [ ] Using JSX
* [ ] Rendering components
* [ ] Passing props

---

### Q20 – Which hooks in this code are performance optimization hooks?

* [ ] `useMemo`
* [ ] `useCallback`
* [ ] `useEffect`
* [ ] `useState`
