# Testing React with React Testing Library

## What is React Testing Library?

Let's look at the main characteristics of React Testing Library (RTL):

- It's included and set up in Create React App.
- Is NOT a test runner, so you need to use it in conjunction with Jest (or another test runner).
- It's the React specific implementation of [DOM Testing Library](https://testing-library.com/docs/dom-testing-library/intro).
- Its primary guiding principle is: *The more your tests resemble the way your software is used, the more confidence they can give you.*

So, as the guiding principle says, you should write your tests in a way that resembles how your app will be used. RTL is mainly used to test user interaction with your components (like clicking a button), to test other actions that are not necessarily triggered by a user (like fetching data), and to check that elements are rendered in the browser.

For example, CRA includes a default test using RTL:

```javascript
import { render, screen } from '@testing-library/react';
import App from './App';

test('renders learn react link', () => {
  render(<App />);
  const linkElement = screen.getByText(/learn react/i);
  expect(linkElement).toBeInTheDocument();
});
```

This example introduces some of the main elements of RTL:

- The *render()* method, used to render React components.
- The `screen` object, used to access DOM elements.
- The `getByText()` method, used to select an element in the DOM, matching the text provided.

To learn how to use RTL, read the [Getting started](https://testing-library.com/docs/) guide.
To check the full list of methods (also called *queries*), see the [Queries](https://testing-library.com/docs/queries/about) section.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
