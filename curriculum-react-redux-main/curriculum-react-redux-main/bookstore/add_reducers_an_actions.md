# Bookstore: add reducers and actions

## Learning objectives

- Understand the concept of state management.
- Use store, actions, and reducers in React.

### Estimated time: 2h

## Description

In this step, you will configure your Redux Store and write _actions_ and _reducer_ for adding and removing books.
NOTE: editing an existing book and updating the progress is not part of this step. Neither is the styling of the application's components but **adding and removing actions need to be implemented.**

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

- Add Redux Toolkit(`npm install react-redux @reduxjs/toolkit`).
- Structure your application files using a "feature folder" approach and use the [_ducks_ pattern](https://github.com/erikras/ducks-modular-redux) for your Redux files. Your files/folder structure could look like this:
  ```
  ...
  /src
      |---/components
      |---/redux
          |--- /books
                  | books.js
          |--- /categories
                  | categories.js
          | configureStore.js
      | index.js
  ```
- Write your book's actions and reducer (in `/src/redux/books/books.js`) using the [_ducks_ pattern](https://github.com/erikras/ducks-modular-redux).
  - Define _action types_ for adding and removing a book.
  - Set the initial state to be an empty array of books.
  - Export _Action Creators_ for your _actions_.
  - Write your reducer and export it as default.
    - Define state changes for the actions that you created.
    - In case of unknown action - return the current state.
- Write your categories actions and reducer (in `/src/redux/categories/categories.js`) using the [_ducks_ pattern](https://github.com/erikras/ducks-modular-redux).

  - Define an _action type_ for checking the status.
  - Set the initial state to be an empty array of categories.
  - Export _Action Creators_ for your _actions_.
  - Write your reducer and export it as default.
    - For the check status action return a string "Under construction".
    - In case of unknown action - return the current state.

- Configure the Redux Store (`/src/redux/configureStore.js`):
  - Importing the necessary methods from Redux Toolkit.
  - Combine both reducers into a root reducer by using `configureStore` function.

### Need a big picture?

1. Add Redux Toolkit (`npm install react-redux @reduxjs/toolkit`).
2. Create a directory that will contain all your Redux logic (`/src/redux`)
3. Configure a Redux store (`/src/redux/store.js`):
4. Define a `slice` of state for `books` that:
   - Includes an **array of books** (initial state: empty array)
   - Includes a **reducer that adds a book**
   - Includes a **reducer that removes a book**
5. Define a `slice` of state for `categories` that:
   - Includes an **array of categories** (initial state: empty array)
   - Includes a **reducer that adds a book**
   - Includes a **reducer that removes a book**
6. Structure your application files using a "feature folder" approach and use the [ducks pattern](https://github.com/erikras/ducks-modular-redux) for your Redux files. Your files/folder structure could look like this:
   ```sh
   /src
       |---/components
       |---/redux
           |--- /books
                   | books.js
           |--- /categories
                   | categories.js
           | store.js
       | index.js
   ```

### Need a big picture?

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
