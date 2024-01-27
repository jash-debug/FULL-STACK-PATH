# Connect your React & Redux app to API

## Learning objectives

- Connect an existing API via Redux and use the data to display something in a UI.

### Estimated time: 2h

## Description

In this lesson, you will learn how to **connect your application to an existing API**, and use that data in your application.

### Why is connecting React-Redux with an API important?

In past lessons, you learned how to add Redux to a React application, and got familiar with Redux concepts such as **store**, **reducers**, and **actions**. With this knowledge you can develop a React application with global state management.

However, in the real world you will work with **external data**: either from an external API or a database. So the next step is to learn how to make HTTP requests from a complex React/Redux application.

### Redux and API: intro

#### Preliminary concepts

To connect Redux with an API you should first learn about a few preliminary concepts:

- Middlewares
- Side effects
- Thunks

To learn more about these concepts read the following article: [Redux and API: intro](../articles/redux_and_api_intro.md).

#### Connect to an external API

As Redux is synchronous by default, we should add a specific **thunk** middleware called `createAsyncThunk` in order to perform asynchronous operations like HTTP requests.

Read the following to learn more about that:

- [Using Middleware to Enable Async Logic](https://redux.js.org/tutorials/fundamentals/part-6-async-logic#using-middleware-to-enable-async-logic)

## Additional materials

**These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.**

If you want to understand why middlewares are needed, and get familiar with terms like _thunk_, read:

- [Why do we need middleware for async flow in Redux?](https://stackoverflow.com/questions/34570758/why-do-we-need-middleware-for-async-flow-in-redux/34599594#34599594).

---

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
