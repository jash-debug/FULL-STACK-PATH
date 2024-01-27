# Redux - immutability

## Learning objectives

- Use immutable state in Redux store.

### Estimated time: 0.5h

## Description

Redux has been designed with **immutability** in mind.

In this lesson, you will learn what it means in a general sense, how it's applied in JavaScript and what is means in the context of Redux.

### Why is it important?

In order to use Redux effectively, it's important to know the way it updates state. The creators of Redux have chosen to **make immutability a requirement** in the design of Redux logic.

By learning what immutability is and how it applies to JavaScript, you will get a deeper understanding of the mechanics of Redux.

### What is immutability?

In computer science, **immutability** refers to the property of _an object or data structure that cannot be altered or modified after it has been created_.

This is a useful thing to do, as it ensures that **data structures do not change unexpectedly**, making it easier to reason about the behavior of code, and improving performance in some cases.

- [Immutability - Computerphile](https://www.youtube.com/watch?v=8Sf6ToPNiA4)

### Immutability in JavaScript & React

In JavaScript, **immutability** can be achieved in several ways, including:

- Using `const` instead of let or var when declaring a variable, which makes the variable reference immutable.

- Using `Object.freeze()` method, which makes the object and all of its properties read-only.

- Using `Object.assign()` and spreading `...` operators to create new objects or arrays, while leaving the original objects or arrays unchanged.

- [Immutability in JavaScript](https://www.telerik.com/blogs/immutability-in-javascript).
- [Pros and Cons of using immutability with React.js](https://reactkungfu.com/2015/08/pros-and-cons-of-using-immutability-with-react-js/)

### Immutability in Redux

In Redux, **immutability** refers to the idea that _the state of the application should never be directly modified_, but instead should **always create a new state that is a modified copy of the original state**.

This is achieved by **creating new state objects whenever a change is made**, rather than mutating the existing state.

- [React Redux Update State Immutable way](https://www.youtube.com/watch?v=Lt4P9BKOPfI)

---

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._