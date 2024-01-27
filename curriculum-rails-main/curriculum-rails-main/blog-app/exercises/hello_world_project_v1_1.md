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
 - Run `rails server` and visit http://localhost:3000/ in your browser!

#### Play with your first Rails website

After checking to make sure your Rails project is being served to the browser (http://localhost:3000/), there are a few things that need to be changed in order to set the display to let us view what we want.  Do not worry if you do not understand everything - you will learn the technical explanation for what is happening in the upcoming lessons.

- Let's use Rails' generators (known as scaffolding) to automagically make the files we need. For this you will do `rails generate controller Pages hello` in your shell, look at the example:
  ```
  $> rails generate controller Pages hello

      create  app/controllers/pages_controller.rb
       route  get 'pages/hello'
      invoke  erb
      create    app/views/pages
      create    app/views/pages/hello.html.erb
      invoke  test_unit
      create    test/controllers/pages_controller_test.rb
      invoke  helper
      create    app/helpers/pages_helper.rb
      invoke    test_unit
  ```
- Looking at the output of the command you will see all the generated things, but for now you only need to focus on one `app/views/pages/hello.html.erb`. You will put your HTML in this one.
- Open the file `app/views/pages/hello.html.erb` and add an `h1` element saying `"Hello world"`.
- Open http://localhost:3000/pages/hello in your browser. You should see your "Hello world" message.
- In `config/routes.rb` replace `get 'pages#hello'` with `root 'pages#hello'`
- Revisit http://localhost:3000/ and see your changes in action. Now your "Hello world" page should be displayed as the main page.
- Push all your changes to GitHub.

### Submit your exercise
[Read this FAQ for a reminder on how to submit your exercise.](https://microverse.zendesk.com/hc/en-us/articles/360061344234)
Now go to your Student Dashboard and submit your exercise.
Paste a link to your GitHub repository.


------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
