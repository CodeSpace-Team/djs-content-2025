# Event Handling in React

Static UI can only go so far — real web applications are interactive. Users click buttons, submit forms, hover over elements, and more. To respond to these interactions, React offers a robust system of event handling that’s similar to vanilla JavaScript, but with some important differences.

In this lesson, you’ll learn how to use React’s event system to make your UI interactive.

## Learning Objectives

By the end of this lesson, you will be able to:

- Add event listeners to elements using React’s syntax.
- Write and bind event handler functions using arrow functions and named functions.
- Prevent default browser behavior during form submissions.
- Trigger updates or actions based on user interaction.

## Adding Event Listeners (onClick, onSubmit)

React uses camelCase syntax for event listeners:

- `onClick` for buttons or divs
- `onSubmit` for forms
- `onChange` for inputs

Example:

```jsx
function App() {
  function handleClick() {
    alert("Button was clicked!");
  }

  return <button onClick={handleClick}>Click Me</button>;
}
```

You can also use inline arrow functions:

```jsx
<button onClick={() => alert("Clicked!")}>Click Me</button>
```

## Arrow Functions vs. Declared Handlers

There are two common ways to handle events:

### 1. Declared (Named) Function

```jsx
function handleClick() {
  console.log("Handled via named function");
}
```

This approach is:

- Cleaner when reused across multiple elements.
- Easier to debug and test.

### 2. Arrow Function Inline

```jsx
<button onClick={() => console.log("Handled inline")}>Click</button>
```

Use inline arrow functions when:

- The logic is simple.
- You need to pass arguments:

      ```jsx
      <button onClick={() => handleClick(item.id)}>Delete</button>
      ```

  Avoid complex logic directly inside the `onClick` — instead, call a handler.

## Preventing Default Form Behavior

In React, submitting a form refreshes the page by default — just like in plain HTML. You need to prevent that manually:

```jsx
function handleSubmit(event) {
  event.preventDefault();
  console.log("Form submitted!");
}

function App() {
  return (
    <form onSubmit={handleSubmit}>
      <input type="text" placeholder="Enter name" />
      <button>Submit</button>
    </form>
  );
}
```

If you forget `event.preventDefault()`, your React app will reload when the form is submitted.

## Practice Challenge: Add Interactivity to a UI

Try the following:

1. **Add a Button**
   - Render a button in your component.
   - Add an `onClick` event that logs a message or updates state.
2. **Create a Form**
   - Create a simple form with an input and a submit button.
   - Add an `onSubmit` handler that logs the input value and prevents default behavior.
3. **Practice Both Approaches**
   - Use both named handler functions and inline arrow functions.
   - Pass custom data (e.g., `onClick={() => handleSelect(id)}`).

## Summary

You’ve now learned how to handle events in React, including `onClick` and `onSubmit`. You also learned the difference between declared and inline handlers, and how to prevent default browser behavior during form submission. These are essential skills for making your apps interactive and user-friendly.
