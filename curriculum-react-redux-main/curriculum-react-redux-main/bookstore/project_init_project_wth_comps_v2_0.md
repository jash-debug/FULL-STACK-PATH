# Bookstore: initialize project with components

## Learning objectives

- Use React Router.
- Use React components.

### Estimated time: 3.5h

## Description

This project will lay foundations for your Bookstore website. You will create the **React** part of the app.
You will also set up routing using **React Router**.

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

- Initialise React app.
- The _building blocks_ of your app should be set as re-usable components. Create a directory for your components.
- Add [React Router](https://github.com/remix-run/react-router/blob/dev/examples/basic/src/App.tsx) and set two `<Route>`s and `<Link>`s for the app's navigation:
  - Books - the default view:
    - Should display the list of books (empty at this point but it should be ready for the data) with the Remove button (no funcionality yet).
      - Create a component called Book for displaying a single book (receive a title and an author as prop) and reuse it in a component that displays a list of books.
    - Should display a form for adding a book (no functionality yet).
      - Create a separate component for this form (with inputs for a title and an author [**IMPORTANT** in the design you can see an input for a category - please replace it with an author.]).
  - Categories:
    - Should display a button "Check status" only.
- Styling is not required at this point.

### Need a big picture?

Remind me about [the big picture of this project](./sneak_peek_v2_0.md).

## Work and submission mode

- You should submit this activity **individually**.

## Code review

Follow [these steps](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/code-review/articles/how_to_ask_for_a_code_review.md) to request a code review of your project.

## Submit your project

After the final approval from a code reviewer, you need to submit your project. [Read this FAQ for a reminder on how to submit your project.](https://microverse.zendesk.com/hc/en-us/articles/360061344234)

Now go to your Student Dashboard and submit your project.

---

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
