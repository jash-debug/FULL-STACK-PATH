# Fetch API data for React components

## Learning objectives

- Use the correct React hook when fetching data
- Connect to an API within a functional component
- Show different UI outputs depending on the component state

### Estimated time: 1h

## Description

In this lesson, you will learn how to make an asynchronous `HTTP request` to an external API in order to fetch data in a React component. You will also work with the React hook `useEffect` together with `useState` to update your local state.

### Why is fetching data from an API in React important?

A major responsibility of the front-end is to **fetch data from an API** to display it to the user. This is done by making an asynchronous HTTP request.

To do this in React, you should do it **right after a component has been rendered in the DOM**. Luckily for us, there is a special function that allows us to execute code after a component has been rendered: `useEffect`.

### A basic data fetch

The simplest version of fetching data in React looks like this _(try it out yourself!)_:

```jsx
import { useState, useEffect } from "react"

function App() {
  const [data, setData] = useState([])

  useEffect(() => {
    const fetchData = async () => {
      const res = await fetch("https://jsonplaceholder.typicode.com/todos")
      const json = await res.json()
      setData(json)
    }
    fetchData()
  }, [setData])

  return (
    <ul>
      {data.map((item) => (
        <li key={item.id}>{item.title}</li>
      ))}
    </ul>
  )
}

export default App
```

Learn more here:

- [Learn useEffect In 13 Minutes](https://www.youtube.com/watch?v=0ZJgIjIuY7U)
- [4 Ways To Fetch Data in React](https://www.youtube.com/watch?v=SbCedTlJWTs)

### Error and loading states

Whenever you're fetching data, you want to give the user **feedback on the progress**. That's why your component should be able to handle 2 additional states: **loading** and when there's an **error**.

- [Error and loading states](../articles/error_and_loading_states.md)

## Additional materials

- [Official documentation - Fetching data with Effects](https://beta.reactjs.org/reference/react/useEffect#fetching-data-with-effects)

**These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.**

---

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
