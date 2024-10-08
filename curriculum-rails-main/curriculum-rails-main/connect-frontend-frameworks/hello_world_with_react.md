# Set up a "Hello world" project with rails-react gem

## Learning objectives
- Implement a connection between a Ruby on Rails back-end and React front-end.
- Understand the pros and cons of different approaches of connecting Ruby on Rails back-end with React front-end.

### Estimated time: 2h



## Description

By now you've used many different gems with Rails and this exercise will have you connect previous knowledge with new knowledge as you get a chance to use the `react-rails` gem. This gem allows you to build React components as a part of your Rails JavaScript and serve it in a component, `react_component`, to be used in a regular ERB file.

*IMPORTANT NOTE: Read **all** requirements before you start building your project.*


### General requirements

- Make sure that there are [no linter errors](https://github.com/microverseinc/linters-config).
- Make sure that you used correct [Gitflow](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/gitflow.md).
- Make sure that you documented your work [in a professional way](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/documentation/articles/professional_repo_rules.md).

### Ruby requirements
- Follow our list of [best practices for Ruby](https://github.com/microverseinc/curriculum-ruby/blob/main/articles/ruby_best_practices.md).

NOTE: Use **Rails 6** for this project so that you can follow the guidelines and instructions included in the curriculum. If you need help for installing different versions of Rails, check this [tutorial](https://github.com/sinansevgi/reviewer-experiments/blob/main/specific_rails.md). 

### Project requirements

 - Create a new Rails app called 'hello-rails-react'.
 - Initialize your project with Git.
 - Set up your project with `webpacker` the `react-rails` gems as describe in the previous lesson's tutorial.
 - Make sure that your project has a Postgres database set up. 
 - Create a table for storing your messages and create 5 different greetings. 
 - Create an API endpoint that selects a random greeting from your table (you will need a controller with an action and Rails route).
 - Create a static view that will be the root of your app.


---------

- Create the `App` component with react-router and render it in your static view.
- Create the `Greeting` component that will display a greeting. Set it up as a route in your App component.
- Create a store, an action and a reducer that will connect to you API endpont to get the random greeting.
- Display the random greeting in your `Greeting` component.

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
