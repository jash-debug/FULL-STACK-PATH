# Authorization

## Learning objectives
- Describe the difference between authorization and authentication.
- Limit access to web app resources based on authorization rules.

### Estimated time: 1.5h

## Description
In this lesson, you will learn about authorization, how it differs from authentication, and a popular gem to implement in your RoR project.

### Why is authorization important?
Because authorization is a core part of most, if not all, applications you will develop. There is always a resource that can only be accessed/modified by certain users (e.g. tweets can only be deleted by owner) or a part of a system that should only be accessed by certain users (e.g. admin panel).

**Guiding questions:**

*Think about this question as you learn about authorization:*

- How would you prevent a user from accessing private resources owned by another user?

### Authorization
Authorization is an access right to a certain resource. In the context of web development and CRUD actions, it defines if a given user can create, read, update, and/or delete a certain resource. Another common name for this is "access control".

This is in contrast to authentication which is a validation of identity, confirming that a user is in fact that user. Usually, you proof this by the combination of username/email and password, and maybe a 2FA step.

To learn more about the difference between authentication and authorization, read the two links below:
- [What is authorization?](https://auth0.com/intro-to-iam/what-is-authorization/)
- [Authentication vs authorization](https://www.okta.com/identity-101/authentication-vs-authorization/)

### RoR Authorization
As with authentication, authorization is one of those things that it is better not to implement yourself for security concerns. It's better to use battle-tested open libraries like [CanCanCan](https://github.com/CanCanCommunity/cancancan).

Unlike authentication, authorization is a more custom solution since it can depend a lot on your business rules. So libraries provide a general framework and helpers which you can then use to implement your authorization rather than a plug-and-play solution like authentication ones. The upside is that a library (in this case CanCanCan) will work to solve any problem and you don't need plugins or extra dependencies.

- [CanCanCan](https://github.com/CanCanCommunity/cancancan)
- [Authorization with CanCanCan](http://tutorials.jumpstartlab.com/topics/auth/authorization.html)
    - You do not need to complete the tutorial - it is enough if you read it and keep it as a refrence for your next project (in which you will need to use CanCanCan). If you decide to give it a try though - make sure that you install the newest version of the cancancan gem (as version in the tuotorial might give you some bugs).
- [CanCanCan: best practices](https://github.com/CanCanCommunity/cancancan/blob/develop/docs/define_abilities_best_practices.md)

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
