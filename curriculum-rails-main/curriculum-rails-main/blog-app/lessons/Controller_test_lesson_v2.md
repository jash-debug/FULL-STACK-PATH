# How to test your controllers

## Learning objectives

- Write tests for controllers.

### Estimated time: 1 hour

## Description
Let's take a moment to envision what is happening with the controller, in the grand scheme of our app. If we examine its points of entry and exit, we see that from the controller we are connected to the URL routing, the model, and the view. Think about how the controller handles these three connections as you learn more about how to test them.

### Why is understanding how to test controllers important?
Controllers are the backbone of your project, as they handle all requests, whether these are coming in from the browser or requesting information from the database.  Simply put, it's important to test controllers properly because of how much they do. They are the central hub of all the project's activity, and knowing their tests are written correctly is important to the entire function of the overall app. Not only that, but as you learn more about testing, you will see that other tests are built around the foundations of controller testing.

#### Writing request specs
A request spec need not be overly complicated and, as you will see, does just what the name implies. By sending a request to a URL, we can then expect certain things from the response: a specific HTTP status code, a redirect, text in the response body, a flash message, etc. At the end of the day, your request spec just wants to make sure that your URL route is giving back the correct response.

- Take a look at this article: ["Request specs"](./articles/request_specs.md)
- The Rails guide has a section on ["Functional tests for your controllers"](https://guides.rubyonrails.org/testing.html#functional-tests-for-your-controllers) which you should read, but keep in mind that they are using a different test framework so you can't just copy and paste things, but the ideas are what matter.
- Follow along with this [written tutorial](https://rubyyagi.com/rspec-request-spec/). You will create a Rails app with API mode (no UI) and write request specs to test the API endpoints.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
