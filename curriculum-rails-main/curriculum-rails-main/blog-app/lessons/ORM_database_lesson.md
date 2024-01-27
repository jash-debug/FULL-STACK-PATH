# Database connection and ORM

## Learning objectives 

- Understand what ORM is.
- Use database migration files to maintain database schema.

### Estimated time: 1.5h

## Description
Since you are already familiar with ERD diagrams and SQL, much of Active Record should feel familiar even if not at first glance. As our model, the Active Record is simply a Ruby syntax way of talking to a database. This is great because once we have our Active Record modeled the way we want, it's simple to switch databases if we want to go from SQLite3 to PostgreSQL!

### Why is understanding the ORM database important? 
We know that Rails speaks Ruby and databases speak SQL, so how do we get them to interact? With an ORM framework! Object-Relational Mapping is a technique that allows us to access our database as if we were accessing class variables in our program. Through the conventions already in place with Rails, thankfully we don't have to write all of the getters and setters for our records ourselves. Instead, Rails gives us Active Record as an ORM framework. 

### Active Record
Go ahead and read [sections 1-4 about Active Record](https://guides.rubyonrails.org/active_record_basics.html#what-is-active-record-questionmark), but don't worry about section 2 of this guide just yet.

We will go deeper into Active Record in the upcoming lessons but right now you just need a basic understanding of it.

#### Migrations
In order to create and maintain a database that is connected to your Rails app, you should always use migrations.

- The most common way you will go about adjusting the database is through [migrations](https://guides.rubyonrails.org/active_record_migrations.html#migration-overview). Go ahead and read section 1 of this guide to learn more about migrations.
- Read through [section 2.1](https://guides.rubyonrails.org/active_record_migrations.html#creating-a-standalone-migration) to see how some Rails naming conventions make generating migration files simple and efficient!
- Read more about running [Rails migrations](https://guides.rubyonrails.org/active_record_migrations.html#running-migrations) and see how to [specify the environment](https://guides.rubyonrails.org/active_record_migrations.html#running-migrations-in-different-environments) or even how to [run only one migration file](https://guides.rubyonrails.org/active_record_migrations.html#running-specific-migrations) at a time.
- Check out [how to create a database table with Rails migrations](./articles/create_table_migration.md) and see some examples of how migration generation commands translate into actual code.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
