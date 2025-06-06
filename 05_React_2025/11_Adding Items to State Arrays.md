# Adding Items to State Arrays

You’ve already learned how to render lists using `.map()` and how to use state and controlled inputs to capture user data. Now it's time to bring those ideas together in a real-world scenario: **building a dynamic list** where the user can add items on the fly.

This lesson focuses on how to update **arrays in state** using best practices and how to render them in response to user interaction.

## Learning Objectives

By the end of this lesson, you will be able to:

- Store an array in component state.
- Append new items to a state array using the spread operator.
- Avoid direct mutation of state.
- Render updated lists dynamically using `.map()`.

## Updating Arrays in State

To manage an array of values, initialize state like this:

```jsx
const [items, setItems] = useState([]);
```

To add a new item:

```jsx
setItems((prevItems) => [...prevItems, newItem]);
```

This uses the **spread operator** (`...`) to create a new array with the existing values plus the new one. This is important because:

- React state must remain **immutable**.
- Directly mutating state (e.g., `items.push(newItem)`) won’t trigger re-renders.

## Avoiding Mutation with the Spread Operator

### Incorrect (mutates state directly):

```jsx
items.push(newItem);
setItems(items); // Might not re-render!
```

### Correct (creates a new array):

```jsx
setItems((prev) => [...prev, newItem]);
```

This ensures React recognizes that state has changed and will re-render your component.

## Displaying Updated State with `.map()`

Once your array is in state, render it using `.map()` just like you did with static data:

```jsx
<ul>
  {items.map((item, index) => (
    <li key={index}>{item}</li>
  ))}
</ul>
```

For production apps, avoid using the array index as the key if items can be reordered or deleted. But for quick prototypes, it's acceptable.

## Practice Challenge: Build a Dynamic List from User Input

1. Create a component (e.g., `ToDoList` or `IngredientsForm`).
2. Use `useState` to track:
   - The input value (`text`)
   - The list of submitted items (`items`)
3. Create a controlled input:
   ```jsx
   <input
     value={text}
     onChange={(e) => setText(e.target.value)}
     placeholder="Add something..."
   />
   ```
4. On form submit:
   - Prevent default behavior
   - Add `text` to the `items` array
   - Clear the input
5. Display the list using `.map()`.

Example:

```jsx
function ListBuilder() {
  const [text, setText] = useState("");
  const [items, setItems] = useState([]);

  function handleSubmit(e) {
    e.preventDefault();
    if (!text.trim()) return;
    setItems((prev) => [...prev, text]);
    setText("");
  }

  return (
    <div>
      <form onSubmit={handleSubmit}>
        <input
          value={text}
          onChange={(e) => setText(e.target.value)}
          placeholder="Add item"
        />
        <button type="submit">Add</button>
      </form>

      <ul>
        {items.map((item, index) => (
          <li key={index}>{item}</li>
        ))}
      </ul>
    </div>
  );
}
```

## Summary

In this lesson, you learned how to dynamically build and render lists by combining state, forms, and rendering logic. You also practiced using the spread operator to safely update arrays in state — a key concept in React development.
