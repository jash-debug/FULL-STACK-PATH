# Add Redux to your project

## Learning objectives

- Connect React and Redux.

### Estimated time: 0.5h

## Description

Redux is meant to help you to **manage the state of your app globally**. In this lesson you will learn how to add it to your project, using Redux Toolkit.

### Why is it important?

Previously, you've learned **how to manage state locally**:

- You define state inside of a functional component using `useState`
- You use the state variables and modifiers either (1) inside the same component, or (2) pass it as props to a child component

But what if you have a component hierarchy that's 10+ levels deep? You will inevitebly end up with `prop drilling`.

Redux solves this problem by producing a structured way to manage state globally (by placing everything inside of a **store**. Whenever a particular component needs to use state, it connects directly to the store with `useSelector` and `useDispatch`.

- [Redux Explained](https://almerosteyn.com/2016/08/redux-explained-again)

### How to add Redux to your project?

First, initialize a new React application with [Create React App](https://reactjs.org/docs/create-a-new-react-app.html#create-react-app):

```sh
npx create-react-app my-app
```

Then, navigate to your `myReactReduxProject` directory and add Redux Toolkit:

```sh
npm install react-redux @reduxjs/toolkit
```

- [React Redux Toolkit Tutorial for Beginners](https://www.youtube.com/watch?v=u3KlatzB7GM)
- [Redux Toolkit Quick Start](https://redux-toolkit.js.org/tutorials/quick-start)

---

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
