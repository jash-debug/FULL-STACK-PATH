# How to setup RoR + React project as two apps

## Learning objectives

- Understand the pros and cons of different approaches of connecting Ruby on Rails back-end with React front-end.

### Estimated time: 1h

## Why is it important?

You already created a simple app that uses both React and Rails. However, the beauty of the distinction between the frontend UI and backend API is that they can be two independent apps.
Thanks to that the maintenance of the project is easier - frontend and backend teams can manage their own repos.
Also, in the future changing the tech stack for either the frontend or backend part is easier.

#### How to set up your project as two apps

In order to set up your project as two apps you basically need to follow these steps:

1. Set up a new Rails app for API as usual.
2. Set up a new React app for UI as usual.
3. Inside the React app use the endpoints exposed by the Rails app.


And this is it! The simplest way to think about it is to imagine that your Rails API will work like any other external API you have used before.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
