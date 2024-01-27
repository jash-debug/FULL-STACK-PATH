# Setting up a custom route, action, and view

In Rails, there is a lot of 'magic' happening behind the scenes that allows files to be linked simply by using the right names and putting them in the right folders. Using Rails generators will make sure this happens 'automagically' but if we want to set up a custom page it's important to know what goes where. We are starting our mini-project with the route, because this is the first place that receives any traffic, and ending with the view, because this is the final output of our traffic. 

## Custom route
Once you have a new Rails project opened, go to your routes.rb file and type:
```ruby
get '/greeting', to: 'custom_pages#hello'
```
This tells our app that when it encounters a `get` request from the URL string `/greeting`, to find the appropriate `controller#action` it should look in the `CustomPages Controller` for the `hello` method.

## Custom controller action

Now, let's go to the `app/controllers` folder and add a new file called `custom_pages_controller.rb` and in it, type the following:  
```ruby  
class CustomPagesController < ApplicationController
  def hello
    render "greet_the_world"
  end
end
```  

## Custom view page

Finally, go to the views folder and create a new folder called `custom_pages`, then inside that folder create a file called `greet_the_world.html.erb`.  In that file, add the following code:  
```ruby   
<h1>Hello World!</h1>
```  

TA-DA! Because we have a folder in our views directory that matches our controller, and that folder has an HTML file that matches our action, Rails is able to put everything together for us, all we need is a route that points the way.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
