# Styling

## Learning objectives

- Use styles in a React app.

### Estimated time: 1h

## Description

In this lesson, you will learn the different ways to add styles to a React application.

### Why is styling important?

Adding styles to any application is fundamental because it defines the look and feel of your application and gives users a sense of professionalism depending on the quality of your design. It's also fundamental to providing a nice user experience that is predictable and consistent.

As you already know, JSX allows us to use CSS inside JavaScript, giving us a lot of flexibility in the way we work, in the tools, and the different approaches or methodologies we have available. There are several ways you can add styles in React, with these being the most popular:

### React basic styling

There are 3 ways to add basic styles to your React applications: inline styles, importing CSS, and importing pre-processed CSS files. To learn about them, read the article [React basic styling](../articles/react_basic_styling.md).

### CSS modules

[CSS modules](https://github.com/css-modules/css-modules) is a project that is getting very popular and CRA also supports it by default. In CSS modules your styles are *scoped locally*. This means that every file has access to a set of styles, there are not global styles, and it avoids *collisions* and *pollution* in the global scope (a common problem with CSS). In React all imported CSS rules are globally scoped and available everywhere in the app. However with the use of CSS modules, styles can be locally scoped and made available only to a single component. Thanks to that every component has access to a specific set of styles and these styles. CSS modules is out of the scope of this lesson, but if you are interested, you can check it out as an extra activity in your free time.

### Styled components

[Styled components](https://styled-components.com/) is another of the most popular projects in the React community. It allows you to write styles as React components! But styled components is also out of scope of this lesson, if you want to know more you should check the website's project.

## Additional materials

**These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.**

- In this lesson we have concentrated mainly on the CSS options you have available in CRA. If you want to learn more about CRA CSS support and how to customize it, read the [CRA documentation](https://create-react-app.dev/docs/getting-started), especially the section *Styles and Assets*.

- The different techniques of using CSS inside JS are known generically as *CSS in JS*. This is a rapidly changing area, where new tools and approaches are always emerging. To get familiar with the current techniques, you can read the article: [An introduction to CSS-in-JS: examples, pros, and cons](https://webdesign.tutsplus.com/articles/an-introduction-to-css-in-js-examples-pros-and-cons--cms-33574).

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
