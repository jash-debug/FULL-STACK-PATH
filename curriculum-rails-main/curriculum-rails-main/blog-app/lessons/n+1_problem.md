# Secure app from n+1 problems

## Learning objectives
- Secure app from n+1 problems.

### Estimated time: 1h

## Description

In this lesson, you will learn about one of the most common problem and how to handle it, the N+1 queries problem. The main issue is this problem can escalate quickly because it depends on an initial query for N objects and then additional queries for each of those objects.

### Why is N+1 important?

Because it is one of the most common performance problems you will find. Thankfully since it is super common it has a pretty standard solution baked into ActiveRecord and a lot of tools to identify the problem and solve it.

### N+1 problem

When does this problem occur? When you fetch multiples rows and then try to access an association for each one, like:

```ruby
posts = Post.order(:published_at)

posts.each do |post|
  puts "Author: #{post.author.name}"
end
```

Fetching the posts is one query with N results and then fetching every author is the other N queries, so N+1 queries total. To solve it ActiveRecord offers eager loading (the `#includes` method), this allows you to specify associations to fetch at the same time the rows you queried are fetched.

- [#includes API doc](https://api.rubyonrails.org/classes/ActiveRecord/QueryMethods.html#method-i-includes)
- [Rails N+1 queries and eager loading](https://dev.to/junko911/rails-n-1-queries-and-eager-loading-10eh)
- There is a gem that helps you to detect n+1 issues. Check it out: [bullet gem - configuration]([https://semaphoreci.com/blog/2017/08/09/faster-rails-eliminating-n-plus-one-queries.html](https://github.com/flyerhzm/bullet#configuration))


## Additional materials [optional header]
**These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.**
- Check the [bullet gem](https://github.com/flyerhzm/bullet) to help find and fix N+1 queries.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
