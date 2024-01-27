# Active Record - CRUD

## Learning objectives

- Write SQL queries with Active Record.

### Estimated time: 1h

## Description
In the previous lesson you learned how to query database with your models thanks to Active Record. Now it is time to make changes in your data.
Therefore, you will learn about basic CRUD operations implementation in Active Record - create (C), read (R), update (U), and delete (D). 

### Why is it important?
Whoever is going to use your websites, sooner or later will need to make changes in your data.

### Learn more about CRUD in Active Record

- Read Rails Guides [CRUD](https://guides.rubyonrails.org/active_record_basics.html#crud-reading-and-writing-data) section and a handy list of [ActiveRecord methods](https://medium.com/@oharacatherine/active-record-crud-operations-e2864a07657e).
- Take a look at the most trivial example of CRUD operations for user model:
```ruby

class User < ApplicationRecord
end

User.create(first_name: 'Tom', last_name: 'Smith', age: '37') # Create
User.find_by(first_name: 'Tom') # Read
User.find(1).update(first_name: 'Ann') # Update
User.find_by(first_name: 'Tom').delete # Delete
```

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
