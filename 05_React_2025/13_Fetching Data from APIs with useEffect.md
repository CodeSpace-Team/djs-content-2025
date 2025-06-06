# Fetching Data from APIs with useEffect

Until now, you’ve worked with static data or user-generated inputs. But in real-world apps, most data comes from external sources — APIs, databases, or backend services. React doesn’t include built-in data-fetching tools, but you can use the browser’s `fetch()` API along with React's `useEffect` hook to handle these side effects.

In this lesson, you'll learn how to fetch data from a remote API, manage loading and error states, and display that data in your components.

## Learning Objectives

By the end of this lesson, you will be able to:

- Understand what `useEffect` is and how it's used for side effects.
- Fetch data from a public API and update component state with the result.
- Handle asynchronous behavior and display loading or error messages.
- Render a list of dynamic content based on fetched data.

## Introduction to useEffect for Side Effects

React components are primarily concerned with rendering UI. But sometimes, you need to perform **side effects**, like:

- Fetching data
- Setting up timers
- Subscribing to external services

For these situations, React provides the `useEffect` hook.

**Syntax:**

```jsx
useEffect(() => {
  // side effect logic here
}, []);
```

The empty array (`[]`) ensures the effect runs only once, when the component mounts.

## Fetching from JSONPlaceholder or Other Mock APIs

[JSONPlaceholder](https://jsonplaceholder.typicode.com/) is a free API you can use for testing. Let’s fetch a list of users.

Example:

```jsx
import { useState, useEffect } from 'react';

function UserList() {
  const [users, setUsers] = useState([]);
  const [isLoading, setIsLoading] = useState(true);
  const [hasError, setHasError] = useState(false);

  useEffect(() => {
    fetch('https://jsonplaceholder.typicode.com/users')
      .then(res => {
        if (!res.ok) throw new Error('Network response failed');
        return res.json();
      })
      .then(data => {
        setUsers(data);
        setIsLoading(false);
      })
      .catch(error => {
        console.error('Fetch error:', error);
        setHasError(true);
        setIsLoading(false);
      });
  }, []);
```

## Storing Fetched Data in State

You use `useState` to hold the fetched data so that it can be rendered:

```jsx
const [users, setUsers] = useState([]);
```

Once the data is fetched, call `setUsers(data)` to update state and trigger a re-render.

## Error and Loading State Management

Always track and manage both loading and error conditions when fetching:

- `isLoading`: Start as `true`, set to `false` once data or error is received.
- `hasError`: Start as `false`, set to `true` only if `.catch()` is triggered.

Use conditional rendering to reflect each state:

```jsx
if (isLoading) return <p>Loading users...</p>;
if (hasError) return <p>Error loading users.</p>;
```

## Practice Challenges: Fetch and Render a List of Posts or Users

1. Create a new component, such as `Posts` or `Users`.
2. Use `useState` to store:
   - Fetched data (`posts`, `users`, etc.)
   - Loading state (`isLoading`)
   - Error state (`hasError`)
3. In `useEffect`, fetch data from one of these:

   - https://jsonplaceholder.typicode.com/users

   - https://jsonplaceholder.typicode.com/posts

4. Display a loading message while fetching.
5. Show an error message if the fetch fails.
6. Once loaded, display the results in a list.

## Summary

In this lesson, you learned how to use `useEffect` to fetch data from an external API, store it in state, and render the result conditionally. You also practiced managing error and loading states, a crucial skill for building responsive web applications.
