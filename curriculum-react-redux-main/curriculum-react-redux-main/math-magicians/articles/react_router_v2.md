# Routing with React Router

## Routing

First of all, what is a **route**? It's a section of the web application (usually a page). For example, when you navigate to the `/contact` route of a website, you can expect all the content that has to do with contact information (like a contact form) would be loaded.

**Routing** is the act of programmatically manipulating a URL in order to send the user to different locations inside of a website. For example, right after a user has submitted the contact form, they would be **routed** to a thank you page (`/thank-you`).

This behavior is crucial to **logically separating parts** of an application. It's much easier to navigate [LinkedIn](https://www.linkedin.com/) if you have a route dedicated to, for example:

- [Your feed](https://www.linkedin.com/feed)
- [Your profile](https://www.linkedin.com/in/yourprofilename)
- [Your suggested jobs](https://www.linkedin.com/jobs/)

Imagine if there were no routes and everything would have to fit within the same page. It would be a chaos to navigate!

### Server-side routing vs. client-side routing

**Routing traditionally happens on the server-side**. Whenever a user goes to a certain endpoint, let's say it's `/account` a GET request will be send to the server to a route with a similar name (i.e. `/api/account`). The server then responds with an HTML page and any other associated assets.

In a Single Page Application (SPA) routing doesn't exist, because **everything happens within the same HTML file**. However, this **produces a bad user experience**; what if you like to nagivate to the `/about`, `/account` or `/cart` pages directly? You would have to navigate through many different parts of the website manually just to get to where you want to go!

With the arrival of Single Page Applications there became a need to distinguish between routing done on the server, now named `server-side routing`, and routing done on the client, named `client-side routing`.

Client side routing allows our app to **update the URL without requesting another document from the server**.

- [Client-side vs Server-side, Front-end vs Back-end?](https://www.youtube.com/watch?v=7GRKUaQ8Spk)

## React Router

With React you build Single Page Applications, and so **it doesn't allow us to change the URL to navigate to different pages**. If we do want to have it, we would have to add that functionality ourselves.

Luckily for us, **the React community has come up with many different solutions**. The most popular one is called [React Router](https://reactrouter.com/en/main/start/concepts) and this is what you'll learn about now.

### Quickstart

First, initialize a new React application using [Create React App](https://reactjs.org/docs/create-a-new-react-app.html#create-react-app)

```sh
npx create-react-app my-app
```

Second, install **React Router**:

```sh
npm install react-router-dom
```

Third, replace the content of your `App.js` with this snippet:

```javascript
// App.js
import { Outlet, Route, Routes } from "react-router"
import { BrowserRouter } from "react-router-dom"
import "./App.css"

function Layout() {
  return (
    <>
      <h1>Layout</h1>
      <Outlet />
    </>
  )
}

function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<Layout />}>
          <Route index element={<div>Home page</div>} />
          <Route path="about" element={<div>About page</div>} />
          <Route path="*" element={<div>If page not found it goes here</div>} />
        </Route>
      </Routes>
    </BrowserRouter>
  )
}

export default App
```

_Try this yourself inside of a fresh install of a React application!_

In this example:

- The [BrowserRouter](https://reactrouter.com/en/main/router-components/browser-router) takes control of the browser's routing functionality
- The [Routes](https://reactrouter.com/en/main/components/routes) is a container that stores all of the individual [Route](https://reactrouter.com/en/main/route/route) components
- The [Route](https://reactrouter.com/en/main/route/route) is a URL that will render the specified `element`

Learn more here about React Router here:

- [Learn React Router v6 In 45 Minutes](https://www.youtube.com/watch?v=Ul3y1LXxzdU)
- [Follow the official tutorial](https://reactrouter.com/en/main/start/tutorial).
- [Look at some code examples in Vite](https://github.com/remix-run/react-router/tree/dev/examples)

---

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
