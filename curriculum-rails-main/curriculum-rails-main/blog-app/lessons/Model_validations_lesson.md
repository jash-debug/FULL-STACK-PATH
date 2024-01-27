# Model validations

## Learning objectives:

-   Use validations for models.

### Estimated time: 0.5 hours

## Description
The concept of validation should not be unfamiliar at this point. We use it in all aspects of development and when working with databases, it becomes even more important. Imagine checking a database of users for anyone over the age of 18 and someone's age is listed as "Sandwich". What's a logical computer to do except throw an error and prevent you from checking your user's age. This may seem like a silly example but when your database has hundreds or thousands of users and they get access to different content based on their age, being unable to check your user's age could result in a poor user experience and potentially affect other users as well. Without validations checking that the data being input is the type of data we want, failure is imminent.

- Check out [this section](https://guides.rubyonrails.org/active_record_validations.html#validations-overview) of the Rails guides for a simple example of a model-level validation.

### Why are model validations important?
While it's a good idea to have validations in place at the database level, doing so requires querying a database before reaching that validation and that can become costly. This cost might be negligible if your data is valid and will be saved but if this is not the case the database will be queried for no reason. Model validations allow us to ensure valid data before getting to the database.

- Check out [this section](https://guides.rubyonrails.org/active_record_validations.html#why-use-validations-questionmark) of the Rails guides for more reasons to use model validations.

#### Validation errors
Validations may be an important aspect of creating a clean database but providing information to the user is an equally important aspect of a good user experience, and as usual, Rails handles this beautifully. When submitting data to create a new record, if there are any failed validations, Rails will attach an `errors` attribute with a message explaining what went wrong. So if you fail to update `@post`, you can see why it failed by looking at `@post.errors`

- Read [this section](https://guides.rubyonrails.org/active_record_validations.html#displaying-validation-errors-in-views) of the Rails guides to see how to display errors in Views

### What is the flash in Rails?
Another way you can display errors, or successes, to the user is through the use of flash messages. You may have seen a flash key in a controller somewhere. Something like `flash[:alert]` or `flash[:notice]`. These little hash keys are one-shot messages you can display to the user that will disappear as soon as the page refreshes. You can technically use any key name you want but it's best to stick to the ones mentioned here as a standard convention. Just as these key names imply, they are great for displaying alerts like when a user puts in the wrong password, notices like when a user adds a friend or creates a post, or anything else you may need to tell the User but only once.

- Read [this section](https://guides.rubyonrails.org/action_controller_overview.html#the-flash) of the Rails guides to read more about working with the flash.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
