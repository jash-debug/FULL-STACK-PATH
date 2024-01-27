# Bookstore: create and remove books

## Learning objectives
- Understand the concept of state management.
- Use store, actions and reducers in React.
- Connect React and Redux.

### Estimated time: 5h

## Description
In this step you will configure your Redux Store and write *actions* and *reducer* for adding and removing books.  You will also add some UI elements to your components and make them *dispatch* actions.
NOTE: editing an existing book and updating the progress is not part of this step. Neither is the styling of the application's components.

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
- Let's start by configuring the Redux Store (`/src/redux/configureStore.js`) and importing the necessary methods from Redux:
    - Import `createStore`
    - Import `combineReducers` - We will only write a reducer for 'books' in this step, but in the future, we might want to add 'categories' or other reducers as well. 
    - Import `applyMiddleware` - To use some handy Redux middleware, like *redux logger*. It's optional, but it will help you a lot in the development process. To install it, you'll need to run:
    ```
    npm i --save redux-logger
    ```
    
    - Import your `booksReducer`, which you are going to write in `/src/redux/books` directory.

    Your `configureStore.js` file could look like this:
    ```javascript
    // configureStore.js 

    import {createStore, combineReducers, applyMiddleware} from 'redux';
    import logger from 'redux-logger';
    import booksReducer from './books/books';

    const reducer = combineReducers({
        booksReducer
        // additional reducers could be added here
    });

    const store = createStore(
        reducer,
        applyMiddleware(logger)
    );

    export default store;
    ```
    
- Write your book's actions and reducer (in `/src/redux/books/books.js`) using the [*ducks* pattern](https://github.com/erikras/ducks-modular-redux). 
    - Define *action types*:
    ```javascript
    // books.js

    const ADD_BOOK = 'bookStore/books/ADD_BOOK';
    const REMOVE_BOOK = 'bookStore/books/REMOVE_BOOK';
    ```
    - Set initial state to be an empty array of books:
    ```javascript
    // books.js
    ...
    const initialState = [];
    ```
    - Export your *Action Creators* (functions, which return *actions*):
    ```javascript
    // books.js
    ...
    export const addBook = payload => ({
        type: ADD_BOOK,
        payload
    })
    export const removeBook = ...
    ```
    - Write your reducer and export it as default:
    ```javascript
    // books.js
    ...
    const reducer =  (state = initialState, action) => {
    switch (action.type) {
        case ADD_BOOK:
            /*
            return a new state object in which the books array will contain a new book object, passed by action.payload.
            Remember -  you MUSN'T mutate the state. You have to return a new state object - i.e.:
            return [ ...state, action.payload];
            */
        case REMOVE_BOOK:
            /*
            use ES6 filter() method to create a new array, which will not contain the book you want to remove from the store (filter by the id key - i.e.: 
            return state.filter(book => book.id !== id);
            */

        default:
            return state;
        }
    };

    export default reducer;
    ```

- In your React component responsible for adding new books set the data inputs in the local React state (set *title* and *author*  - NOTE: *categories* and *comments* are NOT part of this step). Once your new book object is ready to be submitted to Redux store, dispatch a corresponding action, i.e.:
    ```javascript
    // React component
    ...
    // import useDispatch hook
    import { useDispatch } from 'react-redux';
    // import your Action Creators
    import {addBook, removeBook} from './redux/books/books';

    const dispatch = useDispatch();

    ...

    const submitBookToStore = () => {
        const newBook = {
            id, // make sure it's unique
            title,
            author
        }

        // dispatch an action and pass it the newBook object (your action's payload)
        dispatch(addBook(newBook));
    }

    ...
    
    <button onClick={submitBookToStore}>Add Book</button>

    ```
- In your React component responsible for removing books - implement that even by dispatching a corresponding action.
- Use the *redux-logger* to check if your application is working correctly - Open your browser's console and look for the logger messages. Upon every action dispatch, the logger will print:
    - **prev state** - the state of the whole Redux store before the current action was dispatched.
    - **action** - the action object that is being dispatched.
    - **next state** - the state of the Redux store after the current action was dispatched.

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

# Additional requirements

*These are all optional, but if you're interested in exploring this topic further, feel free to implement them. Any exploration here should be done outside program time.*

*If you decide to implement these requirements you should do it in a separate pull request. As always, remember to clearly document your decision in GitHub comments.*

- Implement a filtering feature with a hardcoded list of categories. Clicking on a category label should update the books list and show only the books of a given category.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
