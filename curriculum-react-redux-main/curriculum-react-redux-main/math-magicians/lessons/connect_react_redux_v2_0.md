# Connect React & Redux

## Learning objectives

- Connect React and Redux.

### Estimated time: 2.5h

## Description

[Redux](https://redux.js.org/) is a popular **global state management library**. It is a standalone library that can be used with [vanilla JavaScript applications](https://www.sitepoint.com/redux-without-react-state-management-vanilla-javascript/), as well as with UI frameworks like React, [Angular](https://github.com/angular-redux/store), or [Vue](https://github.com/titouancreach/vuejs-redux).

To use Redux with any of these frameworks you need to introduce some "UI binding" to connect Redux and the UI framework. [**React-Redux**](https://react-redux.js.org/) is the official Redux UI binding library for React applications. If you are using Redux and React together, you should use **React-Redux** to bind these two libraries.

### The React-Redux library

When reading about the [React-Redux library](https://react-redux.js.org/introduction/why-use-react-redux) you might encounter two different API's:

- `Connect` API
- `Hooks` API

`Connect` API is older and used to be the default for React `class` based applications.

Since v7.1.0 **React Redux** supports the `Hooks` API, which is now the recommended way to use the **React Redux Hooks API** as the default approach in your React components development.

#### Step 1: Connect Redux with React

First, you need to connect the Redux store with React at the root level of your application:

```jsx
import React from "react"
import ReactDOM from "react-dom/client"

import { Provider } from "react-redux"
import store from "./store"

import App from "./App"

const root = ReactDOM.createRoot(document.getElementById("root"))

root.render(
  // This is how Redux is connected to a React application
  <Provider store={store}>
    <App />
  </Provider>
)
```

#### Step 2: Access the Redux store inside of a component

Second, in order to access your **state variables** and **state modifiers** inside of your functional components:

```jsx
import React from "react"
import { useSelector, useDispatch } from "react-redux"
import {
  decrement,
  increment,
  incrementByAmount,
  incrementAsync,
  selectCount,
} from "./counterSlice"
import styles from "./Counter.module.css"

export function Counter() {
  const count = useSelector(selectCount) // Provides access to the state variable
  const dispatch = useDispatch() // Triggers the Redux store for state updates

  return (
    <div>
      <div className={styles.row}>
        <button
          className={styles.button}
          aria-label="Increment value"
          onClick={() => dispatch(increment())} // dispatch triggers the Redux store for state updates
        >
          +
        </button>
        <span className={styles.value}>{count}</span>
        <button
          className={styles.button}
          aria-label="Decrement value"
          onClick={() => dispatch(decrement())} // dispatch triggers the Redux store for state updates
        >
          -
        </button>
      </div>
      {/* omit additional rendering output here */}
    </div>
  )
}
```

- Read the [official React Redux introduction to Hooks API](https://react-redux.js.org/api/hooks).

## Additional materials

**These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.**

- Read more about [oficially recommended files and folders structure](https://redux.js.org/style-guide/style-guide#structure-files-as-feature-folders-with-single-file-logic).

When working with some legacy code or reading about React Redux from older sources you might find many references to the `connect` API and functions like `mapStateToProps` or `mapDispatchToProps`. If you want to familiarise yourself with the basic concepts of it, check this [basic tutorial on `connect` API](https://react-redux.js.org/tutorials/connect).

_Keep in mind that this is **NOT** being used anymore, but you might still see it in legacy projects._

---

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._