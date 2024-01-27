# Bookstore: initialize project with components

## Learning objectives
- Understand the concept of state management.
- Use store, actions and reducers in React.
- Connect React and Redux.

### Estimated time: 3.5h

## Description
This project will lay foundations for your Bookstore website. You will create a **React** and **Redux** app. You will structure your files using the "feature folder" approach. You will also set up routing using **React Router**.

*IMPORTANT NOTE: Read **all** requirements before you start building your project.*

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
- Add React Redux (`npm install react-redux`).
- Structure your application files using a "feature folder" approach and use the [*ducks* pattern](https://github.com/erikras/ducks-modular-redux) for your Redux files. Your files/folder structure could look like this:
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
- The *building blocks* of your app should be set as re-usable components.
- Add [React Router](https://reactrouter.com/web/guides/quick-start) and set two `<Route>`s and `<Link>`s for the app's navigation:
    - Books - the default view
        - Should display the list of books (empty at this point but it should be ready for the data) with the Remove button (no funcionality yet)
            - Create a component called Book for displaying a single book and reuse it in a component that displays a list of books
        - Should have a form for adding a book (no functionality yet)
            - Create a separate component for this form
    - Categories
        - Should display "Under construction" text only.
- Styling is not required at this point.

### Need a big picture? 

Remind me about [the big picture of this project](./sneak_peek.md).

## Work and submission mode

- You should submit this activity **individually.**

## Code review

Follow [these steps](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/code-review/articles/how_to_ask_for_a_code_review.md) to request a code review of your project.

## Submit your project

After the final approval from a code reviewer, you need to submit your project.
[Read this FAQ for a reminder on how to submit your project.](https://microverse.zendesk.com/hc/en-us/articles/360061344234)
Now go to your Student Dashboard and submit your project.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
