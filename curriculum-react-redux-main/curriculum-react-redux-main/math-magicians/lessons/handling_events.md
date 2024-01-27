# Handling events

## Learning objectives

- Handle events in a React app.

### Estimated time: 0.5h

## Description

In this lesson, you will learn **how to work with events** in React.

### Why are events important?

**Events** are a fundamental concept, not only of React but of JavaScript. By listening to them our code can know how to respond to them.

React has inherited the concept of events and they are crucial to understanding how to work with `state` correctly.

- [Introduction to events](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events)

### JavaScript and React events

JavaScript has different kinds of events:

- Browser events (i.e. load, unload, scroll, etc.)
- Mouse events (i.e. click, double click)
- Keyboard events (i.e. key down/up)
- Form events (i.e. submit)
- HTML element events
- CSS events

- [Events - Reference](https://developer.mozilla.org/en-US/docs/Web/Events#event_listing)

React has access to these events, but there are some differences you should know:

| JavaScript                      | React                               |
| ------------------------------- | ----------------------------------- |
| Event names are **lowercase**   | Event names are **camelCase**       |
| Events are called `Events`      | Events are called `SyntheticEvents` |
| Functions are passed as strings | Functions are passed directly       |

For example, a button element with an **onclick event** in regular HTML:

```javascript
<button onclick="activateLasers()">Activate Lasers</button>
```

In React with JSX, becomes:

```javascript
<button onClick={activateLasers}>Activate Lasers</button>
```

### Event handlers

An **event handler** is a function that is executed when any of the aforementioned events happen. Using the `event` object you have access to important data, like the `target` (which element created the event) or the `value` of the element (in case of `<input />` elements).

For example, an input `onChange` event:

```javascript
import React from "react"

function App() {
  const onChangeHandler = (event) => {
    console.log(event.target.value)
  }
  return (
    <div>
      <div>
        Name: <input onChange={onChangeHandler} />
      </div>
      <div>
        Lastname: <input onChange={onChangeHandler} />
      </div>
    </div>
  )
}
```

This example uses the same event handler function (`onChangeHandler`) and passes it as event to two different input elements. When `onChange` is fired, the handler receives the `event` object and takes its value from the `target` (which is different, depending on what input is creating the event). In this way, several elements can reuse the same handler!

## Additional materials

**These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.**

- To learn more about the React events system, read the [Responding to Events](https://beta.reactjs.org/learn/responding-to-events) official guide.
- [How react events are different from Js addEventListeners](https://www.youtube.com/watch?v=pXR86JNulw0)

---

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._