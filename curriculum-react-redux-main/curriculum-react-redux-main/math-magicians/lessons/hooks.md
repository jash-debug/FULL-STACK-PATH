# Hooks

## Learning objectives

- Use React hooks.

### Estimated time: 2h

## Description

In this lesson you will learn how to use `state` inside of your functional components with **React hooks**.

### Why are React hooks important?

In React.js, "hooks" are **special functions** that let you "hook into" React state and lifecycle features inside of functional components. They were introduced in [React v16.8](https://reactjs.org/docs/hooks-intro.html).

They are crucial to adding and manipulating state and the DOM.

- [10 React Hooks Explained](https://www.youtube.com/watch?v=TNhaISOUy6Q)

### React hooks

There are several hooks you should learn, with the most important being [useState](https://beta.reactjs.org/reference/react/useState) and [useEffect](https://beta.reactjs.org/reference/react/useEffect),

#### The `useState` hook

The state hook, `useState`, is used to **add state to a component**. It will return an array with a pair of items:

- A state variable
- A state modifier: a function that can modify the state variable

Let's see an example:

```jsx
import React, { useState } from "react"

function Example() {
  const [count, setCount] = useState(0)

  const increment = () => setCount(count + 1)

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={increment}>Click me</button>
    </div>
  )
}
```

What are we doing in this example?

- Before using it, you need to import `useState` from React.
- The line `const [count, setCount] = useState(0);` does the following:
  - It calls `useState` passing `0` as the initial value.
  - `useState` returns an array with two items: the state variable, and a state modifier.
- Using [destructuring assignment syntax](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment) (the `[]`), we assign the initial value to `count`, and the function to `setCount` variables.
- Now, we can use `count` and `setCount` in the component.
- To modify the value of `count`, you must do it with `setCount`.
- The value you pass to `useState` can be any data type, not necessarily a `number` or `string`.

#### The `useEffect` hook

The "useEffect" hook in React is a way to **handle side effects in your functional components**. Side effects refer to anything that affects your component outside of the render function, like:

- Fetching data
- Updating the DOM
- Setting a timer

The useEffect hook lets you tell React **when to run an effect** and **how to clean it up**. It takes two arguments:

- A "effect" function that contains your side effect logic
- An optional "dependency array" that tells React when to re-run the effect.

```jsx
import React, { useState, useEffect } from "react"

function Example() {
  const [users, setUsers] = useState([])

  useEffect(() => {
    const fetchUsers = async () => {
      const response = await fetch("https://randomuser.me/api/")
      const fetchedUsers = await response.json()

      setUsers(fetchedUsers.results)
    }

    fetchUsers()
  }, [])

  return (
    <div>
      {users.length > 0 ? (
        <ul>
          {users.map((user) => (
            <li key={user.id.value}>User: {user.name.first}</li>
          ))}
        </ul>
      ) : (
        <p>No users!</p>
      )}
    </div>
  )
}
```

What are we doing in this example?

- Before using it, you need to import `useEffect` from React.
- The `useEffect` callback does the following:
  - The asynchronous function `fetchUsers` makes an HTTP request to an external API
  - It parses the response
  - It modifies the state using the state modifiers `setUsers`
- The second argument, the dependency array, is empty which means the callback **will be executed once**

For more information about the `useEffect` hook:

- [Learn useEffect In 13 Minutes](https://www.youtube.com/watch?v=0ZJgIjIuY7U)
- [useEffect Dependency array](https://codedamn.com/news/reactjs/useeffect-dependency#useEffect_Dependency_array)
- [All useEffect Mistakes Every Junior React Developer Makes](https://www.youtube.com/watch?v=QQYeipc_cik)

## Rules of hooks

There are a couple of rules you should follow to work with hooks:

- You should call hooks at the top level of a component (before `return`).
- Don't call them inside **loops**, **conditions**, or **nested functions**.
- Only call hooks inside functional components (not from vanilla JS functions).

To learn more about hooks rules and to find some useful tools to work with, read the React documentation section [Rules of Hooks](https://reactjs.org/docs/hooks-rules.html).

## Other hooks

`useState` and `useEffect` hooks are the most important hooks to master. But there are others:

- `useContext`
- `useReducer`
- `useCallback`
- `useMemo`
- `useRef`
- `useImperativeHandle`
- `useLayoutEffect`
- `useDebugValue`

We are not going to explain each one, but if you understand how `useState` and `useEffect` work and follow the rules of hooks, you will be able to understand all of them.

For the complete documentation of hooks, read [Hooks API Reference](https://reactjs.org/docs/hooks-reference.html).

## Additional materials

**These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.**

- [React Hooks Course - All React Hooks Explained](https://www.youtube.com/watch?v=LlvBzyy-558)

---

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._