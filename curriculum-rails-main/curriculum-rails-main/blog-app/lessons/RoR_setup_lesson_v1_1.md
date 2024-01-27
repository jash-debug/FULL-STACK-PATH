# How to set up an RoR project?

## Learning objectives 

- Install Ruby on Rails framework.
- Understand default file structure in Rails.

### Estimated time: 1h

## The Ruby on Rails framework

The Ruby on Rails framework has a bright and friendly community of developers who not only enjoy development, but who also love the 'magic' of development. As a result, Rails can accomplish many tasks for you 'out of the box.' Because so many developers before you have done the exact same steps over and over again, they went ahead and automated them.

Just look at how the Rails new project generator creates an entire usable project for you with one simple line:
```rails new Project```  
In moments you have an entire project directory named Project built for you.

- Take a look at this [breakdown](./articles/default_rails_structure.md) of the important folders in your project directory.

### Why is understanding the Ruby on Rails framework important? 

As future developers, Ruby on Rails can be useful for saving you time and effort. It has an entire full-stack framework packaged nicely together. RoR is a framework that has been open source for over 15 years, and was someone's active project before that. It works. It works well. More than that though, the concepts you learn by understanding how RoR works are applicable to every other stack that has the same components but separately, like MERN.

### Dependencies

In fact, you'll find you are still using some of these same technologies. Just like any other project compiled of features, Rails (remember it's just a gem), has a few dependencies you may recognize. Go ahead and check the most recent version of each of these:

 - Ruby >= 3.0 (ruby --version)
 - SQLite3 >= 3.0 (sqlite3 --version)
   
 ##### Rails as a Gem 

Since Rails started out as a project full of packages and libraries, and has since become the full-stack framework it is, it can be easy to forget that it is also just a package itself.  To install it you can do

```
gem install rails
```

After the installation you should be able to do `rails --version` and get the your current Rails version, which should be at least version 7. 
 
It can be good to keep in mind which version you're using as each of these will update on their own schedule and sometimes the code changes just enough to give us bugs. This will be true for all the packages, gems, APIs, or any other dependencies you may bring into your projects as a developer.

### Database

You may have noticed that SQLite3 is the default database for Rails. It's a simple, lightweight database and works great for local projects and prototyping. However, when deploying your Rails project, you will need to use PostgreSQL. It's a good idea to get comfortable with it starting out, and it's super easy to configure your Rails new generator to set your project up with it by simply appending  

``` --database=postgresql ```
  
to the end of the command, like this:

`rails new Project --database=postgresql`  
`cd Project`  
`rails s`

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
