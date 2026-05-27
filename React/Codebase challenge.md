# React Debugging Challenge — Large but Easy Codebase

```jsx id="lg201a1"
import React, {
  useEffect,
  useMemo,
  useRef,
  useState
} from "react";

function Header({ title }) {
  console.log("Header Render");

  return <h1>{title}</h1>;
}

function SearchBar({ search, setSearch }) {
  console.log("SearchBar Render");

  return (
    <input
      type="text"
      value={search}
      onChange={(e) => setSearch(e.target.value)}
      placeholder="Search user..."
    />
  );
}

function UserCard({ user, onDelete }) {
  console.log("UserCard Render");

  return (
    <div
      style={{
        border: "1px solid gray",
        margin: "10px",
        padding: "10px"
      }}
    >
      <h3>{user.name}</h3>

      <p>Age: {user.age}</p>

      <button onClick={() => onDelete(user.id)}>
        Delete
      </button>
    </div>
  );
}

function Counter() {
  const [count, setCount] = useState(0);

  const renderCount = useRef(0);

  renderCount.current++;

  useEffect(() => {
    console.log("Counter Mounted");
  }, []);

  return (
    <div>
      <h2>Count: {count}</h2>

      <h3>Renders: {renderCount.current}</h3>

      <button onClick={() => setCount(count + 1)}>
        Increment
      </button>
    </div>
  );
}

export default function App() {
  const [users, setUsers] = useState([
    { id: 1, name: "Ali", age: 20 },
    { id: 2, name: "Sara", age: 22 },
    { id: 3, name: "Ahmed", age: 25 }
  ]);

  const [search, setSearch] = useState("");

  const [darkMode, setDarkMode] = useState(false);

  useEffect(() => {
    console.log("App Mounted");
  }, []);

  const filteredUsers = useMemo(() => {
    console.log("Filtering Users");

    return users.filter((user) =>
      user.name
        .toLowerCase()
        .includes(search.toLowerCase())
    );
  }, [users, search]);

  function deleteUser(id) {
    const updatedUsers = users.filter(
      (user) => user.id !== id
    );

    setUsers(updatedUsers);
  }

  function addUser() {
    const newUser = {
      id: Date.now(),
      name: "New User",
      age: 18
    };

    users.push(newUser);

    setUsers(users);
  }

  return (
    <div
      style={{
        background: darkMode ? "#222" : "#fff",
        color: darkMode ? "#fff" : "#000",
        minHeight: "100vh",
        padding: "20px"
      }}
    >
      <Header title="User Dashboard" />

      <button
        onClick={() =>
          setDarkMode(!darkMode)
        }
      >
        Toggle Theme
      </button>

      <hr />

      <SearchBar
        search={search}
        setSearch={setSearch}
      />

      <button onClick={addUser}>
        Add User
      </button>

      <hr />

      {filteredUsers.map((user, index) => (
        <UserCard
          key={index}
          user={user}
          onDelete={deleteUser}
        />
      ))}

      <hr />

      <Counter />
    </div>
  );
}
```

# Questions

## Q201 – What is the main bug in `addUser()`?

* [ ] Direct state mutation
* [ ] `push()` does not exist
* [ ] `useState` cannot store arrays
* [ ] `setUsers` is invalid

---

## Q202 – Why is this problematic?

```js id="9qv66u"
users.push(newUser);
setUsers(users);
```

* [ ] Same array reference reused
* [ ] React blocks arrays
* [ ] `push()` creates new array automatically
* [ ] `setUsers` only accepts objects

---

## Q203 – Best fix for `addUser()`?

* [ ]

```js id="k4zvvv"
setUsers([...users, newUser]);
```

* [ ]

```js id="5m9edv"
users.push(newUser);
```

* [ ]

```js id="5c8zfr"
setUsers(users);
```

* [ ]

```js id="c0r5mj"
setUsers("newUser");
```

---

## Q204 – Why is `useMemo` used here?

* [ ] To optimize filtering calculation
* [ ] To replace `useEffect`
* [ ] To create state
* [ ] To access DOM directly

---

## Q205 – When does `filteredUsers` recalculate?

* [ ] When `users` or `search` changes
* [ ] Only once
* [ ] Every second automatically
* [ ] Only when darkMode changes

---

## Q206 – Which line is a side effect?

* [ ] `console.log("App Mounted")`
* [ ] `return users.filter(...)`
* [ ] `<Header />`
* [ ] `setSearch`

---

## Q207 – Which hook is mainly used for side effects?

* [ ] `useEffect`
* [ ] `useMemo`
* [ ] `useRef`
* [ ] `useState`

---

## Q208 – What does this do?

```js id="o1w7od"
const renderCount = useRef(0);
```

* [ ] Stores mutable value across renders
* [ ] Creates state variable
* [ ] Causes re-render
* [ ] Creates API request

---

## Q209 – Why does this value increase?

```js id="wgrv6v"
renderCount.current++;
```

* [ ] Component re-renders
* [ ] `useRef` behaves like loop
* [ ] `useEffect` updates it automatically
* [ ] Browser updates it

---

## Q210 – Updating `useRef.current` does what?

* [ ] Does NOT trigger re-render
* [ ] Always triggers re-render
* [ ] Deletes component
* [ ] Resets state

---

## Q211 – What is wrong with this key?

```jsx id="b6v0o5"
key={index}
```

* [ ] Index keys may cause UI issues
* [ ] React forbids keys
* [ ] Keys must be strings only
* [ ] Keys create infinite loops

---

## Q212 – Better key choice?

* [ ] `key={user.id}`
* [ ] `key={Math.random()}`
* [ ] `key={user}`
* [ ] No key required

---

## Q213 – Which state change causes App component to re-render?

* [ ] `setSearch`
* [ ] `setUsers`
* [ ] `setDarkMode`
* [ ] All of them

---

## Q214 – Why can child components re-render often?

* [ ] Parent component re-renders
* [ ] JSX blocks rendering
* [ ] `useEffect` disables optimization
* [ ] React refreshes browser

---

## Q215 – Which React concept improves rendering efficiency?

* [ ] Virtual DOM
* [ ] CSS
* [ ] `console.log`
* [ ] HTML attributes

---

## Q216 – What does `SearchBar` receive from parent?

* [ ] Props
* [ ] State directly
* [ ] Context API
* [ ] DOM nodes

---

## Q217 – Props are mainly used for?

* [ ] Parent to child communication
* [ ] Updating browser cache
* [ ] Direct DOM editing
* [ ] API fetching

---

## Q218 – Why does this work?

```jsx id="j3cvlq"
value={search}
```

* [ ] Controlled input
* [ ] Virtual DOM caching
* [ ] useRef binding
* [ ] Async rendering

---

## Q219 – Which statement about rendering is true?

* [ ] State updates can trigger rendering
* [ ] React reloads full page on every render
* [ ] Components render only once
* [ ] Rendering always means DOM replacement

---

## Q220 – Which hook here is mainly for performance optimization?

* [ ] `useMemo`
* [ ] `useEffect`
* [ ] `useState`
* [ ] `useRef`
