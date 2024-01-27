# Blog app: add devise

## Learning objectives
- Build a web app that requires the user to log in.
- Use devise gem for authentication.

### Estimated time: 2.5h

## Description
In this project, you will add the [devise](https://github.com/heartcombo/devise) gem to your app and use it for the registration and login of users.

*IMPORTANT NOTE: Read **all** requirements before you start building your project.*

### General requirements

- Make sure that there are [no linter errors](https://github.com/microverseinc/linters-config).
- Make sure that you used correct [Gitflow](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/gitflow.md).
- Make sure that you documented your work [in a professional way](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/documentation/articles/professional_repo_rules.md).

### Ruby requirements
- Follow our list of [best practices for Ruby](https://github.com/microverseinc/curriculum-ruby/blob/main/articles/ruby_best_practices.md).

### Project requirements
- Remove `current_user` method in `ApplicationController`, devise will provide us with one.
- [Install and setup devise](https://github.com/heartcombo/devise#getting-started).
  - Can register a new user.
  - User logs in with a combination of email and password.
  - Hashed password should be stored in the database.
  - Ask for confirmation of email.
  - Can reset password.
- [Modify the views in devise](https://github.com/heartcombo/devise#configuring-views) for registration and login to match [the wireframes from the Sneak Peek](https://github.com/microverseinc/curriculum-rails/blob/main/blog-app/sneak_peek.md#:~:text=For%20this%20project%20you%20will%20have%20full%20freedom%20in%20terms%20of%20visual%20design%20but%20you%20will%20need%20to%20keep%20the%20following%20wireframes%3A) and your styling.


### Need a big picture?

Remind me about [the big picture of this project](./sneak_peek.md).

## Work and submission mode

- You should implement the above requirements in **all repositories** in your pair-programming group. _That means that each group member needs to open a new pull request in their repo._
- We will check the commit history to make sure that everybody has contributed code on each project.
- You should ask for a review and submit this activity **individually.**

## Code review

Follow [these steps](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/code-review/articles/how_to_ask_for_a_code_review.md) to request a code review of your project.

Each of you needs to request a code review individually.

## Submit your project

After the final approval from a code reviewer, you need to submit your project.
[Read this FAQ for a reminder on how to submit your project.](https://microverse.zendesk.com/hc/en-us/articles/360061344234)
Now go to your Student Dashboard and submit your project.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
