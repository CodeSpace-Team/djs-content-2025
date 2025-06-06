# From Vanilla JavaScript to JSX

React introduced a powerful shift in how we write front-end applications by moving away from imperative manipulation of the DOM to a declarative approach using JSX. To fully appreciate React, it’s essential to first understand the difference between imperative and declarative programming, and how JSX enables a smoother and more readable way to define UI structure.

In this lesson, we’ll compare traditional JavaScript with JSX and learn how JSX improves developer productivity and maintainability in modern web applications.

## Learning Objectives

By the end of this lesson, you will be able to:

- Explain the difference between imperative and declarative user interface design.
- Understand what JSX is and why it’s used in React.
- Identify and follow the syntax rules required when writing valid JSX.

## Declarative vs. Imperative UIs

In traditional JavaScript, building UI requires a lot of manual steps:

- Create elements using `document.createElement`.
- Set attributes and text content manually.
- Append elements to the DOM explicitly.
- Manually update or remove elements when the state changes.

This approach is **imperative**: the developer must specify every step the browser should take.

React, in contrast, uses a **declarative** model. You describe _what_ the UI should look like based on the current state, and React figures out how to update the DOM accordingly.

### Example Comparison

**Imperative (Vanilla JS):**

```js
const h1 = document.createElement("h1");
h1.textContent = "Hello, world!";
document.getElementById("root").appendChild(h1);
```

**Declarative (React JSX):**

```js
ReactDOM.createRoot(document.getElementById("root")).render(
  <h1>Hello, world!</h1>
);
```

Declarative code is often shorter, more readable, and better aligned with how UI should react to data changes over time.

## What JSX Is and Why It Exists

JSX (JavaScript XML) is a syntax extension to JavaScript that allows you to write HTML-like code within JavaScript files. Although browsers do not understand JSX directly, tools like Babel transpile JSX into regular JavaScript function calls (e.g., `React.createElement()`).

JSX provides:

- A familiar and readable syntax for developers with HTML/CSS experience.
- Full power of JavaScript via expressions inside JSX.
- Better tooling: syntax highlighting, linting, autocomplete.

JSX combines the **structure of HTML** with the **power of JavaScript**, enabling developers to write declarative UI code with ease.

## JSX Syntax Rules and Best Practices

JSX looks like HTML, but it has some important rules and differences:

### 1. Single Parent Rule

JSX expressions must have a single outer element. You cannot return multiple sibling elements unless they’re wrapped.

**Invalid JSX:**

```jsx
return (
  <h1>Hello</h1>
  <p>Welcome</p>
);
```

**Valid JSX:**

```jsx
return (
  <div>
    <h1>Hello</h1>
    <p>Welcome</p>
  </div>
);
```

Alternatively, you can use a React Fragment:

```jsx
return (
  <>
    <h1>Hello</h1>
    <p>Welcome</p>
  </>
);
```

### 2. Use `className` Instead of `class`

Since `class` is a reserved word in JavaScript, JSX uses `className` for CSS classes:

```jsx
<h1 className="hero-title">Welcome</h1>
```

### 3. CamelCase for Attributes

JSX uses camelCase for most attributes:

- `onClick` instead of `onclick`
- `tabIndex` instead of `tabindex`

### 4. Self-Closing Tags

Just like in HTML5, self-closing tags must be closed explicitly:

```jsx
<img src="logo.png" alt="Logo" />
<input type="text" />
```

### 5. JavaScript Expressions in Curly Braces

To insert JavaScript values into JSX, use `{}`:

```jsx
const name = "Chris";
return <h1>Hello, {name}!</h1>;
```

You can include any valid expression inside `{}`, such as math operations, function calls, or conditional logic.

## Summary

In this lesson, we saw how React’s declarative approach to UI is simpler and more powerful than traditional DOM manipulation. JSX provides a readable, expressive syntax that merges HTML-like structure with JavaScript logic. Understanding the core syntax rules of JSX is essential for writing reliable, scalable React
