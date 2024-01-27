# Rails magic - how much can a naming convention do for you?

## Learning objectives

-   Understand Rails naming conventions.

### Estimated time: 1h

## Description

A lot of what happens in Rails is continuously described using the word 'magic' and things get completed 'auto-magically', but as Arthur C. Clarke said, "Magic is just science we don't understand yet" and he couldn't have been more right. In Rails, much of that magic comes down to simply following proper naming conventions.

These naming conventions have been set in place to keep things organized and make your life easier. While it may not feel intuitive at first, fear not! It will start to make sense soon enough.

### Why is following naming conventions important?

Naming conventions are what make the Rails magic work. You wouldn't ask a magician to pull a rabbit out of a hat without giving him a rabbit, or saw a lady in half without letting him use a saw, and you can't make the Rails magic work without following the proper naming conventions.

### Rails naming conventions example

As you could observe in your "Hello Rails" project, the view is directly tied to the controller just by properly structuring your project and naming things the same. For example, if we have a Pages controller and that controller has an index action, then we can put the HTML for our index layout in `app/views/pages/index.html.erb` and Rails immediately knows where to go to find the layout. This is some of the Rails magic in action! When it comes to properly naming your view it really is that easy, just name it whatever the corresponding action is named!

That being said, the controller does have a naming convention that we should stick to and that is to pluralize it. Take a look at the examples below to see how controllers and their corresponding views maintain the naming convention:

 - `controllers/posts_controller.rb`
  ```ruby 
  class PostsController
    def index
      # for this action the corresponding view file is /views/posts/index.erb
    end

    def new
      # for this action the corresponding view file is /views/posts/new.erb
    end
  end
  ```
 - `controllers/users_controller.rb`
  ```ruby
    class UsersController
      def index
        # for this action the corresponding view file is /views/users/index.erb
      end

      def new
        # for this action the corresponding view file is /views/users/new.erb
      end
    end
  ```

- Check out [this section](https://guides.rubyonrails.org/action_controller_overview.html#controller-naming-convention) of the Rails guides for a short description of controller naming conventions.
- Check out [this section](https://guides.rubyonrails.org/action_controller_overview.html#methods-and-actions) of the Rails guides for a short description of methods and actions.
- Check out this [mind map](https://teddicodes.files.wordpress.com/2015/02/railsnamingconventions.pdf) for a visual display of naming conventions in Rails.

### Custom naming
- We don't always have to necessarily use the magic of Rails, and sometimes we may find we are forced to break convention. Follow [this guide](./articles/naming_conventions_article.md) to set up a custom route, action, and view and work your own magic!

## Additional materials

*These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.*

- Check out [this cheatsheet](https://alexander-clark.com/blog/rails-conventions-singular-or-plural) of singular and plural naming conventions in Rails.


------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
