# Bookstore: add reducers and actions

## Learning objectives

- Understand the concept of state management.
- Use store, actions, and reducers in React.

### Estimated time: 2h

## Description

In this step, you will implement [Redux Toolkit](https://redux-toolkit.js.org/) inside of a React application. You will:

- Setup a Redux store
- Create a slice to save your state and reducers

_IMPORTANT NOTE: Read **all** requirements before you start building your project._

### General requirements

- Make sure that there are [no linter errors](https://github.com/microverseinc/linters-config).
- Make sure that you used correct flow [Gitflow](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/gitflow.md).
- Make sure that you documented your work [in a professional way](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/documentation/articles/professional_repo_rules.md).

### HTML/CSS requirements

- Follow our list of the [best practices for HTML & CSS](https://github.com/microverseinc/curriculum-html-css/blob/main/articles/html_css_best_practices.md).

### JavaScript requirements

- Follow our list of [best practices for JavaScript](https://github.com/microverseinc/curriculum-html-css/blob/main/articles/javascript_best_practices.md).

### Project requirements

- Add Redux Toolkit (`npm install react-redux @reduxjs/toolkit`).
- Create a directory that will contain all your Redux logic (`/src/redux`)
- Configure a Redux store (`/src/redux/store.js`)
- Define a `slice` of state for `books` that:
   - Includes an **array of books** (initial state: empty array)
   - Includes a **reducer that adds a book**
   - Includes a **reducer that removes a book**
- Define a `slice` of state for `categories` that:
   - Includes an **array of categories** (initial state: empty array)
   - Includes a **reducer that checks the status** and always returns "Under construction" (the initial state should check to that string)
- Structure your application files using a "feature folder" approach and use the [ducks pattern](https://github.com/erikras/ducks-modular-redux) for your Redux files. Your files/folder structure could look like this:
   ```sh
   /src
       |---/components
       |---/redux
           |--- /books
                   | booksSlice.js
           |--- /categories
                   | categoriesSlice.js
           | store.js
       | index.js
   ```

**NOTE: No changes in React components are required in this project.**

### Need a big picture?

Remind me about [the big picture of this project](./sneak_peek_v2_0.md).

## Work and submission mode

- You should submit this activity **individually**.

## Code review

Follow [these steps](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/code-review/articles/how_to_ask_for_a_code_review.md) to request a code review of your project.

## Submit your project

After the final approval from a code reviewer, you need to submit your project. [Read this FAQ for a reminder on how to submit your project.](https://microverse.zendesk.com/hc/en-us/articles/360061344234)

Now go to your Student Dashboard and submit your project.

# Additional requirements

_These are all optional, but if you're interested in exploring this topic further, feel free to implement them. Any exploration here should be done outside program time._

_If you decide to implement these requirements you should do it in a separate pull request. As always, remember to clearly document your decision in GitHub comments._

- Implement a **filtering feature**:
  - Includes a (hardcoded) list of categories
  - Clicking on a category label should (1) **update the books list** and (2) **show only the books of a given category**.

---

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
