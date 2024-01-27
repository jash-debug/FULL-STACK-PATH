# Blog App: validations, model specs, and n+1 problems

## Learning objectives
- Use validations for models.
- Write unit tests for models.
- Secure app from n+1 problems.

### Estimated time: 4h

## Description

In this project, you will add validations to your models, create specs for them, and find and fix N+1 queries problems.

*IMPORTANT NOTE: Read **all** requirements before you start building your project.*

### General requirements

- Make sure that there are [no linter errors](https://github.com/microverseinc/linters-config).
- Make sure that you used correct [Gitflow](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/gitflow.md).
- Make sure that you documented your work [in a professional way](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/documentation/articles/professional_repo_rules.md).

### Ruby requirements
- Follow our list of [best practices for Ruby](https://github.com/microverseinc/curriculum-ruby/blob/main/articles/ruby_best_practices.md).

### Project requirements
- Add the following validations:
  - For the User model:
    - Name must not be blank.
    - PostsCounter must be an integer greater than or equal to zero.
  - For the Post model:
    - Title must not be blank.
    - Title must not exceed 250 characters.
    - CommentsCounter must be an integer greater than or equal to zero.
    - LikesCounter must be an integer greater than or equal to zero.
- Add unit specs for all of your models' methods and validations.
- Add flash messages in the create actions in all your controllers.
- Make sure that the N+1 problem is solved when fetching all posts and their comments for a user.
    - Do not use the bullet gem in this exercise - instead analyze the logs as showed in this [article](https://dev.to/junko911/rails-n-1-queries-and-eager-loading-10eh)
    - **In your PR description include the screenshots of your app's logs before and after the fix**
    - This is the corresponding wireframe view: ![blog all user posts](./images/blog_user_all_posts.png)

### Need a big picture?

Remind me about [the big picture of this project](./sneak_peek.md).

## Work and submission mode

- You should submit this activity **individually.**

## Code review

Follow [these steps](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/code-review/articles/how_to_ask_for_a_code_review.md) to request a code review of your project.

## Submit your project

After the final approval from a code reviewer, you need to submit your project.
[Read this FAQ for a reminder on how to submit your project.](https://microverse.zendesk.com/hc/en-us/articles/360061344234)
Now go to your Student Dashboard and submit your project.

# Additional requirements

*These are all optional, but if you're interested in exploring this topic further, feel free to implement them. Any exploration here should be done outside program time.*

*If you decide to implement these requirements you should do it in a separate pull request. As always, remember to document your decision in GitHub comments.*

- Th basic exercise is about tracking the n+1 issues manually. Once you do that, you can try to use the [bullet gem](https://github.com/flyerhzm/bullet) to find and fix all other N+1 problems in your app.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
