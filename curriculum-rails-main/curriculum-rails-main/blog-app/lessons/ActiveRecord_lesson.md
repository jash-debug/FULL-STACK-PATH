# Active Record - associations & queries

## Learning objectives

- Set up associations between models.
- Write SQL queries with Active Record.

### Estimated time: 2h

## Description
Active Record acts as the translator between Ruby and SQL. So when a request comes from the controller to the model, the model then uses Active Record to speak to the database.

### Why is understanding Active Record important?
All the syntax such as `User.first` and `User.find(1)` are methods brought to us by Active Record. Active Record comes prebuilt with a tremendous amount of features and methods we can use, many of which you may already be using. As such, understanding what is made available through Active Record not only makes you a better Rails developer, it also gives you many ways to gather data without having to write them yourself.

### Tables and Model

First, check [how easy it is to create a model with ActiveRecord!](https://guides.rubyonrails.org/active_record_basics.html#creating-active-record-models)

Models and tables are just two of the many things Rails connects for you if proper naming conventions are used. Let's examine these two by again using our users example. If we have to store some users in a table, it makes sense that we would need it to handle multiple users. Therefore our table names are always pluralized. We might use a table to store users, movies, or account_numbers, but in any case, we're always storing multiple instances of the same basic type of data. On the other hand, a model IS that basic type of data and as such, is expected to handle only one user at a time. When we write validations, for example, we might want to check if a user has a properly formatted email address before saving them to our database. This model may deal with lots of users over time but it only checks ONE at a time. Therefore, we keep the model singular.

Take a look at this quick example:

```ruby

class User < ApplicationRecord
end
```

Thanks to the naming convention the user model will connect to the users table in your database.
And even if this model looks like an empty class, it has a lot of power. As it inherits from the `ApplicationRecord` (and indirectly from the `ActiveRecord`), it already allows you to perform actions on your database records:

```ruby
User.first # returns first record from users table
User.where(first_name: 'Tom') # returns all records with `Tom` as a first name
User.last.delete #deleted the last record in user table
```

- Check out [this section](https://guides.rubyonrails.org/active_record_basics.html#naming-conventions) of the Rails guides for examples of model / table names.

### Querying database with Active Record

You are already familiar with SQL queries. In [this short article](../articles/queries_with_active_record.md), you will learn how to write them by using ActiveRecord methods.

### Associations

Even if you correctly set up foreign keys in your migration files, your models based on the Active Record will NOT recogize the associations between tables automatically. Therefore, you will need to declare those associations in model files. Good news - if you understand the foreign key mechanism and many-to-one/many-to-many relations in databases - understading Active Record associations will be easy for you.

A quick example:

```ruby

class Author < ApplicationRecord
  has_many :books
end

class Book < ApplicationRecord
  belongs_to :author # table with foreign key
end
```

Read more in [The types of associations](https://guides.rubyonrails.org/association_basics.html#the-types-of-associations).
Also remember this simple rule: `belongs_to` associations will always go to the model that connects to the table that includes a foreign key.

As usually with RoR, the naming convention helps you a lot when it comes to the foreign keys. Rails assumes that the column used to hold the foreign key on this model is the name of the association with the suffix "_id" added. If that is not the case you can use [class_name](https://guides.rubyonrails.org/association_basics.html#options-for-belongs-to-class-name) and [foreign_key](https://guides.rubyonrails.org/association_basics.html#options-for-has-many-foreign-key) options when defining your associations.


### Scopes

If you need to create custom search parameters, it would be helpful to remember [lambdas](https://www.rubyguides.com/2016/02/ruby-procs-and-lambdas/). You'll use this syntax when creating [scopes](https://guides.rubyonrails.org/active_record_querying.html#scopes). Looking past these special terms, we will still see a method definition. A scope is similar to a class definition and is often preferred for very simple examples like `scope :in_print, -> { where(out_of_print: false) }` and calling `Book.in_print` to search for all books with a false in their out_of_print column.

## Additional materials

*These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.*

- Read through all of these [finder methods](https://guides.rubyonrails.org/active_record_querying.html#retrieving-objects-from-the-database) to get a stronger understanding of what methods are already available for you.
- Would you like to not follow the naming convention for models and tables? Check [how to override the naming convention](https://guides.rubyonrails.org/active_record_basics.html#overriding-the-naming-conventions).

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
