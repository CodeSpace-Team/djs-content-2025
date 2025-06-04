### Lesson: Introduction to Project Setup and Vite

In this lesson, you'll learn the basics of kicking off a React project, why Vite is the go-to choice for modern web development over Create React App, and how to get your first Vite project up and running.

#### Why Project Structure Matters
Before diving into code, let's talk about the backbone of any web application - its structure. A well-thought-out project structure isn't just about keeping files organized; it's about making your application easier to maintain, scale, and collaborate on. When files and components are where you expect them to be, development becomes smoother, debugging less of a headache, and adding new features a breeze.

### Let's Dive into Project Setup

### Project Setup Walkthrough
In this section, the instructor introduces the process of setting up a basic to-do app using React, emphasizing the importance of applying computer science principles to architecture decisions within React projects. The focus shifts to using Vite, a modern build tool for web projects, for creating a React application due to its efficiency over traditional tools like CodePen for larger projects with multiple files. The instructor walks through installing Vite with npm (Node Package Manager), choosing React as the framework, and deciding between JavaScript and TypeScript for the project. A brief discussion on package managers highlights npm and yarn, touching on their history, features, and the instructor's preference for npm due to its parity with yarn in features and ease of use without additional dependencies. The setup process concludes with creating a new React project using Vite.

EMBED: https://www.youtube.com/watch?v=e9d6ATX-bLA

#### Enter Vite: A Modern Build Tool
Vite (pronounced "veet") is a build tool that promises and delivers speed, hence its name, which means "fast" in French. Unlike its predecessor, Create React App, Vite leverages modern web standards, specifically ES modules, making it lightning-fast. 

## Hold up, What is Vite?

Check out Fireship.io's Vite Overview: https://www.youtube.com/watch?v=KCrXgy8qtjM

If you are looking to go a little deeper check out this crash course by Traversy Media: https://www.youtube.com/watch?v=89NJdbYTgJ8

Its benefits include:

- **Instant Server Start:** Say goodbye to waiting. Vite starts your development server in a fraction of the time.
- **Hot Module Replacement (HMR):** See your changes in real-time without losing state.
- **Optimized Build:** Vite's production builds are optimized for speed, ensuring your app loads quickly for users.

Vite also uses SWC, a Rust-based compiler, for incredibly fast TypeScript and JavaScript transformation, marrying the robustness of Rust with the flexibility of JavaScript.

### Setting Up a Vite Project

Vite has revolutionized the setup process for modern web projects, making it faster and more efficient. Here's how to get started with a new Vite project:

1. **Create a New Vite Project:**
   
   - Open your terminal.
   - Run `npm create vite@latest`. This command pulls the latest version of Vite and initializes a project setup wizard.
   - Follow the prompts. You'll be asked to name your project and choose a template. For a React project, select "react" or "react-ts" if you prefer TypeScript.
   - Navigate into your project directory with `cd your-project-name`.

2. **Understanding the Vite Project Structure:**

   After creating your project, take a moment to explore the structure Vite generates. Here's a quick overview:

   - `index.html`: The entry point of your application. Vite injects the built assets here.
   - `src/main.js` (or `main.ts` for TypeScript): The entry point for your JavaScript. This is where you'll import and render your React app.
   - `src/`: This directory will contain all your project's JavaScript and component files.
   - `vite.config.js`: Vite's configuration file. Here, you can customize the build process, define plugins, and more.

3. **Run Your Project:**

   - Back in your terminal, run `npm run dev` to start the development server.
   - Vite will compile your project and serve it, usually at `http://localhost:3000`. You can now view your project in a web browser.

Vite's simplicity doesn't end with setup. As you dive deeper into development, you'll appreciate its fast HMR (Hot Module Replacement), comprehensive documentation, and community support. By choosing Vite, you're not just optimizing your project's initial setup but also ensuring a streamlined development experience throughout your project's lifecycle.

### Starting with Vite

Embark on your React journey with Vite, a powerful build tool designed for the modern web developer. With Vite, you can expect a seamless development experience that catapults your productivity to new heights. Let's dive into the core features that make Vite an indispensable part of your development toolkit:

#### 1. Opening a Terminal in VS Code
Forget about juggling multiple applications. VS Code allows you to open a terminal directly within your coding environment, streamlining your workflow. This feature is especially handy when you're starting a local Vite server. You'll learn how to quickly launch your development server without ever leaving your editor, making your setup process as efficient as possible.

#### 2. Understanding HMR
One of Vite's standout features is Hot Module Replacement (HMR). But what does this mean for you? Imagine making a tweak to your code and seeing the changes instantly on your screen, without a full page reload. HMR makes this a reality. It refreshes only the modules that have changed, not the entire page, saving you valuable time and keeping your development flow uninterrupted. Explore how HMR can transform the way you build and test your applications, offering an unparalleled development experience.

### Choosing a Package Manager

A package manager is a tool that automates the process of installing, updating, configuring, and managing software packages or libraries within a system or project. In the context of software development, particularly web development, package managers play a crucial role in handling the libraries and dependencies your project needs to run and function correctly.

Package managers keep track of all the software packages and their respective versions that a project depends on. They ensure that the right package versions are installed, resolve version conflicts between packages, and maintain a record of all dependencies in a manifest file (like `package.json` for JavaScript projects). This automation saves developers a significant amount of time and effort, making it easier to manage complex projects with potentially hundreds or thousands of dependencies.

These tools not only manage dependencies but also offer features like package publishing, version management, and workspace management for monorepo setups, making them indispensable in modern web development workflows.

When starting a new project, one of the first decisions you'll make is selecting a package manager. This choice might seem minor, but it can significantly impact your development workflow. Let's dive into the three main contenders: NPM, Yarn, and PNPM.

Watch this video where CoderCoder takes you through NPM and why we need it: https://www.youtube.com/watch?v=P3aKRdUyr0s

#### NPM vs. Yarn vs. PNPM

**NPM** (Node Package Manager) is the original package manager for JavaScript and the default for Node.js. It's widely used and supported, with a vast registry of packages. However, its speed and dependency resolution have been points of contention among developers.

Enter **Yarn**. Created by Facebook, Google, Exponent, and Tilde, Yarn addressed these issues, offering faster installation times and more reliable dependency management through the `yarn.lock` file. This lock file ensures that every install results in the exact same file structure in `node_modules` across all machines. Yarn's introduction sparked improvements in NPM, leading to a healthy competition that benefited the developer community.

**PNPM** stands out by taking a unique approach to node_modules, using a content-addressable filesystem to share packages between projects. This method drastically reduces disk space usage and speeds up installation processes. For large projects or monorepos, PNPM's efficiency can be a game-changer.

#### Why PNPM Might Be Your Speedy Alternative

PNPM addresses the issues of both NPM and Yarn by focusing on performance and efficiency. If you're working with multiple projects or need to save disk space, PNPM could be the ideal choice. Its innovative approach ensures that you download and store a package only once on your machine, no matter how many projects use it. This efficiency makes it particularly attractive for developers looking to optimize their workflow.

## Project Structure: How to Organise your Projects

If you are wondering about how to structure your files and folders in React, check out this guide from Web Dev Simplified: https://www.youtube.com/watch?v=UUga4-z7b6s

### App Structure and React Basics

After running the `npm create vite@latest` command and setting up a basic React project named "to-do example," they opt for JavaScript over TypeScript, suggesting that for the simplicity and scale of the projects being tackled, TypeScript might not offer significant advantages initially. The discussion shifts to package managers, where npm is recommended due to its feature parity with Yarn and simpler integration as it comes bundled with Node.js. 

Following the setup, the instructor emphasizes an "annoyance-driven development" approach to structuring React projects, inspired by Dan Abramov, a React core team member. This method advocates for starting small, with a single file, and gradually refactoring and structuring as the project complexity grows. 

The practical part of the lesson begins with the creation of a basic React application structure in Vite, highlighting the removal of boilerplate code and setting up an `App` component and a `Button` component. The use of named exports for components and the importance of the `useEffect` hook for managing side effects in functional components are also touched upon. The segment on mapping over an array to dynamically create list items in JSX and the necessity of the `key` prop for optimizing React's re-rendering process is introduced with a practical coding example. The instructor briefly mentions the benefits of exploring other frameworks like Svelte for broader understanding, particularly highlighting how Svelte's documentation offers insights into concepts like keying items in a list for efficient updates.

### Organizing Your Project

A tidy project structure is not just about aesthetics; it's about efficiency. A well-organized project simplifies maintenance, scalability, and collaboration. Let's explore how to achieve this organizational bliss in your React projects:

#### 1. Components Folder
In React, components are the building blocks of your application. But as your project grows, so does the complexity of managing these components. Discover best practices for organizing your components into a dedicated folder. This strategy not only keeps your project tidy but also makes it easier to navigate and manage your codebase. Learn how to structure your "components" folder in a way that suits your project's needs and enhances your development workflow.

#### 2. Structuring React Projects
While React gives you the freedom to structure your projects as you see fit, this freedom can sometimes be overwhelming. Where do you start? How do you decide what goes where? This is where the concept of prototyping initial behavior comes into play. By starting with a prototype, you can iteratively refine your project's structure, identifying the most logical and efficient organization of your files and folders. Gain insights into how prototyping can guide you in structuring your React projects effectively, ensuring that your codebase remains manageable and scalable as it evolves.

### Creating Your First Components

#### 1. Building Your App
Starting your React project doesn't have to be daunting. We'll walk you through developing your first components in a hands-on, step-by-step manner. The key here is to focus on building functionality and worry less about getting everything perfect on the first try. Avoiding premature optimization allows you to experiment freely and understand the mechanics of React components deeply. You'll learn to appreciate the simplicity and power of React as you bring your application to life, one component at a time.

#### 2. Using `useState` Hook
State management is a critical aspect of any dynamic application. React's `useState` hook simplifies this process, enabling you to add state to your components with ease. This introduction to `useState` will show you how to manage state within your components effectively, allowing for interactive and dynamic user interfaces. Grasp the concept of state in React and see firsthand how `useState` empowers you to build responsive and stateful components.

#### 3. Understanding JSX
JSX, or JavaScript XML, is a syntax extension for JavaScript that allows you to write HTML structures in the same file as your JavaScript code. This blend of markup and logic streamlines the development process, making it more intuitive and efficient. Discover the benefits of JSX as you learn to create UI components that are both visually rich and functionally robust. JSX will become an invaluable tool in your React toolkit, bridging the gap between design and functionality.

### Understanding "key" Prop in React

When rendering lists of elements in React, using the `key` prop correctly is essential for optimizing your application's performance and ensuring its reliability.

#### 1. Importance of the `key` Prop
React uses the `key` prop to track which items have changed, been added, or been removed. This information helps React optimize re-renders and update the UI efficiently. Through practical examples, you'll learn why assigning a unique `key` to each list item greatly improves your application's performance and user experience.

#### 2. Avoiding `index` as a Key
While using array indices as keys might seem convenient, it can lead to unpredictable behavior and performance issues. We'll delve into why choosing more stable identifiers as keys is crucial and how it affects the re-rendering process. Understanding the correct usage of keys in React will ensure your application is both efficient and bug-free.

### Adding More Functionality

As your journey with React continues, you'll start to see your application take shape, evolving from simple displays of data to interactive experiences. This section guides you through adding more complexity and interactivity to your React application, focusing on user inputs and styling.

#### Creating a Task Form
Learn how to create a form for adding tasks, allowing users to contribute data to your application. This step is crucial in making your app interactive and responsive to user inputs. We'll cover how to handle form submissions in React, ensuring that user data is captured accurately and efficiently. Through this process, you'll understand the significance of state management in collecting and handling user inputs, bringing us to the next crucial aspect of React development: styling.

#### The Importance of the "className" Property <!-- React is plain Javascript, so applying a class to the element is similar to how you would do it in vanilla JS -->
Styling in React is unique due to its JSX syntax. The "className" property plays a pivotal role in applying CSS styles to your components, ensuring that your application is not only functional but also visually appealing. Discover how to effectively use "className" to bring your app to life with CSS, enhancing the user experience with engaging and responsive designs.

### Advanced React Hooks

Diving deeper into React's capabilities, you'll encounter advanced hooks that offer more sophisticated state management and logic reuse across your components.

#### Introduction to Custom Hooks with "useTasks"
Custom hooks are a powerful feature in React that allow you to extract component logic into reusable functions. "useTasks" will be our example of a custom hook designed to manage task-related logic, including adding, deleting, and updating tasks. By abstracting this functionality into a custom hook, you can keep your components clean and focused while sharing logic across your app.

#### Managing Tasks
Building on the "useTasks" custom hook, we will explore how to implement functionalities crucial to any task management application: adding new tasks, deleting existing ones, and updating them. This section will emphasize state management within custom hooks and demonstrate how to manipulate lists of data dynamically in response to user actions.

#### Debugging Techniques for React Apps
As your application grows in complexity, so does the likelihood of bugs. Effective debugging is essential to maintaining a healthy codebase. Learn debugging techniques tailored for React applications, including using the React Developer Tools and leveraging the powerful error boundaries in React. These strategies will help you identify and resolve issues swiftly, keeping your development process smooth and efficient.

By integrating these advanced features and techniques into your React development skill set, you'll be well on your way to creating more complex and interactive web applications. Remember, the key to mastering React lies in practice, experimentation, and continually challenging yourself with new problems to solve. With these tools at your disposal, you're equipped to tackle more advanced projects and continue your growth as a React developer.

### Persisting Data with Local Storage

As your React app becomes more interactive, you'll want to ensure that user data persists between sessions. This section introduces you to leveraging local storage, a web API for storing data locally within the user's browser, enhancing your app's usability by retaining user input and state.

#### Using Local Storage to Save and Retrieve Tasks
Discover how to utilize local storage to save tasks created by users, ensuring that their input remains available across browser sessions. You'll learn the key methods for interacting with local storage, including `setItem` to save data and `getItem` to retrieve it. This knowledge allows you to maintain the state of tasks even when the browser is closed or refreshed, significantly improving the user experience.

#### Abstracting Local Storage Access with Custom Functions
To streamline your code and make local storage interactions more maintainable, we'll guide you through abstracting access to local storage into custom functions. This abstraction not only cleans up your code, making it more readable and reusable but also encapsulates local storage logic, making future changes or enhancements easier to implement.

### Review and Best Practices

After adding functionality and ensuring data persistence, it's crucial to step back and review your code. This final section focuses on consolidating your knowledge, addressing best practices, and introducing tools to help maintain and document your React app effectively.

#### Reviewing the Code and Discussing Best Practices
We'll conduct a comprehensive review of the code you've written, highlighting best practices in React development. This discussion covers everything from component structuring and state management to effective use of hooks and local storage. By understanding these best practices, you can ensure your React applications are not only functional but also optimized for performance, maintainability, and scalability.

#### Using JSDoc for Better Code Documentation and Maintainability
Good documentation is the cornerstone of maintainable code. In this part, you'll learn how to use JSDoc, a popular documentation syntax for JavaScript, to annotate your React components and functions. Documenting your code with JSDoc enhances readability, makes it easier for others to understand and contribute to your project, and aids in debugging and future development efforts. By adopting JSDoc, you commit to a higher standard of code quality and maintainability.

By understanding and implementing the concepts covered in these sections, you'll be well-equipped to build more sophisticated React applications that persist data, adhere to best practices, and are well-documented for future growth. Remember, the journey of learning React is ongoing. Continue to explore, experiment, and refine your approach as you tackle new challenges and build increasingly complex applications. Happy coding!
