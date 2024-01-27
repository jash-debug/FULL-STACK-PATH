# Testing

## Learning objectives

- Write unit tests with React Testing Library.
- Write unit tests with snapshots with Jest.

### Estimated time: 1h

## Description

In this lesson, you will learn how to test a React application using the most popular testing libraries.

### Why is testing important?

Testing your applications is very important because it helps you find bugs, detect when something changes inadvertently , make your apps more secure, and in general it increases the overall quality of a software system.

### Testing React

Testing is a very broad topic because there are many different kinds of tests, methodologies, and tools. The kind of tests you will use depends on the project, tools, and workflow of your current project. For example, there are *unit* tests, *integration* tests, *end-to-end* tests, *smoke* tests, *acceptance* tests, *functional* tests, etc. In React, the most common type of test you are going to write is *unit tests*.

### What are unit tests?

They are called *unit tests* because they are written as a *unit*, without external dependencies. When writing unit tests, you will test your functions or components in an encapsulated and isolated way so that you can be sure that they do what they are supposed to do, and nothing else. For unit tests you shouldn't care about how they relate with other parts of the system.

### Testing libraries for React

There are a lot of libraries you can use to test JavaScript and React. In this lesson, we are going to focus on just 2 of them: **Jest** and **React Testing Library**, since they are officially recommended by React. To learn how to to use them read the following articles:

- [Testing React with Jest](../articles/testing_react_with_jest.md).
- [Testing React with React Testing Library](../articles/testing_react_with_react_testing_library.md).

## Additional materials

**These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.**

In this lesson, we have just learned about unit tests and 2 libraries: Jest and React Testing Library. But there are a lot more libraries you can use to test React applications. To learn about other libraries, read the article [11 Tools and libraries for testing in React](https://blog.bitsrc.io/7-react-testing-libraries-you-should-know-b20ca97422a4).

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
