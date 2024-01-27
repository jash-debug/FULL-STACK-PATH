# Class components lifecycle

## Learning objectives

- Use React life cycle methods.

### Estimated time: 1h

## Description

In this lesson, you will learn what lifecycle methods of React class-based components are and how to use them.

### Why are lifecycle methods important?

React components have a *lifecycle*, consisting of three phases: mounting, updating, and unmounting. Using them you can control the state and props of your components from start to finish.

### Lifecycle methods

Every phase of the lifecycle of a component has its own methods. Sometimes a method is available in more than one phase.

**1. Mounting** (putting elements in the DOM):

- `constructor()`.
- `getDerivedStateFromProps()`.
- `render()` (mandatory).
- `componentDidMount()`.

**2. Updating** (props or state changes):

- `getDerivedStateFromProps()`. 
- `shouldComponentUpdate()`.
- `render()` (mandatory).
- `getSnapshotBeforeUpdate()`.
- `componentDidUpdate()`.

**3. Unmounting** (element is removed from the DOM):

- `componentWillUnmount()`

**Important notes**:

- Lifecycle methods are called in this order:
- `render()` is the only mandatory method; all others are optional.
- Some methods are more used than others. You will frequently use `componentDidMount()` and `componentDidUpdate()`, so learn them well.

### Example: a lifecycle method in action

Let's see an example of a common scenario: using `componentDidMount()` to load some data from an API, when a component has just been mounted in the DOM.

```javascript
import React, { Component } from 'react';
 
class Todo extends Component {
  constructor(props) {
    super(props);
 
    this.state = {
      todo: null,
    };
  }
 
  componentDidMount() {
    fetch('https://jsonplaceholder.typicode.com/todos/1')
      .then(response => response.json())
      .then(todo => this.setState({ todo }))
  }
 
  ...
}

export default Todo;
```

In this example:

- The `constructor()` method is called first, setting `todo` as `null` in the component's state.
- When the component has finished rendering, `componentDidMount()` makes a *request* to an API, getting some data from the *response*, and setting this data as our `todo` state.

To learn more, read the React guide explanation of [state and lifecycle](https://reactjs.org/docs/state-and-lifecycle.html).

## Additional materials

**These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.**

Read the [React lifecycle](https://www.w3schools.com/react/react_lifecycle.asp) article by W3Schools and play with the examples.

Check this [interactive diagram](https://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/) of lifecycle methods, show and hide the "less common" checkbox.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
