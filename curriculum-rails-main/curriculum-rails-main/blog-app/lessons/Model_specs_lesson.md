# Model specs

## Learning objectives:

-   Write unit tests for models.

### Estimated time: 0.5h

## Description

Model specs are a great way to double-check that your inputs will be saved appropriately and only when they are expected to. Whether following BDD or TDD, if you write your expectations in tests you can be certain your database is protected from unexpected entries. For example, you may have set up a uniqueness validation in your model but did you realize that it defaults to being case sensitive? In this way, `Hello World` and `hello world` are considered to be unique but it might not be ideal to have two different users with the names `BrandonD` and `brandond`. Having properly tested this model and noticed that both users would be accepted as separate records will save yourself a headache later on and prompt an update to your model validation.

### Why are unit tests important?

Simply put, testing your model is important because ensuring that your model works properly helps to ensure that all of your data flows through your app and into your database correctly. As the model is responsible for describing data associations, ensuring the presence of data columns, validating data, and it contains methods for accessing and scoping data, it is a key point for the entry of bugs. If your model is well-tested, you can rest assured that your database is safe from undesirable entries.

### Writing unit tests

Writing unit tests is no different than writing any other test if you start with your expectations and write tests that prove them. Luckily for us, models are pretty straightforward most of the time, and you can run down the model file to see what to test. If a relationship has been defined, make sure that the relationship is accessible. If there is a validation in place, make sure a new record is not valid without that column's presence, uniqueness, or whatever other validation had been set up.

 - Check out this easy-to-follow example on how to [test model validations](https://hackernoon.com/how-to-write-your-first-tests-using-rspec-in-rails-applications-hhfk2bqs).

## Additional materials

*These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.*

 - Go through this more in-depth look at [how to write unit tests](https://semaphoreci.com/community/tutorials/how-to-test-rails-models-with-rspec).

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
