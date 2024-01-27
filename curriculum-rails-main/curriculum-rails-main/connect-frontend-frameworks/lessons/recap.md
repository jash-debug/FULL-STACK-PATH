# Read a recap of Ruby on Rails, React & Redux frameworks 

## Learning objectives

- Understand principles of Ruby on Rails and React frameworks.

### Estimated time: 1h

## Why is understanding Ruby on Rails, React, & Redux important?
Because they are very popular frameworks, you will find plenty of opportunities in the world for using them. Even if you don't use these exact technologies, the fundamentals learned with these frameworks are applicable across nearly every aspect of development. The MVC pattern is one of the most common you will find, the principles of OOP used in Ruby are an aspect of many other important programming languages, and the overall skills you can develop in gaining a better grasp of these frameworks will serve you in your career in many ways. React has been a popular framework ever since its release and there is a library available for nearly anything you can imagine, not to mention it's built on JavaScript so using it allows you to hone a skill that will be useful nearly everywhere in web development. Even though it may seem like these frameworks are competing technologies, they are still very good at interacting with each other - React can even be integrated into a Rails project! And using both will ensure your knowledge of Ruby and JavaScript are fresh and continuously improving.

#### Ruby on Rails
Ruby on Rails uses a very clear-cut MVC pattern, going as far as to even name the coordinating folders as models, views, and controllers. Everything in RoR, including RoR itself, is a gem (or library), and adding more to your project is simple. Just be careful to only use those gems that are well maintained! While RoR comes out of the box with SQLite3, PostgreSQL is a more common production database, and if you decide to switch be sure to reflect this change in the database.yml file.  The routes file, in your config folder, generates the URLs available in your project and links them to whatever controller action you wish. Database queries can be called in your controller actions to offer CRUD operations through endpoints and views. Naming the folders inside the views folder to match your controller actions will auto-magically connect your views to the correct actions. A model represents a single record instance, so it will be singularly named, while a controller handles all the records so its name will be pluralized.

- Refer back to [this lesson](https://github.com/microverseinc/curriculum-rails/blob/main/blog-app/lessons/MVC_lesson.md) for a quick review of the MVC pattern.

#### React
React, being a JavaScript front-end framework, is extremely versatile and can be used to accomplish nearly anything you need in front-end web development. It speeds up front-end processing by maintaining a representation of the DOM in memory, called the virtual DOM, and using it to track changes so that it can update the actual DOM only when necessary. While some projects may require very little setup for React to work inside them, as a standalone framework it is very common to need Node, Webpack, and Babel in order to correctly compile your code into proper HTML and JS. Passing props (variables that are passed into your components) to React makes it very easy to create modular components that can be reused in all sorts of projects, and React hooks give you access to all sorts of things like local state and path history.

- Refer back to [this lesson](https://github.com/microverseinc/curriculum-react-redux/blob/main/math-magicians/lessons/what_is_react.md) for a quick review of React.

#### Redux
Redux handles the closest thing React has to a database and as such, can be referred to as a state management tool. While React is capable of handling a local state, individual to each component, Redux is able to handle a global state and pass that data between components. There are still limitations though, as this state is only available until the page refreshes. To accomplish this, Redux makes use of three important principles. The first principle is an immutable state tree. This is another way of referring to the state and can be thought of as a snapshot of all your data. As a snapshot, the state tree is read-only and can not be altered directly, which brings us to the second key principle of Redux: actions. By dispatching an action, the Redux store is told exactly how to change the current state. For example, an action might be to simply increment or decrement a value and can be dispatched in response to a click event. When this action fires it sends a message in a way that allows Redux to know how to change the values in your state by using the third principle of Redux: reducers. Reducers are pure functions that take the previous state of your app, accept the action, use those instructions to change a copy of your state, and output a brand new state. This can be a slow process when dealing with a lot of data so be careful how much you store in your Redux state tree!

- Refer back to [this lesson](https://github.com/microverseinc/curriculum-react-redux/blob/main/bookstore/lessons/lesson_redux_intro-store_actions_reducers.md) for a quick review of Redux.

- Be sure to refresh your knowledge of the difference between pure and impure functions by reading [this article](https://dev.to/sanspanic/pure-vs-impure-functions-50aj).

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
