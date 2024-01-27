# JSX

## Learning objectives

- Explain what JSX is.

### Estimated time: 0.25h

## Description

In this lesson, you will learn what **JSX** is and how to use it in React.

### Why is JSX important?

**JSX** is a _HTML-like syntax_ that allows you to write HTML and CSS **inside JavaScript**. It allows you to write HTML and CSS within the same file as your React code.

### JSX

In the past, web development best practices taught us that HTML, CSS, and JavaScript should be **separated**, every one in its own file and doing different things, with a unique **scope** and **responsibility**: this is the design principle of [separation of concerns](https://www.youtube.com/watch?v=eZNG7igXujs).

Well, things have changed in the last years. Modern JavaScript tools, like [Webpack](https://webpack.js.org/) and [Babel](https://babeljs.io/), now allow you to write HTML, CSS, and JavaScript together! And in React, this is the preferred way of building frontend web applications.

Here's how it looks:

```jsx
const myHtml = (
  <div>
    <h1>My title</h1>
    <p>
      I'm a paragraph, <span>and I'm a span</span>
    </p>
  </div>
)
```

Doesn't very different from regular HTML, right? Behind the scenes, however, React, Webpack, and Babel convert that code to this:

```javascript
"use strict"

const myHtml = React.createElement(
  "div",
  null,
  React.createElement("h1", null, "My title"),
  React.createElement(
    "p",
    null,
    "I'm a paragraph, ",
    React.createElement("span", null, "and I'm a span")
  )
)
```

As you can imagine, writing code like this is much more complicated. So JSX is a better alternative!

## Additional materials

**These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.**

For a deeper explanation of how JSX works and its advanced features, read the following guides:

- [JSX in depth](https://reactjs.org/docs/jsx-in-depth.html).
- [What the heck is JSX and why you should use it to build your React apps](https://www.freecodecamp.org/news/what-the-heck-is-jsx-and-why-you-should-use-it-to-build-your-react-apps-1195cbd9dbc6/).

---

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
