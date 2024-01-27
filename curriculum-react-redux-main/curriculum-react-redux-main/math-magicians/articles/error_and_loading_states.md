# Error and Loading states in functional components

It's important to give the user feedback whenever something is changing in the page. 2 essential states are the `loading` and `error` states.

#### Loading

Whenever an HTTP request is sent, you should show the user a "loading state".

The simplest version of the implementation consists of 2 parts:

- Create a state variable to track the loading state
  - Change its value before and after the HTTP request
- Prepare JSX to show while the component is waiting for the response to come back

```jsx
// Create a loading state variable
const [isLoading, setIsLoading] = useState(false)

// Prepare loading JSX
<div>Loading...</div>
```

Add it to the rest of your component:

```jsx
import { useState, useEffect } from "react"

function App() {
  const [data, setData] = useState([])
  const [isLoading, setIsLoading] = useState(false)

  useEffect(() => {
    const fetchData = async () => {
      setIsLoading(true)
      const res = await fetch("https://jsonplaceholder.typicode.com/todos")
      const json = await res.json()
      setData(json)
      setIsLoading(false)
    }
    fetchData()
  }, [setData, setIsLoading])

  if (isLoading) return <div>Loading...</div>

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

#### Error handling

A similar process applies to handling errors when making HTTP requests:

- Create a state variable to track the error state
- Prepare JSX to show when an error has been thrown

Keep in mind that you have to "catch" your errors in case they happen! This can be done easily using a `try/catch` block.

```jsx
// Create an error state variable
const [hasError, setHasError] = useState(null)

// Prepare error JSX
<div>Error! Try again</div>
```

Add it to the rest of your component:

```jsx
import { useState, useEffect } from "react"

function App() {
  const [data, setData] = useState([])
  const [hasError, setHasError] = useState(false)
  const [isLoading, setIsLoading] = useState(false)

  useEffect(() => {
    const fetchData = async () => {
      setIsLoading(true)
      try {
        const res = await fetch("https://jsonplaceholder.typicode.com/todos")
        const json = await res.json()
        setData(json)
      } catch (error) {
        setHasError(true)
      }
      setIsLoading(false)
    }
    fetchData()
  }, [setData, setIsLoading])

  if (hasError) return <div>Something went wrong!</div>

  if (isLoading) return <div>Loading...</div>

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

You could also inject the `error` message into the JSX, but that is up to the technical requirements!

Learn more here:

- [Loading Indicator and error handling](https://www.mariokandut.com/how-to-handle-errors-and-data-loading-state-with-react-hooks/)

---

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
