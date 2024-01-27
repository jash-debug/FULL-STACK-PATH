# Redux and API: Intro

### Redux and async data

When working with data that is fetched from a server, we are dealing with **asynchronous** data.

However, **Redux itself only works synchronous by default**. The [documentation](https://redux.js.org/tutorials/fundamentals/part-6-async-logic#redux-middleware-and-side-effects) explains:

> "By itself, a Redux store doesn't know anything about async logic. It only knows how to synchronously dispatch actions, update the state by calling the root reducer function, and notify the UI that something has changed."

To be able to work with async data, you should learn about **middlewares**, **thunks** and **side effects**.

#### What are middlewares in Redux?

In Redux Toolkit, **middleware** refers to a layer of code that sits between the dispatch action and the reducer. It allows you to **modify or enhance the behavior of your store** by:

- Intercepting dispatched actions, or
- Performing some processing

and then either forwarding the action to the next middleware or directly to the reducer.

Middlewares are **chainable**, which means that you can have several middlewares that will be called one after the other _(we will see in the next section below)_.

- [Redux Middleware and Side Effects](https://redux.js.org/tutorials/fundamentals/part-6-async-logic#redux-middleware-and-side-effects)

#### Using the `thunk` middleware

There's a special kind of middleware that allows you to introduce custom logic to your Redux store: a **thunk**. Thunks can be created and dispatched using the `createSlice` and `createAsyncThunk` functions provided by Redux Toolkit.

But, what is a "thunk"? In general programming, a **thunk** is a programming term that means a piece of code that does some delayed (asynchronous) work.

In Redux Toolkit, it is a higher-order function that allows for **asynchronous actions and state updates** in your Redux store. It's a way to handle **side-effects such as API calls or other asynchronous actions in a Redux store**, allowing you to delay or conditionally dispatch actions.

- [React Redux Thunk Middleware in Redux Toolkit](https://www.youtube.com/watch?v=93CR_yURoII)

### Thunks vs. middlewares

In Redux Toolkit, both **thunks** and **middleware** are used to handle side-effects and perform asynchronous operations in your Redux store, but they differ in terms of their purpose and how they are used.

A **thunk** refers to a higher-order function that returns a function that dispatches an action. A **middleware** refers to a layer of code that sits between the dispatched action and the reduction of the state.

#### How to work with side effects in Redux

A **side effect** is any change to state or behavior that can be seen _outside of returning a value from a function_. Some common kinds of side effects are things like:

- Logging a value to the console
- Saving a file
- Setting an async timer
- Making an AJAX HTTP request
- Modifying some state that exists outside of a function, or mutating arguments to a function
- Generating random numbers or unique random IDs (such as `Math.random()` or `Date.now()`)

One of the foundations of Redux is that you should _avoid side effects_ in reducers, but **middlewares are designed to work with side effects** in a safe way.

- [React Redux Thunk Middleware in Redux Toolkit](https://www.youtube.com/watch?v=93CR_yURoII)

---

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
