### Lesson: React Hooks

#### Objectives
By the end of this lesson, learners will be able to:
1. Understand the purpose and use of React Hooks in functional components.
2. Utilise basic hooks like `useState` and `useEffect` for state management and side effects.
3. Implement custom hooks for reusing logic across components.
4. Manage network requests within React components using hooks and handle response states.

#### Key Terms
- **React Hooks**: Functions that let you "hook into" React state and lifecycle features from function components.
- **useState**: A Hook that lets you add React state to functional components.
- **useEffect**: A Hook that lets you perform side effects in function components.
- **Custom Hooks**: Functions that start with `use` and call other hooks, allowing you to extract component logic into reusable functions.
- **Network Requests**: Operations to send or receive data from a server asynchronously within a component.
- **Loading State**: The interface indication that data is currently being fetched.
- **Error State**: The interface response when a network request fails.
- **Success State**: The interface update that shows the result of a successful network request.

Check out the official React Docs on Hooks: https://react.dev/reference/react/hooks 

#### 1. Introduction to Hooks

React Hooks are functions that let you "hook into" React's state and lifecycle features from within functional components. Introduced in React 16.8, hooks provide a more direct API to the React concepts you already know: props, state, context, refs, and lifecycle. They do not work inside classes — they let you use React without classes.

**Why Use Hooks?**

- **Simplicity**: Functional components with hooks are generally simpler and more concise than class components.
- **Reusability**: Hooks allow you to reuse stateful logic without changing your component hierarchy.
- **Organisation**: Hooks encourage more modular and flexible code by organising related logic into separate functions.

  
- **Functional Components with Hooks**:
  - Can use state and other React features without writing a class.
  - More concise and easier to read.
  - Example:
    ```javascript
    function Example() {
      const [count, setCount] = React.useState(0);

      React.useEffect(() => {
        document.title = `You clicked ${count} times`;
      });

      return (
        <button onClick={() => setCount(count + 1)}>
          Click me
        </button>
      );
    }
    ```

#### 2. Basic Hooks

**useState: Introduction and Syntax**

`useState` is a hook that lets you add state to functional components, the state can be of any data type

- Syntax: `const [state, setState] = React.useState(initialState);`
- Example:
  ```javascript
  function Counter() {
    const [count, setCount] = React.useState(0);

    return (
      <div>
        <p>You clicked {count} times</p>
        <button onClick={() => setCount(count + 1)}>
          Click me
        </button>
      </div>
    );
  }
  ```

**useEffect: Introduction, Use Cases, and Handling Side Effects**

`useEffect` is a hook that lets you perform side effects in functional components.

- Syntax: `React.useEffect(() => { /* Side effect */ }, [dependencies]);`
- Without cleanup:
  ```javascript
  React.useEffect(() => {
    document.title = `You clicked ${count} times`;
  });
  ```
- With cleanup:
  ```javascript
  React.useEffect(() => {
    const subscription = props.source.subscribe();
    return () => { // Cleanup
      subscription.unsubscribe();
    };
  }, [props.source]); // Only re-subscribe if props.source changes
  ```

**Discuss Cleanup and Dependencies**

- **Cleanup**: Some effects require cleanup to prevent memory leaks, such as subscribing to an external data source. The cleanup function is returned at the end of the effect.
- **Dependencies**: The second argument to `useEffect` is an array of dependencies. React will only re-run the effect if any of the dependencies have changed. Omitting this argument means the effect runs after every render. An empty array means the effect runs once after the initial render.


### 3. Custom Hooks

Custom Hooks are a powerful feature in React that allows you to extract component logic into reusable functions. This approach helps in creating cleaner, more readable, and maintainable components by sharing logic across them.

#### Concept of Reusing Logic with Custom Hooks

The main idea behind custom hooks is to take advantage of the hooks mechanism to encapsulate logic that can be reused across multiple components. This not only helps in avoiding duplication but also promotes a more modular and scalable application architecture.

#### Examples

**useFormInput**: Simplifies handling form inputs by managing the state and changes for an input field.

```jsx
function useFormInput(initialValue) {
  const [value, setValue] = React.useState(initialValue);

  function handleChange(e) {
    setValue(e.target.value);
  }

  return {
    value,
    onChange: handleChange,
  };
}
```

**useFetch**: A custom hook for making network requests, managing the loading state, and handling responses.

```jsx
function useFetch(url) {
  const [data, setData] = React.useState(null);
  const [loading, setLoading] = React.useState(true);
  const [error, setError] = React.useState(null);

  React.useEffect(() => {
    const fetchData = async () => {
      try {
        const response = await fetch(url);
        const data = await response.json();
        setData(data);
      } catch (error) {
        setError(error);
      } finally {
        setLoading(false);
      }
    };

    fetchData();
  }, [url]);

  return { data, loading, error };
}
```

### 4. Fetching Data with Hooks

#### Using `useEffect` for Network Requests

`useEffect` is commonly used for executing side effects in functional components, which includes fetching data from APIs. This hook runs after the first render and after every update, depending on the dependencies you specify.

#### Managing Loading, Error, and Success States

To provide a good user experience, it's crucial to manage the loading, error, and success states when fetching data. This helps users understand what's happening and if they need to take any action.

#### Demonstration with a Contact Form Example

Consider a contact form where users submit their email and a message. The form submission involves posting the data to a server and handling the response appropriately.

```jsx
function ContactForm() {
  const [email, setEmail] = React.useState('');
  const [message, setMessage] = React.useState('');
  const [status, setStatus] = React.useState('idle');

  async function handleSubmit(event) {
    event.preventDefault();
    setStatus('loading');

    try {
      const response = await fetch('/api/contact', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ email, message }),
      });

      if (!response.ok) throw new Error('Network response was not ok');
      setStatus('success');
    } catch (error) {
      setStatus('error');
    }
  }

  return (
    <form onSubmit={handleSubmit}>
      {/* Form fields and submission button */}
    </form>
  );
}
```

#### Introduction to SWR for Data Fetching

SWR is a React hook library for data fetching, which simplifies handling data synchronization, caching, revalidation, and more. It provides a more intuitive and efficient way to fetch, cache, and update data in your React applications with minimal code.

```jsx
import useSWR from 'swr';

function Profile() {
  const { data, error } = useSWR('/api/user', fetcher);

  if (error) return <div>Failed to load</div>;
  if (!data) return <div>Loading...</div>;
  return <div>Hello, {data.name}</div>;
}
```

This section has elaborated on creating custom hooks for reusing logic, effectively fetching data using hooks, and managing response states, with an introduction to the SWR library for efficient data fetching and state management in React.


## Extra Resources
React Hooks Crash Course by DevelopedbyEd
https://www.youtube.com/watch?v=9mTgKFjJRXg

Learn React Hooks: useEffect by Cosden Solutions
https://www.youtube.com/watch?v=-4XpG5_Lj_o

Learn React Hooks: useState by Cosden Solutions
https://www.youtube.com/watch?v=V9i3cGD-mts

10 React Hooks Explained by Fireship
https://www.youtube.com/watch?v=TNhaISOUy6Q&t=323s

useSWR Hook Documentation: https://swr.vercel.app/docs/getting-started



#### Possible Exercise: Create a `useWindowWidth` Custom Hook

This exercise aims to create a custom hook that tracks the window width, allowing components to respond to window resizing.

```jsx
function useWindowWidth() {
  const [width, setWidth] = React.useState(window.innerWidth);

  React.useEffect(() => {
    const handleResize = () => setWidth(window.innerWidth);
    window.addEventListener('resize', handleResize);
    return () => window.removeEventListener('resize', handleResize);
  }, []);

  return width;
}
```















