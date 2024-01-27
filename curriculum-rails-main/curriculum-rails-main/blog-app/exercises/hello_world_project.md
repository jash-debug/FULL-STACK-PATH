# Hello Rails app 

## Learning objectives
- Install Ruby on Rails framework.
- Use RubyGems as a software package system.

### Estimated time: 1.5h

## Exercise

As you know by now, we have a clear path from the browser to the routes file to the Controller action, which can pull data from the database through the Model and create an instance variable that is then sent to the View to be displayed to the user.

Let's put this into practice by creating our very own Rails 'Hello World!' project!

*IMPORTANT NOTE: Read **all** instructions before you start this exercise.*

### Instructions

 - Create a new app called 'hellorails'.
 - Initialize your project with Git.
 - Make sure that your project has Postgres database set up. 
 - Display a <strong>h1</strong> element to the display that says 'Hello World!'. 
 - Run `rails s` and visit http://localhost:3000/ in your browser!

#### Play with your first Rails website

After checking to make sure your Rails project is being served to the browser, there are a few things that need to be changed in order to set the display to let us view what we want.  Do not worry if you do not understand everything - you will learn the technical explanation for what is happening in the upcoming lessons.

- We need a Controller. Since everything goes through that, let's go ahead and generate one:   
 ```ruby 
 rails generate controller Pages hello
 ```   
 This should give us a Controller and a View.  

- Set up the View. There should now be a `hello.html.erb` in the `views/pages` directory. Put your HTML in that file.

- Set your route.  In the `config/routes.rb` file, you always need to set a root route. We want to set our route to a controller#action. So for our example we'll want to set  
 `root 'pages#hello'` 
- Revisit http://localhost:3000/  and see your changes in action.
- Push all your changes to GitHub.

### Submit your exercise
[Read this FAQ for a reminder on how to submit your exercise.](https://microverse.zendesk.com/hc/en-us/articles/360061344234)
Now go to your Student Dashboard and submit your exercise.
Paste a link to your GitHub repository.


------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
