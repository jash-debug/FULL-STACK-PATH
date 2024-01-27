# Controllers

## Learning objectives

- Use controllers to handle requests and render empty views.
- Use params from browser requests in a safe way.

### Estimated time: 1.5h

## Description

Controllers do exactly what the name implies: they control. Your controller will be the central hub of all the activity happening in your app. It gathers whatever data you need, applies any necessary logic to that data, and then offers that data to your view. Despite how much controllers do, or maybe because of it, it's best to keep in mind that we want our controller to be as clean and thin as possible.

### Why is understanding controllers important?

Understanding how to work with your controller is a critical step in understanding how to work with Rails. Luckily for us, there's not THAT much to understand. By now you've seen how we can create custom controller actions, or use the standard RESTful actions. You've also seen how Rails connects our view to the controller.

### Learn more about controllers
-  Refresh on [Rails Guides intro to controllers](https://guides.rubyonrails.org/action_controller_overview.html#what-does-a-controller-do-questionmark).
-  Read about [methods and actions](https://guides.rubyonrails.org/action_controller_overview.html#methods-and-actions).
-  Read about [parameters](https://guides.rubyonrails.org/action_controller_overview.html#parameters).


### Handling params in the controller

Here's where we start to find something tricky. How do we get params into our controller in order to use them? Well to start off, let's recall our show route as an example.
```ruby
get "/users/:id", to: "users#show"
```

Now given that route, if we put `http://localhost:3000/users/1` into our browser, and have a show controller like this:
```ruby 
def show 
  puts params
end
```
We might see something like this `{"controller"=>"users", "action"=>"show", "id"=>"1"}` show up in the console. We can call our variable anything this way and we can find it in params using the same name we put in the URL. So if we have a route like `/users/:anything` then we would have `params[:anything]` available to call on in the corresponding controller action.

Pay special attention to the [strong parameters description in Rails Guides](https://guides.rubyonrails.org/action_controller_overview.html#strong-parameters).

## Additional materials

*These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.*

- Read about [skinny controllers](https://dev.to/kputra/rails-skinny-controller-skinny-model-5f2k) and how to put your fat controller on a diet!

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
