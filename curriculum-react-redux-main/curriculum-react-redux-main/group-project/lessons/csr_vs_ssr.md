# Client-side rendering vs. Server-side rendering

## Learning objectives

- Learn to distinguish between the differences between Client-side rendering (CSR) & Server-side rendering (SSR)
- Get familiar with Next.js

### Estimated time: 1h

## Description

In this lesson you'll learn the differences between Client-side rendering (CSR) & Server-side rendering (SSR), as well as one popular solution to build React applications that use SSR: [Next.js](https://nextjs.org/)

### Why is it important?

Once the application code has been generated in a way that the browser can actually run, the next question is where you decide to do this: in the browser or server?

Understanding what happens behind the scenes of the rendering process will allow you to know how to build more performant SPAs.

### Ingredients for a SPA

Building Single Page Applications in React usually includes:

- **JavaScript transpiling**, which is the conversion of a fairly new version of JavaScript (that’s not yet supported by most browsers) into an older version (that is supported). The leading tool for this is [Babel](https://babeljs.io/)
- **Module bundling**, which is the optimizing and putting together of various modules and dependencies into one or few big modules. This is usually done with a tool like [Vite](https://vitejs.dev/) or [Webpack](https://webpack.js.org/)

This is needed to generate the files the browser will run in order to actually initiate the process of rendering. But how will the browser then go about rendering the application for a user to be able to interact with it?

### Client-side rendering (CSR) vs. Server-side rendering (SSR)

The two biggest rendering strategies arre CSR and SSR.

#### Client-side rendering (CSR)

![CSR](https://www.growth-rocket.com/wp-content/uploads/2020/07/Client-Side-Rendering-Flowchart.jpg)

CSR refers to the rendering of the application on the _client-side_, i.e. within the user's browser.

In this approach, the initial HTML is sent from the server to the browser, and the **JavaScript code is then executed to render the application dynamically**.

This results in a fast and responsive user experience as the browser can handle the rendering process.

#### Server-side rendering (SSR)

![SSR](https://www.growth-rocket.com/wp-content/uploads/2020/07/Server-Side-Rendering-Flowchart.jpg)

SSR involves rendering the application on the server before sending it to the browser.

The **server generates the HTML for the initial view and sends it to the browser**, which then updates the content dynamically as the user interacts with the application.

This approach is particularly useful for applications that need to be indexed by search engines or for those that need to provide an initial view to users with slow internet connections.

Learn more here:

- [A Closer Look at Client-Side & Server-Side Rendering](https://www.growth-rocket.com/blog/a-closer-look-at-client-side-server-side-rendering/)
- [What are Server Side Rendering (SSR) & Client Side Rendering (CSR) | Pros + Cons](https://www.youtube.com/watch?v=ObrSuDYMl1s)

#### SSR in React with Next.js

One of the major downsides of using _client-side rendering_ is the [loss of SEO results](https://www.youtube.com/watch?v=-B58GgsehKQ), as well as a slow [First Contentful Paint (FCP)](https://web.dev/fcp/); both which are crucially important for a business.

As a result, the React community has produced several SSR frameworks. The most popular is [Next.js](https://nextjs.org/).

Learn more here:

- [Next.js in 100 Seconds](https://www.youtube.com/watch?v=Sklc_fQBmcs)
- [Next.js For React Developers](https://www.youtube.com/watch?v=omV9GEpQUGk)

---

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
