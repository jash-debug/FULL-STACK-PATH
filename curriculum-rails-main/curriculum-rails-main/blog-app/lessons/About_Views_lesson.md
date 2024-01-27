# Learn about views 

## Learning objectives

- Use preprocessed HTML file with embedded Ruby code.
- Use layouts and templates for shared content.

### Estimated time: 1.5h

## Description
The view in Rails takes us all the way full circle back to the very beginning of web development with HTML. You can write out your entire HTML file as you normally would and Rails would do nothing different to it at all. However, with the addition of ERB, we now have the ability to create more dynamic HTML layouts and our HTML goes from being a static page to a dynamic template!

### Why is understanding views important?
Properly understanding Rails views is a powerful way to create a dynamic user experience while saving a lot of time. The best practices that are kept when working with other such files will be equally important here as we work to keep our HTML semantic by choosing the right elements, to keep it DRY by reusing code whenever possible, and of course, we don't want logic here. However, because the Rails view doesn't necessarily have to use anything but HTML it can be really easy to give ourselves extra work.

### What is ERB?
ERB stands for Embedded Ruby but it is just HTML that gets to use a new type of element: Ruby elements. By processing an ERB file we can now go from putting this in the view:
`<h1>Hello World!</h1>`
to putting this in the controller:
`@greetings = 'Hello World!'`
and getting to put this in the view:
`<h1><%= @greetings %></h1>`

- Read [this section](https://guides.rubyonrails.org/action_view_overview.html#erb) of the Rails guides to learn more about the different ERB tags.

### Routing controller actions to views
Don't forget to be mindful of naming conventions when creating your view files! Although it is always possible to create custom views that don't follow naming conventions, following these conventions allows Rails to do a lot of the work for you.

- Read [this section](https://guides.rubyonrails.org/action_view_overview.html#using-action-view-with-rails) of the Rails guides to see the standard views that go with a controller.

### Using layouts
Setting layouts can save you a lot of time, especially if you need to set different `meta` tags in your `head` element. Rails comes with a standard layout called `application.html.erb` which, because of naming conventions, is automatically chosen for the application controller and all controllers that inherit from it.

- Check out [this guide](https://www.tutorialspoint.com/ruby-on-rails/rails-layouts.htm) to see how to work with Rails layouts.

### Using partials
Partials are arguably one of the most powerful aspects of the Rails view. By naming an ERB with an underscore in front of the file name we are able to call upon it with the `render` method and pass variables to it. Not only do partials help us organize our code into more readable chunks, for example by putting the header and footer in their own separate partials, but it also helps us keep things DRY such as when we need the same form in more than one view.

- Read [section 3](https://guides.rubyonrails.org/action_view_overview.html#partials) of the Rails guide on partials but when you reach section 3.2.4 you can stop for now.

## Additional materials

*These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.*

- Read [this article](https://medium.com/@acushla4real/rails-view-helpers-best-practices-guide-d7d7b6db3db4) to see some ways to clean up your views!
- Read [section 2.2.14](https://guides.rubyonrails.org/layouts_and_rendering.html#finding-layouts) of the Rails guides to see how Rails finds the right layout to use.
- Read [section 2.2.14.1](https://guides.rubyonrails.org/layouts_and_rendering.html#specifying-layouts-for-controllers) of the Rails guides to see how to set a custom layout for your controller.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
