# Component Architecture and State Lifting

As your React apps grow, you’ll encounter situations where multiple components need access to the same piece of data. This is where **state lifting** becomes essential. Instead of duplicating state or forcing data through unnecessary workarounds, React encourages you to move shared state up to the **nearest common ancestor**.

In this lesson, you'll learn when and how to lift state, how to pass data and event handlers between components, and how to structure your components for clean, maintainable architecture.

## Learning Objectives

By the end of this lesson, you will be able to:

- Identify when state should be lifted for shared access.
- Refactor components to move state into a common ancestor.
- Pass state and setter functions as props to child components.
- Apply best practices for organizing component relationships.

## State Lifting: When and Why

**Lifting state** means moving it up from one component to a parent so that multiple child components can share it.

You should lift state when:

- Two or more components need access to the same data.
- One component needs to update state that affects another.
- You want a parent to control its children's behavior through shared logic.

**Example Scenario:**

- A parent component renders a list.
- A child component adds new items.
- Another child component displays the list.

In this case, the list data should live in the parent and be passed down to both children.

## Sharing State Between Components

### Before Lifting (isolated state):

```jsx
function InputBox() {
  const [value, setValue] = useState("");
  return <input value={value} onChange={(e) => setValue(e.target.value)} />;
}

function Display() {
  return <p>No way to access the input above.</p>;
}
```

## After Lifting (shared state):

```jsx
function App() {
  const [value, setValue] = useState("");

  return (
    <>
      <InputBox value={value} onChange={(e) => setValue(e.target.value)} />
      <Display value={value} />
    </>
  );
}

function InputBox({ value, onChange }) {
  return <input value={value} onChange={onChange} />;
}

function Display({ value }) {
  return <p>Input: {value}</p>;
}
```

## Best Practices for Clean Component Structure

- Keep components **focused** — one responsibility per component.
- Only lift state as high as necessary.
- Avoid "prop drilling" by keeping component trees shallow when possible.
- Use **container/presenter** patterns if needed:
  - Container holds state logic.
  - Presenter focuses on rendering.

## Practice Challenge: Refactor a Multi-Component App to Lift Shared State

1. Start with a small app where:

   - One component captures input (`InputForm`)
   - Another displays the list (`ItemList`)
   - Each manages its own state separately

2. Refactor by:
   - Moving the list state up to the parent (`App`)
   - Passing the list and setter function as props
   - Handling submission and rendering from shared state

## Summary

In this lesson, you learned how to lift state to a shared parent component so that multiple children can access or modify it. You also practiced structuring components for clarity and reusability. These skills are essential for keeping your codebase manageable as your React projects grow in size and complexity.
