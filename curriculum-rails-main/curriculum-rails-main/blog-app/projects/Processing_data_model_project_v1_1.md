# Blog App - processing data in models

## Learning objectives
- Set up associations between models.
- Write SQL queries with Active Record.

### Estimated time: 3h

## Description
Now it's time to set up our models. To start with, we have tables for Users, Posts, Comments, and Likes, which means we need a model for each one. You've already set the foreign key in the table schema but be sure to write it here too!

*IMPORTANT NOTE: Read **all** requirements before you start building your project.*

### General requirements

- Make sure that there are [no linter errors](https://github.com/microverseinc/linters-config).
- Make sure that you used correct [Gitflow](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/gitflow.md).
- Make sure that you documented your work [in a professional way](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/documentation/articles/professional_repo_rules.md).

### Ruby requirements
- Follow our list of [best practices for Ruby](https://github.com/microverseinc/curriculum-ruby/blob/main/articles/ruby_best_practices.md).

### Project requirements

### Create models
-  Create model classes for all entities as shown in the [ERD diagram](../images/blog_app_erd_v1_1.png).
-  Set up associations between models.
    - Remember that `author_id` column in `posts` table should be the foreign_key for the `users` table.

### Use models to insert data
- Familiarize yourself with ['rails c' command](https://guides.rubyonrails.org/command_line.html#bin-rails-console).
- Open rails console for your project.
- Create at least one user by running the following code:
    ```ruby
       first_user = User.create(name: 'Tom', photo: 'https://unsplash.com/photos/F_-0BxGuVvo', bio: 'Teacher from Mexico.')
       second_user = User.create(name: 'Lilly', photo: 'https://unsplash.com/photos/F_-0BxGuVvo', bio: 'Teacher from Poland.')
    ```
- Create at least 4 posts written by one of the users you created by running the following code:
    ```ruby
       first_post = Post.create(author: first_user, title: 'Hello', text: 'This is my first post')
    ```
- Create at least 6 posts comments for one of the posts you created by running the following code:
    ```ruby
       Comment.create(post: first_post, user: second_user, text: 'Hi Tom!' )
    ```
- Use other [CRUD methods](https://github.com/microverseinc/curriculum-rails/blob/main/blog-app/lessons/active_record_crud.md) to find, update and delete entities.


### Create custom methods
Your models should include some additional methods.
-  Users
    - A method that returns the 3 most recent posts for a given user.
-  Posts
    - A method that updates the posts counter for a user.
    - A method which returns the 5 most recent comments for a given post.
-  Comments
    - A method that updates the comments counter for a post.
-  Likes
    - A method that updates the likes counter for a post.
- Go to `rails c` and check if your methods are working.

### Need a big picture?

Remind me about [the big picture of this project](../sneak_peek.md).

## Work and submission mode

- You should submit this activity **individually.**

## Code review

Follow [these steps](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/code-review/articles/how_to_ask_for_a_code_review.md) to request a code review of your project.

## Submit your project

After the final approval from a code reviewer, you need to submit your project.
[Read this FAQ for a reminder on how to submit your project.](https://microverse.zendesk.com/hc/en-us/articles/360061344234)
Now go to your Student Dashboard and submit your project.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
