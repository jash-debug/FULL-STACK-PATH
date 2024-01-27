# Webpack

## Learning objectives

- Use webpack to bundle JavaScript.

### Estimated time: 1h

## Description
**Webpack** is a static module bundler for modern JavaScript applications. It's intelligent enough to build all app dependencies based just on your file imports. It starts from a list of modules defined as *entry points* and recursively builds a *dependency graph* that includes every module the application needs. 

### Why is webpack important?
Historically, webpack enabled developers to use ES6 modules before any browser implemented support for using them. 
Today webpack also allows for stylesheets and non-code assets, such as images and web fonts, to be used just like module imports thanks to its *dependency graph* and *loaders*. It cares for performance in production and provides a great experience for developers.

- [Understanding the complexity of Modern web dev stack](https://www.youtube.com/watch?v=QliwSwWHJoQ)

To start your adventure with webpack, go through the following crash course:
- [Webpack 5 Crash Course](https://www.youtube.com/watch?v=IZGNcSuwBZs)

In addition, we recommend you to also go through the official documentation. This is important because it will include details on the most recent version (as of today this is webpack v5.8).

- [Getting started with webpack](https://webpack.js.org/guides/getting-started/).
- [Asset management](https://webpack.js.org/guides/asset-management/).
- [Output management](https://webpack.js.org/guides/output-management/).
- [Development](https://webpack.js.org/guides/development/).

## Additional materials
*These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.*
If you'd like to understand better how webpack works, read about the [main webpack concepts](https://webpack.js.org/concepts/).


------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
