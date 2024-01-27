# Read about Rails router and RESTful routes

## Learning objectives

- Understand Rails RESTful design and router.

### Estimated time: 1h

## Description

You've already learned about RESTful routing and in Rails, the same concept applies for the same reasons. By using RESTful routes, Rails actually makes routing quite simple. Our `routes.rb` file allows us to connect requests to our controller#actions. Our routes are clearly defined and easy to direct. More importantly, because we have the REST standard, Rails has been able to set up a beautiful piece of magic for us when it comes to declaring our routes.
 
### Why is using RESTful routes important?

We use the RESTful guidelines in Rails so that we can all work under a standard practice. While there are other architectures out there in the world wide web, REST is by far the easiest to use and in general, is more flexible than others. For these reasons, and others, it is quickly becoming the most popular way of structuring our back-end and understanding how REST is implemented will benefit you in and out of Rails.

### RESTful design
There are 7 RESTful route actions: index, new, show, create, edit, update, and destroy. If you had to write each of these routes individually, for every controller, you can imagine your routes file getting quite large, quite fast. Just look at this:
```ruby 
  get "/users", to: "users#index" # usually requires a view
  get "/users/new", to: "users#new" # usually requires a view
  get "/users/:id", to: "users#show" # usually requires a view
  post "/users", to: "users#create"  # usually a submitted form
  get "/users/:id/edit", to: "users#edit" # usually requires a view
  put "/users/:id", to: "users#update" # usually a submitted form
  delete "/users/:id", to: "users#destroy" # usually called with a button
  ``` 
However, if we stick to convention, we can do all of this with just one line: 
```ruby
resources :users
```    

 Now isn't that nice?
 
-   Here are some great visual diagrams to help you in [understanding Rails routes and restful design](https://medium.com/podiihq/understanding-rails-routes-and-restful-design-a192d64cbbb5).
 
-   Check out [this section](https://guides.rubyonrails.org/routing.html#listing-existing-routes) of the Rails guides to see how to view your available routes in the console!

### Rails router
The Rails router is also much simpler than you may originally believe. Ultimately, all we're referring to is the `routes.rb` file. In this file, all we're doing is telling our app 'when a URL comes in from the browser, send it to this controller action'. It's as simple as that.

<center>

| HTTP verb | Everything after the root URL | Direction | Controller#action |
| :-------------: | :----------: | :-----------: |  :-----------: |
|  get | '/users', | to: | 'users#index' |

</center>

We will learn in later lessons that we can do much more with our routes, such as redirecting them, adding a namespace, or creating custom path names, but for now it's enough to focus on routes the way we've written them here.

- Read the notes below the [CRUD, verbs, and actions](https://guides.rubyonrails.org/routing.html#crud-verbs-and-actions) section of the guides to see why route ordering is important! 

- Check out [this section](https://guides.rubyonrails.org/routing.html#nested-resources) of the Rails guides for a look at how to work with nested resources.

## Additional materials

*These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.*

- Check out [this section](https://guides.rubyonrails.org/routing.html#dynamic-segments) of the Rails guides to see how we get params from our URLs!

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
