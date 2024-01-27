# How to test your controllers

## Learning objectives 

- Write tests for controllers.

### Estimated time: 1 hour

## Description
Let's take a moment to envision what is happening with the controller, in the grand scheme of our app. If we examine its points of entry and exit, we see that from the controller we are connected to the URL routing, the model, and the view. Think about how the controller handles these three connections as you learn more about how to test them.

-  Read [this article](https://www.microverse.org/blog/understanding-rspec-controller-request-specs-integration-test-using-capybara) for a great look into Rails controller testing.

### Why is understanding how to test controllers important? 
Controllers are the backbone of your project as they handle all requests, whether these are coming in from the browser or requesting information from the database.  Simply put, it's important to test controllers properly because of how much they do. They are the central hub of all the project's activity and knowing their tests are written correctly is important to the entire function of the overall app. Not only that, as you learn more about testing you will see that other tests are built around the foundations of controller testing.

#### Writing request specs
A request spec need not be overly complicated and as you will see, does just what the name implies. By sending a request to a URL we can expect the response to either render a view or redirect us. If your controller action redirects the user, and your request spec follows that redirect, it will ultimately still expect some view to be rendered. That's all it takes. At the end of the day, your request spec just want to make sure that your URL route is rendering the correct view.

-  Watch [this video](https://www.youtube.com/watch?v=SG08tPL_RbY) for some examples on how to write a proper request spec.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
