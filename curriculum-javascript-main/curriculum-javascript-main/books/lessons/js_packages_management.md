# JavaScript packages management


## Learning objectives

- Use npm as a software packages system.

### Estimated time: 1h

## Description

In this lesson, you will learn how to use code prepared by someone else in your project in an efficient way by using packages manager.

### Why is it important?

If you can make use of someone else's code in order to build your application, there is no need to reinvent the wheel. This reusing of code is considered a good practice. 

A collection of reusable code that can provide your application extra functionality is called a **package**. However, it's sometimes also called a **library** or **dependency**.

You can access packages other developers have written through a **package manager**, which is CLI tool that allows you to download and install them to your local machine.


### Package manager

First, read about [dependencies in your project](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Understanding_client-side_tools/Package_management#a_dependency_in_your_project).

Then read the part [What exactly is a package manager?](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Understanding_client-side_tools/Package_management#what_exactly_is_a_package_manager) to get a general idea of this concept.

### npm as a package manager

- `npm` is associated with node.js and it might be confusing. Therefore first read the following fragment [Why Do You Need Node for a Front End Project?](https://www.freecodecamp.org/news/how-to-set-up-a-front-end-development-project/#why-do-you-need-node-for-a-front-end-project)
- Then, read ["What is npm?"](https://docs.npmjs.com/about-npm) and ["What is npm?" by w3schools](https://www.w3schools.com/whatis/whatis_npm.asp)
- npm is installed with Node.js. This means that you have to install Node.js to get npm installed on your computer.
    - [Download it](https://nodejs.org/en/download/) 
    - Verify installation
    ```
      node -v
      npm -v
    ```


**Spoiler alert:** Above we are pointing you to the specific parts of the article "How to Set Up a Front End Development Project". You can see in that article also a part about Webpack. Please ignore it, for now, you will learn about Webpack in a separate lesson.


### ES6 modules and packages

Now, let's think for a while about ES6 modules. Remember how you can import your modules? Here is the good news: you can also import modules from external code that you add to your project as a package.
Take a look at the example of the Three.js library: [Install from npm](https://threejs.org/docs/index.html#manual/en/introduction/Installation). In order to use its functions you need to:

- Install it with npm:
```
npm install --save three
```
- Import it in your code:

```
import * as THREE from 'three';
```

### Organizing your ES6 code

With external packages and your own modules, you can organize your frontend code in a better way.
-  Check [How to Add Libraries to Your JavaScript Project](https://www.freecodecamp.org/news/how-to-set-up-a-front-end-development-project#how-to-add-libraries-to-your-javascript-project) to see an example of a well-structured project.


**Spoiler alert:** Above we are pointing you to the specific parts of the article "How to Set Up a Front End Development Project". You can see in that article also a part about Webpack. Please ignore it, for now, you will learn about Webpack in a separate lesson.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
