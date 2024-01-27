# Blog app - integration specs for views

## Learning objectives
- Write integration tests with Capybara gem.

### Estimated time: 2.5 hours

## Description
In this project, you will create integration tests for all of the views used in your project. Be sure to cover the user stories (or user workflows) that you **want** your users to experience while taking into consideration the possible errors your users may cause.

*IMPORTANT NOTE: Read **all** requirements before you start building your project.*

### General requirements

- Make sure that there are [no linter errors](https://github.com/microverseinc/linters-config).
- Make sure that you used correct [Gitflow](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/gitflow.md).
- Make sure that you documented your work [in a professional way](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/documentation/articles/professional_repo_rules.md).

### Ruby requirements
- Follow our list of [best practices for Ruby](https://github.com/microverseinc/curriculum-ruby/blob/main/articles/ruby_best_practices.md).

### Project requirements
-  Use Capybara to write integration tests for each view in your project.

- Login page:
  - I can see the username and password inputs and the "Submit" button.
  - When I click the submit button without filling in the username and the password, I get a detailed error.
  - When I click the submit button after filling in the username and the password with incorrect data, I get a detailed error.
  - When I click the submit button after filling in the username and the password with correct data, I am redirected to the root page.
  
- User index page:
  - I can see the username of all other users.
  - I can see the profile picture for each user.
  - I can see the number of posts each user has written.
  - When I click on a user, I am redirected to that user's show page.
  
- user show page:
  - I can see the user's profile picture.
  - I can see the user's username.
  - I can see the number of posts the user has written.
  - I can see the user's bio.
  - I can see the user's first 3 posts.
  - I can see a button that lets me view all of a user's posts.
  - When I click a user's post, it redirects me to that post's show page.
  - When I click to see all posts, it redirects me to the user's post's index page.

- User post index page:
  - I can see the user's profile picture.
  - I can see the user's username.
  - I can see the number of posts the user has written.
  - I can see a post's title.
  - I can see some of the post's body.
  - I can see the first comments on a post.
  - I can see how many comments a post has.
  - I can see how many likes a post has.
  - I can see a section for pagination if there are more posts than fit on the view.
  - When I click on a post, it redirects me to that post's show page.

- Post show page:
  - I can see the post's title.
  - I can see who wrote the post.
  - I can see how many comments it has.
  - I can see how many likes it has.
  - I can see the post body.
  - I can see the username of each commentor.
  - I can see the comment each commentor left.

**Be sure to include integration specs for any other features you may have implemented!**


### Need a big picture? 

## Work and submission mode

- You should implement the above requirements in **all repositories** in your pair-programming group. _That means that each group member needs to open a new pull request in their repo._
- We will check the commit history to make sure that everybody has contributed code on each project.
- You should ask for a review and submit this activity **individually.**

Remind me about [the big picture of this project](../sneak_peek.md).

## Code review

Follow [these steps](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/code-review/articles/how_to_ask_for_a_code_review.md) to request a code review of your project.

Each of you needs to request a code review individually.

## Submit your project

After the final approval from a code reviewer, you need to submit your project.
[Read this FAQ for a reminder on how to submit your project.](https://microverse.zendesk.com/hc/en-us/articles/360061344234)
Now go to your Student Dashboard and submit your project.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
