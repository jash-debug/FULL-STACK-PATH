# APIs

## Learning objectives
- Build an API that is RESTful.
- Understand the importance of APIs and docs following standards.

### Estimated time: 2h

## Description
In this lesson, you will learn how you can start building an API using Ruby on Rails. An API follows pretty much the same logic as a traditional app, but it returns data in another format (like JSON) instead of HTML.

### Why are APIs important?
Because building an API is what allows you to have multiple front-ends that use the same back-end. For example, the web page, a desktop app, and a mobile app are different front-ends, but they all will use the same API (back-end).

### APIs
In our context, an API is a back-end that responds to requests in a format different than HTML (in most cases JSON).

One particular difference between a traditional back-end and API is that an API is stateless. There are no cookies or sessions to keep some state between requests. Because of this, authentication is handled differently. One authentication solution is to use [JWT](https://jwt.io/).

To learn more about APIs, read the following articles:
- Start with the [Intro to APIs and how to build them with RoR by The Odin Project](https://www.theodinproject.com/paths/full-stack-ruby-on-rails/courses/ruby-on-rails/lessons/apis-and-building-your-own)
- Read Rails guides about [Rails API-only](https://guides.rubyonrails.org/api_app.html)
- Follow the tutorial [Create a Basic API with Ruby on Rails](https://web-crunch.com/posts/create-a-basic-api-with-ruby-on-rails). You do not need to build the API from this tutorial. Just make sure that you understand the process outlined in the videos and double-check it by reading the notes. Once you start building your own API in the following activities, you can go back to this tutorial in order to get the guidelines.


## Additional materials
**These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.**

- [What is token-based authentication](https://stackoverflow.com/questions/1592534/what-is-token-based-authentication)
- [RAILS 6 & 7 API Authentication with JWT (Token-based authentication)](https://www.bluebash.co/blog/rails-6-7-api-authentication-with-jwt/)

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
