# Connect React & Redux

## Learning objectives
- Connect React and Redux.

### Estimated time: 2.5h

## Description
Redux is a standalone library. It can be used with vanilla JS applications or with UI frameworks like React, Angular, or Vue. To use Redux with any of these frameworks you need to introduce some "UI binding" to tie Redux and the UI framework together. The most convenient way of binding an application's UI with Redux is to use a dedicated UI binding library. [**React Redux**](https://react-redux.js.org/) is the official Redux UI binding library for React applications. If you are using Redux and React together, you should use **React Redux** to bind these two libraries.

### Why is it important?
The process of subscribing to the store, checking for updates, and triggering a re-render can be handled by the UI binding library and made more accessible and easy to use with its dedicated methods.

Although we said that Redux is a standalone library that can be used with various frameworks it's worth mentioning that it was originally designed and intended for use with React. It's also worth noting that the **React Redux** library is maintained directly by the Redux team.

If you're still not convinced that using **React Redux** library is the best way to connect React and Redux, read [Why use React Redux](https://react-redux.js.org/introduction/why-use-react-redux).

When reading about **React Redux** you might encounter two different API's:

- `Connect` API
- `Hooks` API

`Connect` API is older and used to be the default for React `class` based applications. Since v7.1.0 **React Redux** supports the `Hooks` API. 

The Redux team now recommends using the **React Redux Hooks API** as the default approach in your React components development.

- Read the [official React Redux introduction to Hooks API](https://react-redux.js.org/api/hooks).
- Watch [this video guide ](https://www.youtube.com/watch?v=hc3CSmw3L6I) on how to set up your React Redux application.
- Watch [this video](https://www.youtube.com/watch?v=fn9Y76Naw_U) to learn about two main patterns for structuring Redux code in React applications.

## Additional materials
**These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.**

- Read more about [oficially recommended files and folders structure](https://redux.js.org/style-guide/style-guide#structure-files-as-feature-folders-with-single-file-logic).
- Read more about [the *ducks* pattern](https://github.com/erikras/ducks-modular-redux).

When working with some legacy code or reading about React Redux from a bit older sources you might find many references to the `connect` API and functions like `mapStateToProps` or `mapDispatchToProps`. If you  want to familiarise yourself with the basic concepts of it, check this [basic tutorial on `connect` API](https://react-redux.js.org/tutorials/connect).

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
