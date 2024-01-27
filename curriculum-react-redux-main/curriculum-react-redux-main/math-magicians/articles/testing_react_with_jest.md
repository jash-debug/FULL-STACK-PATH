# Testing React with Jest

## What is Jest?

Let's look at the main characteristics of Jest:

- Jest is a JavaScript testing framework developed by Facebook, just like React (and because of that they both are fully integrated).
- You can use Jest to test vanilla JS or React.
- It's included and set up in Create React App.
- Jest is a *test runner* and an *assertion library*, at the same time.
  - A test runner is a library that takes care of *running* your tests. Jest will look for all the files matching a pattern (commonly the filename ending in `.test.js`) and execute them.
  - An assertion library is a set of methods you can use to *test* your assertions (or expectations). For example, this *should be* a number, this *should be equal* to 10, this *should not be* a number, etc.
- You can integrate Jest with other libraries.
  - You will still use Jest as the test runner, but you can import and use other assertion libraries.
- One of the main features of Jest is *snapshot testing*, which is a way to check that the UI doesn't change unexpectedly (because another developer has changed it, a library has been updated with breaking changes, or as a *side effect*).

Let's see a basic example of a unit test written in Jest: testing a sum function (vanilla JS).

Given a function `sum` in `sum.js`:

```javascript
function sum(a, b) {
  return a + b;
}
module.exports = sum; // You should export your file
```

And a test file in `sum.test.js`:

```javascript
const sum = require('./sum'); // You need to import the file you want to test

test('adds 1 + 2 to equal 3', () => {
  expect(sum(1, 2)).toBe(3);
});
```

Look at the methods `test()`, `expect()`, and `toBe()`. This is Jest in action:

- You should wrap every test inside a `test()`, and provide 2 arguments, a description of the test, and a callback function.
- Inside the callback function, you will use the `expect()` method in conjunction with *matchers*, like `toBe()`.

Now let's see how to test React components using snapshots (Jest official example):

```javascript
import React from 'react';
import renderer from 'react-test-renderer';
import Link from '../Link.react';

it('renders correctly', () => {
  const tree = renderer
    .create(<Link page="http://www.facebook.com">Facebook</Link>)
    .toJSON();
  expect(tree).toMatchSnapshot();
});
```

- This test uses `it`() instead of `test()`, they are interchangeable.
- `react-test-renderer` is another library you can use to "render" React components outside of a browser. You can check more details [here](https://reactjs.org/docs/test-renderer.html), but we are going to use React Testing Library instead.
- `toMatchSnapshot()` compares that the snapshot (a text representation of the component) matches with the previous one, or creates a new snapshot if it's the first time the test is run.

## How to run tests with Jest?

Since Jest is already set up in CRA, you just have to run the following command:

```bash
npm run test
```

To learn how to use Jest, read the following guides:

- A general introduction: [Getting started](https://jestjs.io/docs/getting-started).
- To see the full list of *matchers*, consult the [Expect API documentation](https://jestjs.io/docs/expect).
- To learn how to work with snapshots, read [Snapshot testing](https://jestjs.io/docs/snapshot-testing).

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
