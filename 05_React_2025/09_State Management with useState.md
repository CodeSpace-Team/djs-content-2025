# State Management with useState

Up to this point, you’ve passed data to components using props, which are great for passing information down from a parent. But what if a component needs to track and update its own data — such as toggling visibility, changing text, or capturing user input?

That’s where **state** comes in. In this lesson, you’ll learn how to use React’s `useState` hook to add dynamic behavior to your components.

## Learning Objectives

By the end of this lesson, you will be able to:

- Understand the difference between props and state.
- Use the `useState` hook to add interactivity to components.
- Recognize what causes React to re-render.
- Track and display changing data in the UI.

## Learning Resource (Lessons 9 - 14)

**Scrimba Course**: [React State](https://scrimba.com/learn-react-c0e/~0z7t)

## Difference Between Props and State

| Props                        | State                       |
| ---------------------------- | --------------------------- |
| Passed from parent           | Defined inside component    |
| Read-only                    | Can be updated (mutable)    |
| Controlled by parent         | Controlled by the component |
| Used to configure components | Used to manage local data   |

Think of **props** as external inputs and **state** as internal memory.

Props do not change unless the parent changes them. State is updated by the component itself in response to events.

## useState Syntax and Rules

To use state in a component, you call the `useState` hook:

```jsx
import { useState } from "react";

function App() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times.</p>
      <button onClick={() => setCount(count + 1)}>Click Me</button>
    </div>
  );
}
```

### Key Concepts:

- `useState` returns an array with two elements:
  - The **current value** of the state.
  - A **setter function** to update that value.
- You must call `useState` **at the top level** of your component — not inside loops or conditionals.
- State updates trigger a `re-render` of the component.

## What Triggers a Re-render

A React component re-renders when:

- Its **state changes** (via a `setX` call).
- Its **props change**.
- A **parent** component re-renders and passes in new props.

Only the affected component and its children re-render — React’s diffing algorithm ensures efficient updates.

## Practice Challenges: Create Toggle Buttons and Input Displays Using State

### 1. Toggle Button

Create a component that toggles between “ON” and “OFF” each time it’s clicked.

```jsx
import { useState } from "react";

function Toggle() {
  const [isOn, setIsOn] = useState(false);

  return <button onClick={() => setIsOn(!isOn)}>{isOn ? "ON" : "OFF"}</button>;
}
```

### 2. Track Input Value

Create a component that shows the current value of a text input as you type.

```jsx
import { useState } from "react";

function InputTracker() {
  const [text, setText] = useState("");

  return (
    <div>
      <input
        type="text"
        onChange={(e) => setText(e.target.value)}
        placeholder="Type something..."
      />
      <p>You typed: {text}</p>
    </div>
  );
}
```

## Summary

In this lesson, you learned how to manage dynamic data within components using the `useState` hook. State enables your components to respond to user interaction and re-render with updated information. Understanding how and when state causes re-renders is key to mastering React’s reactivity.
