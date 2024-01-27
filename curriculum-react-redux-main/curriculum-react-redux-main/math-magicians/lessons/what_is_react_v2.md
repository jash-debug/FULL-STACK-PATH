# What is React?

## Learning objectives

- Explain what React is.
- Describe what a virtual DOM is.

### Estimated time: 0.75h

## Description

In this lesson you will learn what `React.js` is, what the `virtual DOM` is, how React uses the virtual DOM, and why React is so popular.

### Why is React important?

[React.js](https://reactjs.org/) is a front-end library introduced by Facebook in 2013 and it has become one of the most popular ways to build modern user interfaces today.

- [React in 100 seconds](https://www.youtube.com/watch?v=Tn6-PIqc4UM)
- [The Story of React](https://www.youtube.com/watch?v=Wm_xI7KntDs)

### React core concepts

In order to fully understand how to build frontend web applications with React, you need to understand a few core concepts:

- **Build tools**
  When building React applications, you'll use features that browsers can't understand. The solution to this is to use a [build tool](https://www.youtube.com/watch?v=V5qvWl-O-zE), which will resolve these issues.

  That said, it is possible to [use React directly in your HTML](https://reactjs.org/docs/add-react-to-a-website.html). However, in order to build complex web applications, you need to use proper build tools that allows for **module bundling** and **transpilation**.

- **Virtual DOM**.
  React manipulates the Document-Object Model (DOM), but DOM manipulation is slow. To solve this problem, React uses a [virtual DOM](https://www.youtube.com/watch?v=rysTbzKOEO0), which is a representation (in memory) of the real DOM. React keeps track of the changes in the virtual DOM and updates the actual DOM only as needed, making it really fast.

- **Components**
  Components are **self-contained units that define a portion of a user interfaces**. They are simple JavaScript functions that returns **JSX**, a HTML-like syntax.

- **State**
  State is an object that stores a component's **dynamic data** and determines how a component renders and behaves. By listening to **user events**, the data in the component changes.

- **Props**
  Props in are **data passed from a parent component to a child component** through **customly defined attributes** placed on component instances.

In the following lessons you go deeper into these and other, related concepts.

## Additional materials

_These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time._

- [Official documentation](https://reactjs.org/)
- [A Brief History of Frontend Frameworks](https://www.youtube.com/watch?v=Kzeog8yTFaE)

---

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
