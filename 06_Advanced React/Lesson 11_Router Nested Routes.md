### Lesson: Router Nested Routes and Navigation

We now advance to nested routing and additional React Router features. Nested routing allows for complex UI structures, while Link and NavLink facilitate seamless navigation. We'll also examine how search parameters can filter content and manage state. This lesson extends your routing knowledge for more sophisticated application development.

### 4. Nested Routes

#### What is Nested Routing?
Nested routing refers to the concept of defining routes within routes. This hierarchical approach to routing allows for the construction of complex UI structures with parent-child relationships, where child routes are rendered within the context of their parent routes. Nested routes are particularly useful for applications that require multiple layers of navigation.

#### Implementing Nested Routes
React Router v6 makes nested routing straightforward. You define nested routes by placing `Route` components inside other `Route` components, matching the nested structure of your UI.

**Example:**
```jsx
import React from 'react';
import { Routes, Route } from 'react-router-dom';
import Layout from './components/Layout';
import Home from './components/Home';
import About from './components/About';
import User from './components/User';

function App() {
  return (
    <Routes>
      <Route path="/" element={<Layout />}>
        <Route index element={<Home />} />
        <Route path="about" element={<About />} />
        <Route path="user" element={<User />} />
      </Route>
    </Routes>
  );
}
```
In this example, `Layout` is a component that serves as a parent route containing nested routes for `Home`, `About`, and `User`. The `index` route corresponds to the default child route that renders when the user navigates to the parent route's path.

### 5. Link and NavLink

#### What is Link and NavLink?
`Link` and `NavLink` are components provided by React Router that allow you to create navigable links in your application. They enable the user to navigate between different routes without a full page refresh, maintaining the SPA experience.

- **Link:** Used for basic navigation between routes.
- **NavLink:** Similar to `Link` but includes styling attributes to indicate the active route.

#### Using Link and NavLink for In-App Navigation
To use `Link` or `NavLink`, simply import them from `react-router-dom` and use them in place of `<a>` tags for internal navigation.

**Example using Link:**
```jsx
import { Link } from 'react-router-dom';

function Navbar() {
  return (
    <nav>
      <Link to="/">Home</Link>
      <Link to="/about">About</Link>
    </nav>
  );
}
```
**Styling Active Links with NavLink:**
`NavLink` comes with a `className` prop that accepts a function. This function is called when the link is active, allowing you to style it differently.

**Example:**
```jsx
import { NavLink } from 'react-router-dom';

function Navbar() {
  return (
    <nav>
      <NavLink
        to="/"
        className={({ isActive }) => (isActive ? "activeLink" : "link")}
      >
        Home
      </NavLink>
      <NavLink
        to="/about"
        className={({ isActive }) => (isActive ? "activeLink" : "link")}
      >
        About
      </NavLink>
    </nav>
  );
}
```
In this example, `NavLink` automatically adds the "activeLink" class to the link corresponding to the current route, allowing for visual indication of the active route.

### 6. Search Params

#### Introduction to Search Parameters
Search parameters (also known as query strings) in the context of routing are used to pass optional information to a route through the URL. They follow the `?key=value` format and can be used for various purposes, such as filtering data or tracking page state without changing the route path.

#### Implementing and Using Search Parameters
To work with search parameters in React Router, you can use the `useSearchParams` hook, which allows you to read and modify the search parameters in the URL.

**Example:**
```jsx
import { useSearchParams } from 'react-router-dom';

function FilterPage() {
  let [searchParams, setSearchParams] = useSearchParams();
  
  const filter = searchParams.get('filter') || 'all';

  const updateFilter = (newFilter) => {
    setSearchParams({ filter: newFilter });
  };

  return (
    <div>
      <button onClick={() => updateFilter('all')}>All</button>
      <button onClick={() => updateFilter('active')}>Active</button>
      <button onClick={() => updateFilter('completed')}>Completed</button>
      <p>Current Filter: {filter}</p>
    </div>
  );
}
```
In this example, the application filters data based on the `filter` search parameter. The `useSearchParams` hook is used to access and update the URL's search parameters, allowing the app to dynamically change the displayed content based on user interaction.

Let's move on to Protected Routes. 