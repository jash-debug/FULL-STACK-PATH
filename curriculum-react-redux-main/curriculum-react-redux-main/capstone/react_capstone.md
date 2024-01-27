# React capstone project - Metrics webapp

## Learning objectives

- Use React documentation.
- Use React components.
- Use React props.
- Use React Router.
- Connect React and Redux.
- Handle events in a React app.
- Write integration tests with a React testing library.
- Use styles in a React app.
- Use React life cycle methods.
- Apply React best practices and language style guides in code.
- Use store, actions and reducers in React.

### Estimated time: 18.5h

## Description

This React capstone project ([remember what they are?](https://github.com/microverseinc/curriculum-html-css/blob/main/articles/capstone_intro.md))is about building a mobile web application to check a list of metrics (numeric values) that you will create making use of React and Redux. 

You will select an API that provides numeric data about a topic that you like and then build the webapp around it. The webapp will have several pages:
- one page with a list of items that could be filtered by some parameters; in the example below, it's a list of metrics that can be filtered by the country (imagine a search field to introduce the country name like Italy, Croatia, etc.). This page should be your homepage.
- one page for the item details; in the example, the detail page for Czech Republic cities with number of views.

<p align="center">
  <img src="./images/metrics_app.png" alt="Home page" />
</p>

*IMPORTANT NOTE: Read **all** requirements before you start building your project.*

### General requirements

- Make sure that there are [no linter errors](https://github.com/microverseinc/linters-config).
- Make sure that you used correct [Gitflow](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/gitflow.md).
- Make sure that you documented your work [in a professional way](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/documentation/articles/professional_repo_rules.md).

### HTML/CSS & JavaScript requirements

- Follow our list of [best practices for HTML & CSS](https://github.com/microverseinc/curriculum-html-css/blob/main/articles/html_css_best_practices.md).
- Follow our list of [best practices for JavaScript](https://github.com/microverseinc/curriculum-html-css/blob/main/articles/javascript_best_practices.md).

### Project requirements

**API**
First you need to choose an API to base the development of the webapp on. The API should allow you to get numeric values based on a parameter. We recommend that you choose an API that is open or needs an API key. If you choose an API that require authentication, **you should implement it on your own**. 

  Some example APIs are:
  - [Financial modeling prep API](https://financialmodelingprep.com/developer/docs/): stock data.
  - [Air pollution API](https://openweathermap.org/api/air-pollution): air quality data.

  You can find many APIs in [this GitHub repo](https://github.com/public-apis/public-apis). Some of the APIs requires a token for authentication and some others are just open.

**Design**
- You should follow these [design guidelines](https://www.behance.net/gallery/31579789/Ballhead-App-(Free-PSDs)), including:
  - Colors (select one main color for your website).
  - Typography: font face, size and weight.
  - Layout: composition and space between elements.

Original design idea by [Nelson Sakwa on Behance](https://www.behance.net/sakwadesignstudio).

The [Creative Commons license of the design](https://creativecommons.org/licenses/by-nc/4.0/) requires that you give appropriate credit to the author. Therefore, you must do it in the README of your project.

**Interactions**
- Home page
  - When the page loads, the webapp shows the list of categories that could be filtered out by some parameter, for example by the category name.
  - Along with the category name, you will display some numeric values per category that come from the API.
  - When the user clicks (or taps) on a category item, the application navigates to the details page.

- Details page
  - In the details page, the webapp retrieves data from the API to show detailed data in the category.
  - When the user clicks on the "Back" button (<), the user navigates to the home page.

**Testing requirements**
- Create unit tests for pure functions in your Redux code.
- Create integration tests for your application using the React Testing Library.
  - You may need to mock the access to the API, so that your tests don't send actual requests.
  - You may need to mock the connection to the Redux Store.

**Technical requirements**

- The project is a single-page application (SPA) built with React and Redux.
- The data retrieved from the API should be stored in the Redux store.
- You should filter the data that you retrieve from the API using a Filter stateless component.
- Every page (the main page and the pages for each item) should have a unique route within the SPA.
- The project should be deployed and accessible online using [Render](https://render.com), [Netlify](https://www.netlify.com/) or [GitHub Pages](https://pages.github.com/).
  - Add a link to the online version of your app to your README file.

### Project documentation

Once you have finished the development of the project, you should record a video presenting the features of the project you built. It is a video with a **maximum length of 5 minutes**. The content of the video should include:

- a description of the project.
- a demo of the project features.
- you should also highlight some interesting piece of code or something you built that you are very proud of.

For recording the video you can use tools like [Loom](https://www.loom.com/) that let you share a private link to the recording, and configure a shot that shows your computer screen and your face at the same time in a small picture.

## Challenge breakdown

Here is a suggestion of what you can do every day (just a suggestion, not mandatory):

### Day 1
- Select the API you are going to use. 
- Build files structure for your React app. 
- Prepare routes and navigation in your app.

### Day 2

- Make sure that a user can display a list of items and filter them. Data should come from the API.
- Create the tests for the application.

### Day 3

- Style your components to match the design provided.
- Deploy the project and test for final details.
- Record a video for your project.
- Create a good README and PR description.


## Work and submission mode

- You should submit this activity **individually.**

## Code review

You will get a code review when you build the complete project, not after each milestone. Once you have it ready, follow [these steps](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/code-review/articles/how_to_ask_for_a_code_review.md) to request a code review of your project.

## Submit your project

After the final approval from a code reviewer, you need to submit your project.
[Read this FAQ for a reminder on how to submit your project](https://microverse.zendesk.com/hc/en-us/articles/360061344234).

Now go to your Student Dashboard and submit your project.

## Additional requirements

*These are all optional, but if you're interested in exploring this topic further, feel free to implement them. Any exploration here should be done outside program time.*

*If you decide to implement these requirements you should do it in a separate pull request. As always, remember to clearly document your decision in GitHub comments.*

- You could implement some UX improvements: include transitions and/or animations, etc.
- You can implement additional pages in the website (each with a route in the SPA): about me, references, etc.
- Make sure that you have a decent desktop design for the webapp.

------

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
