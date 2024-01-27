# Querying database with Active Record

### Conditions
The ability to query using parameters with `where` might be what reminds you the most of SQL. Using `where`, we have lines like this: 
```ruby 
Book.where("title = ?", params[:title])
```
to help us find a specific book, by its title.

#### Order and limit
[Ordering with Active Record](https://guides.rubyonrails.org/active_record_querying.html#ordering) requires only one method. And [limiting the number of records](https://guides.rubyonrails.org/active_record_querying.html#limit-and-offset) as well.
```ruby 
Book.order(title: :desc)
Book.limit(10)
```

#### Chaining methods
As long as our [method that returns a single object](https://guides.rubyonrails.org/active_record_querying.html#retrieving-a-single-object) is at the end of the line, we can also [chain methods](https://guides.rubyonrails.org/active_record_querying.html#understanding-method-chaining) together! For example, if we want the first 7 users in ascending order we could just say: 
```ruby
User.limit(7).order(created_at: :asc)
```

### Existence
We can check the [existence](https://guides.rubyonrails.org/active_record_querying.html#existence-of-objects) of a table with `User.exists?` or even pass an array of user IDs like this: `User.exists?(id: [1, 2, 3])` to check if some users exist. 

### Aggregates
We can even get immediate [calculations](https://guides.rubyonrails.org/active_record_querying.html#calculations) by passing a column name to `count`, `average`, `minimum`, `maximum`, or `sum` like `User.average('hours')`.

### Joins
Also, take special note of the difference between `includes()` and `joins()` if chained to a `where()` statement. The Ruby on Rails guide section about [specifying conditions on Eager Loaded associations](https://guides.rubyonrails.org/active_record_querying.html#specifying-conditions-on-eager-loaded-associations) explains that one of the key differences is when using `includes()`, if no results match, then all original table records would be returned. However, with a `joins()`, if no conditions match, then no records are returned.

### Pluck
We could [pluck](https://guides.rubyonrails.org/active_record_querying.html#pluck) out an array with all of the users' ids using `User.pluck(:id)` or IDs and names with `User.pluck(:id, :name)`. This is common enough that we can now just say `User.ids`!

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
