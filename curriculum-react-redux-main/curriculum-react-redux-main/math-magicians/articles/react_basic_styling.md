# Styling React Components

Adding CSS in React works slightly different than in regular HTML. Below you'll learn the **essential things** you need to know about how to style your React components.

## Classes

In React, you specify a CSS class with the `className` attribute. It works like the `class` attribute in regular HTML:

```jsx
<button className="button">Click Me</button>
```

## Styling: 2 methods

There are 3 primary ways of styling your components using CSS: **Inline styling**, **importing CSS** and **CSS modules**

- [Different Ways to Write CSS in React](https://css-tricks.com/different-ways-to-write-css-in-react/)
- [CSS Styles in React JS](https://www.youtube.com/watch?v=RYDXbp7vmjc)

### Method 1: Inline styling

This is the simplest way to add a style, using the `style` attribute of any JSX element. It takes an **object that includes CSS rules**:

```jsx
function Example() {
  return <div style={{ color: "red", backgroundColor: "green" }}>Example</div>
}
```

**IMPORTANT: only use the `style` attribute when your styles depend on JavaScript variables. Why? The [documentation recommends it](https://reactjs.org/docs/faq-styling.html#are-inline-styles-bad)**

To make your code cleaner you can put the object inside of a variable:

```jsx
function Example() {
  const styles = { color: "red", backgroundColor: "green" }
  return <div style={styles}>Example</div>
}
```

### Method 2: Importing CSS

You can write your styles in one or several `.css` files. You can write your CSS rules in the same way as usual:

```css
/* Button.css */
.button {
  background-color: #4caf50;
  border: none;
  color: white;
}
```

Then you can safely import the `.css` file into your component like so:

```jsx
import "./Button.css"

function Button() {
  return <button className="button">Click Me</button>
}
```

**IMPORTANT: Importing a CSS file in React is not possible using only regular JS. You need a tool like [Create React App](https://create-react-app.dev/) or [Vite](https://vitejs.dev/) to do it.**

### Method 3: CSS Modules

A `CSS module` is a regular CSS file that can be imported like an object. You start by speciyfing your stylesheet with the `.module.css` extension:

```css
/* Button.module.css */
.button {
  background-color: #4caf50;
  border: none;
  color: white;
}
```

You can then import this file into a component:

```jsx
import styles from "./Button.module.css"

function Button() {
  return <button className={styles.button}>Click Me</button>
}
```

**IMPORTANT: Importing a CSS file is not possible using only regular JS. You need a tool like [Create React App](https://create-react-app.dev/) or [Vite](https://vitejs.dev/) to do it.**

## Applying classes conditionally

The great thing about JSX is that **you can add logic to change the way your components behave**. This also applies to classes:

```jsx
function Button(props) {
  return (
    <button className={`button ${props.isActive ? "active" : ""}`}>
      Click Me
    </button>
  )
}
```

## Importing pre-processed CSS

Sometimes you want to use a CSS pre-processer like [SASS](https://sass-lang.com/), instead of regular CSS:

```jsx
import "./Button.scss"

function Button() {
  return <div className="button" />
}
```

Again, it depends on the build tool you're using. See the official documentation for more information on how to set that up:

- [Create React App](https://create-react-app.dev/docs/adding-a-sass-stylesheet/)
- [Vite](https://vitejs.dev/guide/features.html#css-pre-processors)

---

_If you spot any bugs or issues in this activity, you can [open an issue with your proposed change](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/open_issue.md)._
