# Set up a "Hello world" project with two apps

## Learning objectives
- Implement a connection between a Ruby on Rails back-end and React front-end.
- Understand pros and cons of different approaches of connecting Ruby on Rails back-end with React front-end.


### Estimated time: 2h

## Description

Now that you're familiar with Rails and React, it's time to put them together in a new kind of 'Hello World!' app. This exercise is going to have you create a React front-end with a Rails back-end and connect them to display a random message.

*IMPORTANT NOTE: Read **all** requirements before you start building your project.*


### General requirements

- Make sure that there are [no linter errors](https://github.com/microverseinc/linters-config). **Note for rails api projects without any styling files, delete the stylint configuration in the linter.yml file (line 23 -36) to avoid errors**
- Make sure that you used correct [Gitflow](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/gitflow.md).
- Make sure that you documented your work [in a professional way](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/documentation/articles/professional_repo_rules.md).

### Ruby requirements
- Follow our list of [best practices for Ruby](https://github.com/microverseinc/curriculum-ruby/blob/main/articles/ruby_best_practices.md).

### Project requirements



 - Create a new Rails API app called 'hello-rails-back-end'.
 - Initialize your project with Git.
 - Make sure that your project has a Postgres database set up. 
 - Create a table for storing your messages and create 5 different greetings. 
 - Create an API endpoint that selects a random greeting from your table (you will need a controller with an action and rails route).

---------

- Create a new React app called 'hello-react-front-end'
- Initialize your project with Git.
- Create the `App` component with react-router.
- Create the `Greeting` component that will display a greeting. Set it up as a route in your App component.
- Create a store, an action and a reducer that will connect to you API endpont to get the random greeting.
- Display the random greeting in your `Greeting` component.

------

- In the README file for the Rails API, add a link to your React app.
- Also, in the README file for the React app, add a link to your Rails API.
- When submitting for a review - use a link to the pull request in your Rails API.
- In the repo for the frontend part - include a PR with changes.

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
