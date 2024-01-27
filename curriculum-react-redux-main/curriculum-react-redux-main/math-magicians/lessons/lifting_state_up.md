# Lifting state up

## Learning objectives

- Understand the mechanism of lifting state up.

### Estimated time: 1h

## Description

In this lesson, you will learn what **lifting state up** is and how it's useful to share state across components.

### Why is lifting state up important?

In the lesson about Props & State, you learned when to use state and when to use props. We said that props are **passed down** from a parent component to its children (which is called [unidirectional data flow](https://www.educative.io/answers/what-is-unidirectional-data-flow-in-react)).

You also learned that components can have **state**, dynamic data that changes its content either because of _user activity_ or _programmatically_.

But what happens **when you need to share state between two or more components**? What happens when you need to pass some data to a component that is not a child, but a _sibling_ (a component at the same hierarchical level)?

This is where **lifting state up** comes in.

### Lifting state up

You need to pass some data to a sibling, but you can't pass it as props, because props can only be passed _down_. If you create the same piece of state in several sibling components, you are duplicating code (and we already learned our code should be _DRY_), then you will need to update it in several places, a process that will produce bugs!

The solution to this problem is **lifting state up**. This means that you should:

1. Remove state from all child components
2. Move it to their closest common parent
3. Pass the state down to them via props

- [Sharing State Between Components](https://beta.reactjs.org/learn/sharing-state-between-components)

### Props and handlers

In React, a prop can be anything: a simple value as a string, number, or boolean, or a more complicated object or array. Props can also be functions!

An **event handler** is a function that is executed when an event is fired. For example, when a button is clicked, a "click" event is fired, etc.

```jsx
function Button() {
  return (
    <button onClick={() => alert("You clicked the button!")}>Click me!</button>
  )
}
```

- [Responding to Events](https://beta.reactjs.org/learn/responding-to-events)

In React you can pass these **event handlers** as props, and children components will be able to execute them. When they are called, they will have access to the data of the children, and it will _bubble up_ to the parent.

This is a common pattern known as "data down, events up" (also known as "actions up").

- [Understanding Information Flow in React: Data Down, Action Up](https://medium.com/swlh/understanding-information-flow-in-react-data-down-action-up-b6c792a8b010)

### Summary

To summarize:

- When lifting state up, you will pass event handler functions from the common parent component to its children as props.
- These handlers will be _declared_ in the parent but _called_ in the children components.
- In the children components you can modify the data and then send it back to the parent, calling the handler received as a prop.
- In that way, the parent component will have access to the data coming from the children.
- Eventually, the parent component can pass it down again.

A good example of lifting state up in action can be found in [this article](https://www.geeksforgeeks.org/lifting-state-up-in-reactjs/).

## Additional materials

**These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.**

- [Lifting state up with REACT ](https://www.youtube.com/watch?v=ahKsy1FS45k)

---

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._