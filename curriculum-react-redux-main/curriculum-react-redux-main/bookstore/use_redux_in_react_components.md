# Bookstore: Use Redux in React components.

## Learning objectives

- Understand the concept of state management.
- Use store, actions and reducers in React.
- Connect React and Redux.

### Estimated time: 3h

## Description

In this step you will **use a Redux store to display books**. You'll implement `react-redux` in order to connect your **store** and then access your **state variables** (accessed through `useSelector`) and **state modifiers** (which will be a combination of a `reducer` and `useDispatch`).

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

- Connect your `store` to the main component of your React app.
- Define a state `slice` which will contain your books
  ```json
  // Initial state:
  [
    {
      "id": "item1",
      "title": "The Great Gatsby",
      "author": "John Smith",
      "category": "Fiction"
    },
    {
      "id": "item2",
      "title": "Anna Karenina",
      "author": "Leo Tolstoy",
      "category": "Fiction"
    },
    {
      "id": "item3",
      "title": "The Selfish Gene",
      "author": "Richard Dawkins",
      "category": "Nonfiction"
    }
  ]
  ```
- Display your `books`, received from the slice, in a reusable component
- Dispatch actions using `useDispatch`
- Add a `<Button>` component, which includes:
  - An event handler that **adds** a book to the `books` array (with attributes _id_, _title_ and _author_)
- Add a `<Button>` component, which includes:
  - An event handler that **removes** a book to the `books` array (by _id_)

### Need a big picture?

Remind me about [the big picture of this project](./sneak_peek_v2_0.md).

## Work and submission mode

- You should submit this activity **individually**.

## Code review

Follow [these steps](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/code-review/articles/how_to_ask_for_a_code_review.md) to request a code review of your project.

## Submit your project

After the final approval from a code reviewer, you need to submit your project.
[Read this FAQ for a reminder on how to submit your project.](https://microverse.zendesk.com/hc/en-us/articles/360061344234)
Now go to your Student Dashboard and submit your project.

# Additional requirements

_These are all optional, but if you're interested in exploring this topic further, feel free to implement them. Any exploration here should be done outside program time._

_If you decide to implement these requirements you should do it in a separate pull request. As always, remember to clearly document your decision in GitHub comments._

- [ ] Implement a **filtering feature**
  - Use hardcoded list of categories
  - Clicking on a category label should:
    - Update the books list
    - Show only the books of a given category

---

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
