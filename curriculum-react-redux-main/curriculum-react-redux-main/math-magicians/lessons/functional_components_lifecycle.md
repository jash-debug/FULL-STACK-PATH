# Functional components lifecycle

## Learning objectives

- Use React lifecycle methods.
- Use React hooks.

### Estimated time: 1h

## Description

In this lesson, you will learn what **component lifecycle is** and **how they work in functional components**.

### Why is component lifecycle important?

Everything in this world has a lifecycle. Take humans: we are born, grow, and then die. Like humans, React components also have a lifecycle:

- Components are born (**mounted** on the DOM)
- They grow (**updating** when it receives new props or state)
- and, eventually, die (**unmount** from DOM)

In React, this is referred to as `component lifecycle`.

On the surface this seems like a radical idea: **rendering a component in various stages**. Usually when you deal with regular HTML you just load a page into the browser and it’s done, right? Well, actually no. A regular HTML page actually also has a lifecycle!

- [Page: DOMContentLoaded, load, beforeunload, unload](https://javascript.info/onload-ondomcontentloaded)

React just took the concept and reduced its scale from a complete page to a component of a page.

The 3 states a component can be in (mounted, updating, unmounted) determine **when a component is rendered into the DOM**.

- [The React Lifecycle of a Functional Component](https://www.youtube.com/watch?v=Zz9pLellSQA)

### useEffect

- The `useEffect`, allows you to perform _side effects_ (a change produced by another change) when state changes.
- You will use `useEffect` together with `useState`.
- `useEffect` expects two arguments (it is a function!): a function, and a _array that should include state variables_ (known as a **dependency array**)
- In the dependency array, you can pass the pieces of state you want to watch. Every time one of those variables changes, `useEffect` will be called.
- If the dependency array is empty, `useEffect` will be called **just once** (after component is mounted, similar to `componentDidMount()`).

Let's see an example:

```javascript
import React, { useState, useEffect } from "react"

function Example() {
  const [count, setCount] = useState(0)

  useEffect(() => {
    console.log(`You clicked ${count} times`)
  }, [count]) // Executes the console.log whenever the "count" variable is updated

  const increment = () => {
    setCount(count + 1)
  }

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={increment}>Increment by 1</button>
    </div>
  )
}
```

This example does the following:

- It creates a `count` state variable, and a function, `setCount`, to change its value.
- Every time you click on the button then `setCount` is called, updating the value of `count`.
- `useEffect` receives a **function as its first argument**, and a **dependency array as its second argument**, containing only one state variable (`[count]`).
- Every time the value of `count` changes, `useEffect` is called. It will ignore other state variables.

Let's see another common example, fetching data when the components are mounted:

```javascript
import React, { useState, useEffect } from "react"

function Example() {
  const [users, setUsers] = useState(null)

  useEffect(() => {
    const fetchData = async () => {
      const response = await fetch(`https://your-super-cool-api.com/users`)
      const usersData = await response.json()
      setUsers(usersData)
    }
    fetchData()
  }, []) // Executes once, after the component has been mounted

  return <div>{users.length > 0 ? JSON.stringify(users) : "Loading..."}</div>
}
```

This example is a bit different:

- The dependency array is empty.
- It will be executed **only once**, after the component is mounted into the DOM
- When doing asynchronous requests, you can't use the `async` keyword directly in `useEffect`, you should create a function inside it (`fetchData`) and call it immediately.

- [UseEffect & UseEffect with API Requests](https://www.youtube.com/watch?v=3Wb9l18KoxI)
- [Offial documentation - useEffect](https://beta.reactjs.org/reference/react/useEffect)

---

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._