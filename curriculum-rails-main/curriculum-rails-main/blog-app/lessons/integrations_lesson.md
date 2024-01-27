# Integrations specs

## Learning objectives

- Write integration tests with the Capybara gem.

### Estimated time: 1h

## What are integration specs?

Integration specs are used to test user workflows. They are very similar to functional tests, however their primary difference is that they can be used to 'integrate' several controllers to properly test what is being generated in the view. This allows your tests to be written in such a way that they follow the exact same paths your users will and guarantees the content you expect to display, is indeed displayed.

### Why are integration specs important?

Understanding the path that an integration test needs to take is critical in maintaining proper working code and being able to account for possible User interactions. It can not only help identify bugs before a user experiences them, it will also help you create a better user experience as you plan the intended actions your Users should take. While it is certainly useful to test standalone parts of your project, integration tests allow you to also make sure your project is interacting with itself, and user input, the way it should.

#### What is Capybara?

Capybara is a gem that seamlessly integrates with RSpec, and many other testing suites, to provide advanced testing capabilities for your Rails project. Capybara focuses on testing from the front-end back in order to properly simulate User stories by mimicing the actions a user might take.
  
  - Check out [this tutorial](https://www.youtube.com/watch?v=2TInLtG8dj4) for using Capybara with RSpec in Rails 7.
  
  - Check out [this tutorial](https://www.codewithjason.com/rails-testing-hello-world-using-rspec-capybara/) for an example that tests a simple 'Hello World' project using RSpec and Capybara.

## Additional materials 

*These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.*

  - Explore the [Capybara Docs](https://rubydoc.info/github/teamcapybara/capybara) for yourself to quickly search files, methods, and classes within Capybara.

  - Check out the [Capybara Repository](https://github.com/teamcapybara/capybara) to explore the source code.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
