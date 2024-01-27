# Redux intro - store, actions, reducers

## Learning objectives
- Understand the concept of state management.
- Use store, actions and reducers in React.
- Use Redux documentation.
- Connect an existing API via Redux and use the data to display something in a UI.

### Estimated time: 1.5h

## Description
So far you've learned about React components that use the concept of *state*. However, it was always a local state that was impacting only a given component. As your application grows you may need to control the state of several components at once or have one global state. For example, you may want to present a different user interface in your components depending on whether the user is signed in or not. Global state management in large applications requires a dedicated system - and that's exactly what Redux offers.

### Why is Redux important?
UI libraries and frameworks like React usually don't offer any data management systems. Most modern applications rely heavily on data, so having a reliable system to control the application's global state and manipulate data is a must. Redux quickly became very popular among JS developers because of its simple yet powerful concepts that bring order and predictability to working with large amounts of data in interactive applications. A great set of dedicated tools makes it an excellent choice for React applications.

To be able to use Redux you need to understand its core concepts: Store, Actions and Reducers.

- Read this introductory article about the [core concepts of Redux](https://redux.js.org/introduction/core-concepts).
- Read [why and when you should use Redux](https://redux.js.org/tutorials/essentials/part-1-overview-concepts#why-should-i-use-redux).
- Watch Dan Abramov, the co-creator of Redux, explaining the concepts of [**Immutable state tree**](https://egghead.io/lessons/react-redux-the-single-immutable-state-tree) and [**Actions**](https://egghead.io/lessons/react-redux-describing-state-changes-with-actions) - the first two principles of Redux.
- Remind yourself what [pure and impure functions](https://egghead.io/lessons/react-redux-pure-and-impure-functions) are to better understand how [**Reducers**](https://egghead.io/lessons/react-redux-the-reducer-function) work and grasp the merit of the third principle of Redux.
- Now go through a summary of all those concepts [by reading the rest of this article](https://redux.js.org/tutorials/essentials/part-1-overview-concepts#redux-terms-and-concepts).

- Next read about the practical aspects of [getting started with Redux](https://redux.js.org/introduction/getting-started) and how to work with it in React applications.

- Finally, take a look at how to [connect your application with external API and work with fetched data using React and Redux](https://medium.com/swlh/quick-guide-for-fetching-api-data-using-react-redux-and-hooks-with-explanation-10503726bc6b).


## Additional materials 
**These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.**

Getting your head around all those new concepts might be daunting. However, the only way to feel more comfortable with it is to learn more and more about it.

- Read [this article](https://www.educative.io/blog/understanding-redux) covering all the basic concepts of Redux from a slightly different perspective.
- Check [this text](https://medium.com/leanjs/introduction-to-redux-redux-explained-with-very-simple-examples-b39d7967ceb8) using an interesting metaphor for covering the Redux state updates.
- Watch one more video from Dan Abramov about [writing reducers for a To-Do app](https://egghead.io/lessons/react-redux-writing-a-todo-list-reducer-adding-a-todo).

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
