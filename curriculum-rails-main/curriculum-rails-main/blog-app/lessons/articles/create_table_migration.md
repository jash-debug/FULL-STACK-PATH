# Generate migration files
Migrations are here to help us 'migrate' or 'move table data into' our database arrangement, or schema. This lets us add tables, add columns, change table or column names, set default data for columns, change primary keys, and much more! We can easily generate a migration file and, using some semantic language, we are able to auto-magically generate some code in our migration file:

`rails generate migration add_column_to_users name:string`

# Write migrations
-  ### Create a table
`rails generate migration CreateUsers`
```ruby 
class CreateUsers < ActiveRecord::Migration[6.0]
    def change
      create_table :users do |t|

        t.timestamps
      end
    end
end
```
-  ### Add foreign keys
`rails generate migration AddUserRefToProducts user:references`
```ruby 
class AddUserRefToProducts < ActiveRecord::Migration[6.0]
     def change
       add_reference :products, :user, foreign_key: true
     end
end
```
-  ### Add indexes
`rails generate migration AddAddressToUsers address:string:index`
```ruby 
class AddAddressToUsers < ActiveRecord::Migration[6.0]
     def change
       add_column :users, :address, :string
       add_index :users, :address
     end
end
```

# Run migrations
To run all migrations is quite easy. Simply use the code below: 

`rails db:migrate`

# Basic Troubleshooting
- Using the [change method](https://guides.rubyonrails.org/active_record_migrations.html#using-the-change-method) allows for a lot of leeway in case we've done something wrong in our migration. With it, we are given access to an easy way to revert roll the database back to a previous version.
- If we ever make a mistake in our migration file, it's quite easy to [rollback the database](https://guides.rubyonrails.org/active_record_migrations.html#rolling-back), adjust our file, and migrate the changes again.
-  **Never roll back a migration that has already been pushed!**
    - Best case scenario, you will cause problems with the local database of your teammates and worse case scenario, you will cause problems with the production database.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
