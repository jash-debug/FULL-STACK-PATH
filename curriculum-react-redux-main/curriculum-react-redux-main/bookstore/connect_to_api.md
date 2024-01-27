# Bookstore: connect to API

## Learning objectives

- Understand the concept of state management.
- Use store, actions and reducers in React.
- Connect React and Redux.
- Connect an existing API via Redux and use the data to display something in a UI.

### Estimated time: 3.5h

## Description

In this project, you will **connect your React & Redux application to an existing API** to create and remove books from a server.

_Note: Before you start, make sure to read the [Bookstore API documentation](https://www.notion.so/Bookstore-API-51ea269061f849118c65c0a53e88a739) to learn how to use the API._

_IMPORTANT NOTE: Read **all** requirements before you start building your project._

### General requirements

- Make sure that there are [no linter errors](https://github.com/microverseinc/linters-config).
- Make sure that you used correct [Gitflow](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/gitflow.md).
- Make sure that you documented your work [in a professional way](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/documentation/articles/professional_repo_rules.md).

### JavaScript requirements

- Follow our list of [best practices for JavaScript](https://github.com/microverseinc/curriculum-html-css/blob/main/articles/javascript_best_practices.md).

### Project requirements

In the previous project you developed the **add book** and **remove book** features directly in your application. Now you will refactor your code to use the **Bookstore API** to add and remove books.

1. Read the documentation of the [Bookstore API](https://www.notion.so/Bookstore-API-51ea269061f849118c65c0a53e88a739) you will use as a backend
2. Use [`axios`](https://axios-http.com/docs/intro) to make your HTTP requests
3. Create a special action creator using [createAsyncThunk](https://redux-toolkit.js.org/api/createAsyncThunk) called `fetchBooks`, which includes the HTTP request with `axios`
4. Add `fetchBooks` to your the `extraReducers` section of your `booksSlice`, where you will actually update the state
5. Navigate to your `<BookList>` and import `useEffect` (from `react`) and `useDispatch` from `react-redux`
6. Dispatch your `fetchBooks` from inside `useEffect`
7. Render your `books` inside of the `<BookList>` component
8. Refactor your `addBook` and `removeBook` functions with `createAsyncThunk` to include HTTP requests to the Bookstore API

_Note: Everything should work the same as before_

_Note: No styling is required at this stage_

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
<Add any additional instructions you may need or leave blank>

---

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
