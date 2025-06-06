# Setting Up a React App with Vite

Modern web applications require build tools to compile JavaScript, handle modules, and optimize performance. React doesn't run in the browser as-is — it must be bundled and transpiled. In this lesson, we’ll introduce **Vite**, a modern front-end build tool that provides a faster and simpler experience for starting and developing React projects.

## Learning Objectives

By the end of this lesson, you will be able to:

- Understand what Vite is and why it's used to scaffold React apps.
- Use the command-line interface to create a new Vite-based React project.
- Identify the role of key files like `main.jsx` and `App.jsx` in a Vite setup.
- Navigate and understand the folder structure of a Vite project.

## Intro to Vite and Why It’s Fast for React

Vite (pronounced "veet", meaning "fast" in French) is a modern build tool created by Evan You, the creator of Vue. It is designed to offer:

- Lightning-fast startup via native ES modules
- Instant hot module replacement (HMR)
- Minimal configuration out of the box
- Support for JSX, TypeScript, CSS modules, and more

Unlike older tools like Webpack, which bundle the entire app on startup, Vite serves modules on-demand during development — making it ideal for React projects.

## Using `npm create vite@latest`

To scaffold a new Vite + React project:

1.  Open your terminal and navigate to a working directory.
2.  Run the following command:
    ```bash
    npm create vite@latest
    ```
3.  When prompted:

    - Choose a project name (e.g.,` my-react-app`)
    - Select the `React` template (or `React + TypeScript` if preferred)

4.  Install dependencies:

    ```bash
    cd my-react-app
    npm install
    ```

5.  Start the dev server:

        ```bash
        npm run dev
        ```

    This will launch your React app at `http://localhost:5173` (or another available port).

## Understanding the Project Folder Structure

Once the project is created, explore the following key files:

- `index.html`

  The HTML entry point. It contains a `<div id="root">` where React injects the app.

- `main.jsx`

  This is the true entry point for the React app. It imports React and the root `App` component, and renders it to the DOM:

  ```jsx
  import React from "react";
  import ReactDOM from "react-dom/client";
  import App from "./App.jsx";

  ReactDOM.createRoot(document.getElementById("root")).render(
    <React.StrictMode>
      <App />
    </React.StrictMode>
  );
  ```

- `App.jsx`
  This is the top-level component where your main layout and routing logic often begins. Initially, it contains a simple template:

  ```jsx
  function App() {
    return (
      <div>
        <h1>Hello Vite + React!</h1>
      </div>
    );
  }

  export default App;
  ```

- `vite.config.js`

  The configuration file for Vite. Most basic React apps won’t need to touch this.

- `package.json`

  Lists dependencies and scripts like dev, build, and preview.

## Practice Challenge: Scaffold and Run a React App

1. Create your own Vite project as demonstrated.
2. Open it in a code editor (like VS Code).
3. Start the development server.
4. Open the browser and confirm that the app is running.
5. Modify the text in `App.jsx` and observe changes with Hot Module Reloading.

   **Explore main.jsx and App.jsx**

   Spend time tracing:

   - How the `main.jsx` file initializes and renders the app.
   - How the `App.jsx` component is composed and exported.
   - Where future components will be imported and rendered.

## Summary

In this lesson, students installed and ran a Vite-powered React project. They explored the initial file structure, understood the roles of `main.jsx` and `App.jsx`, and saw how Vite streamlines the setup process compared to traditional tooling. With the environment ready, students are now prepared to start building their own components and apps.
