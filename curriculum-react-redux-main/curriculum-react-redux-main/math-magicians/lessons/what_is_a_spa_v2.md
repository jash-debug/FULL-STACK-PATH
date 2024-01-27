# What is a Single Page App?

## Learning objectives

- Understand the concept of Single Page Application.

### Estimated time: 0.5h

## Description

In this lesson, you will deepen your knowledge about **Single Page Applications (SPAs)**. Single Page Applications were briefly introduced in [module 2](https://github.com/microverseinc/curriculum-javascript/blob/main/books/lessons/lesson_intro_spa.md#single-page-applications); now you will learn more about them.

### Why is a SPA important?

The traditional client-server model requires that **a browser sends out an HTTP request to the server whenever there is a page change**. These applications are called `static sites`, or `multi page applications (MPA)`.

This model works just fine, but there are some **disadvantages**:

- The user has to wait until the content has loaded.
- While desktop or native apps offer a continuous workflow, browser pages are constantly interrupted.
- Sometimes you only need to download a small piece of data, not the whole page.

A SPA attemps to solve these problems in the following ways:

| Problem                                              | Solution                                             |
| ---------------------------------------------------- | ---------------------------------------------------- |
| Download a new page from the server at every request | Download all the "pages" at the initial website load |
| Page only loads when all content has loaded          | Update only the content that needs to be updated     |

The traditional MPA vs SPA lifecycle can be summarized with this diagram:

<p align="center">
  <img src="../images/spa-vs-mpa.png" alt="SPA vs MPA"  width="500px"/>
</p>

<sub>Image credit: https://yalantis.com/blog/single-page-apps-vs-multiple-page-apps/</sub>

- [Understanding Single Page Applications and Multi Page Applications](https://www.youtube.com/watch?v=ZEpfiGu1f8g)

### SPA and AJAX

SPAs are built using regular JavaScript through a technique called **Asynchronous JavaScript and XML** (or AJAX).

It enables a web app to **make an HTTP request without reloading the whole page**. This is achieved by sending and receiving data _asynchronously_, using the [XMLHttpRequest object](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest).

Check the code snippets presented in [this article](https://attacomsian.com/blog/xhr-json-response). 
You can try them out in the browser's console!


However, this method of making asynchronous HTTP requests is outdated and nowadays we use the method [fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) method.

```javascript
fetch("https://jsonplaceholder.typicode.com/todos/1") // Send request
  .then((response) => response.json()) // Parse response
  .then((json) => console.log(json)) // Log response
```

- [AJAX with XMLHttpRequest](https://www.youtube.com/watch?v=mLL5pdIbqWc)
- [Fetch in Under Five](https://www.youtube.com/watch?v=FmpMIaukgfA)
- [Sending JavaScript HTTP Requests](https://www.youtube.com/watch?v=4K33w-0-p2c)

Some useful tips about AJAX:

- The term AJAX is used, in general, to talk about asynchronous requests.
- You can work with JSON or XML, not just XML.
- Most likely, you are not going to work with the XMLHttpRequest object directly.
- We recommend you work directly with the `fetch` API, since it's a fully supported standard.

### Libraries and frameworks to develop SPA

You can develop a SPA with only vanilla JavaScript, but that would mean a lot of work. To avoid reinventing the wheel, you can use a framework that will help you bootstrap your project and will give you the main features you need **out-of-the-box**. There are several options, the most popular of which are:

- [React](https://reactjs.org/)
- [Angular](https://angular.io/)
- [Vue](https://vuejs.org/)

In this module, you will learn how to work with **React**. All the frameworks listed are great, but we have chosen React because:

- It's the most popular
- Has a big community
- Easy to use documentation
- Lots of learning resources
- Its ecosystem offers everything you need to add additional features
- There is a great demand for React developers in the labor market

### SPA pages

A Single Page Application consists of a **single page** (1 HTML file), but that doesn't mean you can't have several pages or sections to categorize your content. For this purpose we have **routes**.

A traditional web site has several pages, **identified by the URL**. For example, you can have:

- `http://www.mycoolpage.com/home`
- `http://www.mycoolpage.com/about`
- `http://www.mycoolpage.com/contact`

SPAs can work with different URLs (modifying the `/home`, `/about`, or `/contact` part, in our example) using a **router**, which is software that modifies the URL of the browser. There are several routers available. You will learn about [React Router](https://reactrouter.com/en/main) in a following lesson.

### Cons of SPAs

SPAs can help you offer a more natural, continuous experience to users, but they also introduce some new problems. The **main problems** are:

- **Search Engine Optimization**

  Since the content of the page is generated or modified dynamically, search engines may have issues indexing your pages.

- **JavaScript is mandatory**

  In the (unusual, but possible) case of a browser not supporting JavaScript, the whole page will be unusable.

These problems can be solved, and there are tools you can use for it, but you should be aware of the potential pitfalls of SPAs and the strategies to fix them.

- [Single Page Applications (SPAs). Most Discussed Pros & Cons](https://novateus.com/blog/single-page-applications-spas-most-discussed-pros-cons/)

## Additional materials
-  AS SPAs rely heavily on client-side code, which can be manipulated by attackers through various techniques they are prone to XSS issues. Learn about this type of security problem by watching [this video](https://www.youtube.com/watch?v=DqK_OYat-3M).

---

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
