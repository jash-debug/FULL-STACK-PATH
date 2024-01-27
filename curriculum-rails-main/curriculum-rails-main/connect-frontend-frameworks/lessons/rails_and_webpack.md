# How to setup RoR + React project as one app with Webpack

## Learning objectives

- Understand the pros and cons of different approaches of connecting Ruby on Rails back-end with React front-end.

### Estimated time: 1h

## Why is this important?

Rails is still a very widely used framework but many people still prefer to use JavaScript frameworks for front-end features. As such, integrating React into your Rails project can have several benefits, some less obvious than others. 

The most obvious reason is ease. As Microverse students, you're already familiar with React so creating a front-end with familiar technology is always more comfortable. However, as you get more experienced with Rails you will find there's really very little it can't do.

Another reason you might want a React front-end could be for compatibility. There are lots of prebuilt features ready and waiting to be used in a new app and several of them are written in React. Additionally, converting a web app into a mobile or desktop app becomes very easy as things like Ionic and Electron are able to compile your React code, while it is unable to do so with Ruby.

Whatever the reason, there are ways to integrate your React front-end with your Rails back-end for one versatile monolithic app that can be hosted from a single source.  

At the end of the day, some people like their sandwich cut into rectangles while others like it in triangles, some like the crust on their toast, and others don't. Ultimately there's no wrong choice and the best choice may differ from project to project!

#### How to use React inside a Rails app

 - First, read an article by David Heinemeier Hansson [Rails 7 will have three great answers to JavaScript in 2021+](https://world.hey.com/dhh/rails-7-will-have-three-great-answers-to-javascript-in-2021-8d68191b). It should give you a general understanding that there are 3 ways of working with Rails + React:
     - by using [import maps](https://github.com/rails/importmap-rails) (this approach has some downsides as pointed out by DHH _" You can do React with import maps, but it'll be through htm, and that might well be a compromise too far for those who are all-in."_)
     - by using [jsbundling-rails](https://github.com/rails/jsbundling-rails) (this approach is recommended by DHH: _"It's this path you should probably pick if you're going all-in on something like React with JSX or another JavaScript framework that demands a transpilation step"_)
     - by creating two separate apps (**SPOILER ALERT: you will learn about this in separate lesson and project**)
- Secondly, check the section named [**"Webpack"** in the article titled "How to Use React in a Ruby on Rails App"](https://betterprogramming.pub/react-with-rails-2022-bd28e1fcd355#ad0a)

## Additional resources

If you are curious about setting up Rails with React by using import maps, watch the official video [Alpha preview: Using React with import maps on Rails 7](https://www.youtube.com/watch?v=k73LKxim6tw).


------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
