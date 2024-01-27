# Props & state

## Learning objectives

- Use React state.
- Use React props.

### Estimated time: 0.5h

## Description

In this lesson, you will learn what React **state** and **props** are and how to work with them.

### State

State is **data that can be updated** through:

- User interaction (click, select, typing, drag and drop, etc.)
- Programmatically (a timer finishes, a request to a server is resolved, etc.)

**State management** is the concept of _adding_, _updating_, _removing_ and _reading_ pieces of state in an application.

Here's how it looks in code:

```javascript
function Cat() {
  const [isSleeping, setIsSleeping] = useState(false)

  const wakeUpCat = () => {
    setIsSleeping(true)
  }

  return (
    <div>
      <p>{`The cat is ${isSleeping ? "sleeping" : "awake"}`}!</p>
      <button onClick={wakeUpCat}>Wake up!</button>
    </div>
  )
}
```

In this example, the `Cat` component has a `isSleeping` state. Note that it can change when clicking on the button.

### Props

Props are **custom attributes given to components**, which can be used to pass **data to a component as input**.

It works the same as passing arguments to a function, only instead of declaring parameters **you declare your own attributes on a component instance**.

Here's an example of a component receiving data through the `name` props:

```javascript
function Parent() {
  return (
    <>
      <Child name="Alusine" />;
      <Child name="Fatma" />;
    </>
  )
}

function Child(props) {
  return <div>My name is {props.name}!</div>
}
```

In the `<Child />` component, `name` is received from a `<Parent />` and can be displayed in the user interface.

### Props vs state

A component may use only props (like in the previous example), only state, or both state and props. You should decide what is better in depending on the circumstance:

```javascript
function Cat ({ timeToEat }) {
  return <p>{`I'm ${timeToEat ? "happy" : "sad"} now!`}</p>;
} 

function CatGroup() {
  const [isTimeToEat, setIsTimeToEat] = useState(false);

  const alertCats = () => setIsTimeToEat(true);

  return (
    <div>
      <Cat timeToEat={isTimeToEat} />
      <Cat timeToEat={isTimeToEat} />
      <Cat timeToEat={isTimeToEat} />
      <button onClick={alertCats}>
        Time to eat!
      </button>
    </div>
  )
}
```

State is usually defined in the parent component, as seen in `<CatGroup />`. It is then passed down through props, `timeToEat`, to each instance of `<Cat />

## Additional materials

**These are all optional, but if you're interested in exploring this topic further, here are some resources to help you. Any exploration here should be done outside program time.**

To learn how to architect your components, props, and state in the _react way_, read the [Thinking in React](https://reactjs.org/docs/thinking-in-react.html) guide.

Read this article: [React.js for beginners — props and state explained](https://www.freecodecamp.org/news/react-js-for-beginners-props-state-explained/) for a deeper explanation and examples of how to work with state and props.

When working with **forms**, form elements usually mantain their own state, updating it on user input. They are called _controlled components_. Read how to work with them in the [Forms](https://reactjs.org/docs/forms.html) guide.

---

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
