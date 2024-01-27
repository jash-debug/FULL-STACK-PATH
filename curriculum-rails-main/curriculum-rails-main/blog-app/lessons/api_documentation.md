# API documentation

## Learning objectives
- Generate documentation for an API.
- Understand the importance of APIs and docs following standards.

### Estimated time: 2h

## Description
In this lesson you will learn about API documentation. Good documentation is one of the most important parts of building an API.

The idea is that a user of your API can figure out how to use it by just reading the documentation and doesn't need to contact the API developer, support team, or read the actual code of the API.

One of the gold standards in API documentation is [Stripe's API documentation](https://stripe.com/docs/api).

### Why is API documentation important?

Imagine having to explain how one of your API endpoints works to every new user. It gets tiresome fast, right? So instead of explaining it every time it is better to write the explanation down and start your documentation.

Now as a user, imagine having to ask the API development team or support team how to use an endpoint every time you want to build something, or even worse, having no one to ask and needing to look into the API code to figure out how to use it. As a user you will never want to work with an API like that. This is why you, as an API developer, want to write documentation for your users.

**Guiding questions:**

*Think about these questions as you learn about API documentation.*

- What do you need to explain to use an endpoint?
- How can you make your documentation easily accessible?
- Should documentation come before or after implementation?

### Writing API documentation
One of the best ways to tackle writing documentation is to make it a part of your process, similar to how TDD makes tests part of your process. So first you write the documentation for an endpoint and then create the implementation for it using the documentation as requirements.

API documentation should be written for most users, not for the technical or senior ones. So try to keep it simple and have good examples for it. In general, try to follow the pattern of explaining an endpoint, the arguments it takes, what it returns, and an example of how to use it.

- [How to write API documentation](https://hackernoon.com/how-to-write-great-api-documentation-c710cd1c696).
- [Writing API documentation: best practices and examples](https://www.altexsoft.com/blog/api-documentation/).

### Generating API documentation
Even better than writing the documentation is generating the documentation for you. It also has the extra benefit that you won't have a discrepancy/outdated documentation if it is generated from your code.

In Rails, you can use the [rswag](https://github.com/rswag/rswag) gem to create specs that it can then convert into documentation and present it in an embedded version of [swagger-ui](https://github.com/swagger-api/swagger-ui) for easy browsing. This approach has the benefit of following TDD: you need to first write the specs and then they will be used to generate the documentation. So if at any moment there is a difference between implementation and documentation your tests should detect it.

- [Getting started with rswag](https://github.com/rswag/rswag#getting-started).
- [Documenting an API with rswag](https://medium.com/@sushildamdhere/how-to-document-rest-apis-with-swagger-and-ruby-on-rails-ae4e13177f5d).

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
