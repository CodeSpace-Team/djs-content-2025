# Conditional Rendering and UI States

React is built around the idea of reactive UIs — your components respond to changes in data or user actions. One of the most powerful techniques for doing this is **conditional rendering**: showing or hiding elements based on the current state.

In this lesson, you’ll learn how to conditionally display content in JSX using logical operators, and how to manage different UI states like loading, error, and empty results.

## Learning Objectives

By the end of this lesson, you will be able to:

- Use conditional logic to control what gets rendered in JSX.
- Apply logical operators like `&&` and ternary (`? :`) expressions inside JSX.
- Manage and represent different UI states such as loading, error, and empty views.
- Build components that adapt their output based on user interactions or app state.

## Rendering Based on State

Consider a scenario where you're fetching data or waiting for user input. You may need to render:

- A loading indicator while data is being fetched.
- An error message if something goes wrong.
- An empty state if no data is available.
- A list of results once the data is ready.

These UI variations are based on **state**, and you can use conditions to switch between them.

Example with flags:

```jsx
if (loading) return <p>Loading...</p>;
if (error) return <p>Error occurred!</p>;
if (data.length === 0) return <p>No results found.</p>;

return <DataList items={data} />;
```

## Logical Expressions in JSX

React allows you to use JavaScript expressions inside JSX using `{}`. You can write conditions using:

### 1. `&&` Operator

Use this to render something **only if** a condition is true.

```jsx
{
  items.length > 0 && <ItemList items={items} />;
}
```

If the condition is false, nothing is rendered.

### 2. Ternary (`? :`) Operator

Use this to render one of two options based on a condition.

```jsx
{
  isLoggedIn ? <Dashboard /> : <LoginPrompt />;
}
```

You can also use nested ternaries for multiple branches, though it’s best to keep them simple for readability.

### 3. Wrapping Conditional Blocks

You can also use traditional `if/else` logic in a function and return different JSX, or create helper functions for more complex conditions.

## Managing Multiple UI States

In real apps, you may have multiple conditions to represent different stages:

```jsx
if (isLoading) {
  return <LoadingSpinner />;
}

if (error) {
  return <ErrorMessage />;
}

if (data.length === 0) {
  return <EmptyState />;
}

return <ResultsList items={data} />;
```

Alternatively, you can use inline logic inside your JSX tree:

```jsx
<div>
  {isLoading && <p>Loading...</p>}
  {error && <p>Something went wrong.</p>}
  {!isLoading && !error && data.length === 0 && <p>No results.</p>}
  {!isLoading && !error && data.length > 0 && <ResultsList items={data} />}
</div>
```

## Practice Challenges: Show/Hide Elements and Conditionally Render Components

1. Build a basic component that toggles a message on and off when a button is clicked.

   ```jsx
   function ToggleMessage() {
     const [isVisible, setIsVisible] = useState(false);

     return (
       <div>
         <button onClick={() => setIsVisible((prev) => !prev)}>
           Toggle Message
         </button>
         {isVisible && <p>This is a conditional message.</p>}
       </div>
     );
   }
   ```

2. Build a data-driven list with fake loading state:

   ```jsx
   function DataFetcher() {
     const [isLoading, setIsLoading] = useState(true);
     const [items, setItems] = useState([]);

     useEffect(() => {
       setTimeout(() => {
         setItems(["Apple", "Banana", "Cherry"]);
         setIsLoading(false);
       }, 1500);
     }, []);

     if (isLoading) return <p>Loading...</p>;
     if (items.length === 0) return <p>No items found.</p>;

     return (
       <ul>
         {items.map((item, i) => (
           <li key={i}>{item}</li>
         ))}
       </ul>
     );
   }
   ```

## Summary

In this lesson, you learned how to make your components react to different application states using conditional rendering. Whether you're waiting for data, showing a message, or toggling visibility, conditional logic is essential for building dynamic user interfaces.
