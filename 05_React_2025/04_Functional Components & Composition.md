# Functional Components & Composition

React is built around components — small, reusable pieces of code that represent parts of the user interface. By breaking an application into components, you can create more organized, scalable, and maintainable code.

In this lesson, you’ll learn how to write functional components, import them into other components, and structure a basic app layout using a parent-child hierarchy.

## Learning Objectives

By the end of this lesson, you will be able to:

- Write functional React components that return JSX.
- Compose a user interface using multiple components.
- Understand how data and structure flow from parent to child components.

## Writing Functional Components

A **functional component** in React is simply a JavaScript function that returns JSX. These components are the building blocks of every React application.

Here’s the basic structure of a functional component:

```jsx
function Header() {
  return <h1>Welcome to My App</h1>;
}
```

Or using arrow function syntax:

```jsx
const Header = () => {
  return <h1>Welcome to My App</h1>;
};
```

All component names must start with an **uppercase letter**. This is how React knows it’s a component and not a native HTML tag.

Each component can return a single JSX element or multiple elements wrapped in a container:

```jsx
const Main = () => (
  <main>
    <h2>Get Started</h2>
    <p>This is the main content area.</p>
  </main>
);
```

## Importing and Composing Components

Components can and should be placed in separate files to keep code organized.

To use a component from another file:

1.  Export it from its file:

    ```jsx
    // Header.jsx
    export default function Header() {
      return <h1>My App</h1>;
    }
    ```

2.  Import it where you want to use it:

    ````jsx
    // App.jsx
    import Header from './Header';

    function App() {
      return (
        <div>
          <Header />
        </div>
      );
    }
      ```

    This is called **composition** — assembling your UI by combining smaller parts.
    ````

## Parent-Child Relationships

When one component renders another inside its return statement, it becomes the **parent** of that component.

Example:

```jsx
function App() {
  return (
    <div>
      <Header />
      <Main />
      <Footer />
    </div>
  );
}
```

In this example:

- `App` is the **parent**.
- `Header, Main`, and `Footer` are its **children**.

This structure creates a component tree, with `App` at the root. You’ll build more complex relationships as you pass data (props) between components later in the course.

## Practice Challenge: Create and Compose Components

Follow these steps to put the concepts into practice:

1. Create three new files: `Header.jsx, Main.jsx`, and `Footer.jsx` inside a `components/` folder.
2. In each file, define and export a functional component:

   - `Header`: Displays the app’s title or logo.
   - `Main`: Displays some placeholder main content.
   - `Footer`: Displays copyright or footer info.

3. In `App.jsx`, import each component.
4. Compose them in the return statement:

   ```jsx
   import Header from "./components/Header";
   import Main from "./components/Main";
   import Footer from "./components/Footer";

   function App() {
     return (
       <div>
         <Header />
         <Main />
         <Footer />
       </div>
     );
   }

   export default App;
   ```

5. Run your app and confirm the components are displaying correctly.

## Summary

You’ve now learned how to write and compose React functional components. This structure — building small, focused components and assembling them into a complete UI — is the foundation of React development. As your apps grow in complexity, this modular approach will make them easier to understand and maintain.
