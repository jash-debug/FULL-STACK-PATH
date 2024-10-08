# Blog app: add authorization rules

## Learning objectives
- Limit access to web app resources based on authorization rules.

### Estimated time: 2.5h

## Description
In this project, you will add authorization to your app using [CanCanCan](https://github.com/CanCanCommunity/cancancan).

*IMPORTANT NOTE: Read **all** requirements before you start building your project.*

### General requirements

- Make sure that there are [no linter errors](https://github.com/microverseinc/linters-config).
- Make sure that you used correct [Gitflow](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/gitflow.md).
- Make sure that you documented your work [in a professional way](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/documentation/articles/professional_repo_rules.md).

### Ruby requirements
- Follow our list of [best practices for Ruby](https://github.com/microverseinc/curriculum-ruby/blob/main/articles/ruby_best_practices.md).

### Project requirements
- Install CanCanCan in your project.
- Add a `role` column to the users table. Remember to use a migration for this.
- A user can delete a post if it is theirs or if they have an admin role (column `role` has value `"admin"`). Use CanCanCan for this authorization.
    - For that you need to implement the post deleting functionality. Add the "Delete" button to the view and make sure that only authorized users can see it.
- A user can delete a comment if it is theirs or if they have an admin role (column `role` has value `"admin"`). Use CanCanCan for this authorization.
    - For that you need to implement the comment deleting functionality. Add the "Delete" button to the view and make sure that only authorized users can see it.


### Need a big picture?

Remind me about [the big picture of this project](./sneak_peek.md).

## Work and submission mode

- You should implement the above requirements only in **one repository** in your pair-programming group.
- You should ask for a review and submit this activity **on behalf of your pair-programming group.**

## Code review

Follow [these steps](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/code-review/articles/how_to_ask_for_a_code_review.md) to request a code review of your project.

## Submit your project

After the final approval from a code reviewer, you need to submit your project.
[Read this FAQ for a reminder on how to submit your project.](https://microverse.zendesk.com/hc/en-us/articles/360061344234)
Now go to your Student Dashboard and submit your project.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
