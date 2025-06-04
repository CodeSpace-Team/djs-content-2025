### Building Your First React App

React is a powerful JavaScript library for building user interfaces, primarily via the creation of reusable components. It uses a declarative programming model to create efficient and flexible applications. This lesson will guide you through setting up your first React application, introducing you to the key concepts of React including JSX, components, state, and props.

In this lesson, we are learning how to create a React component using JSX and differentiating it from plain HTML. We are also discussing the evolution of React from using class components to the modern function-based approach. React allows us to define custom elements, manage component state using hooks, and render components efficiently. Finally, we are exploring how React's virtual DOM works to optimize updates and manage rendering processes. This understanding is crucial for building dynamic and responsive web applications.

Jump into the video below:

EMBED: https://www.youtube.com/watch?v=Q-9uOQmjlNQ


#### Setting Up the Environment

To begin developing with React, you will need Node.js installed on your computer. Node.js comes with npm (Node Package Manager), which you will use to create and manage your React project.

1. **Install Node.js**: Download and install Node.js from [nodejs.org](https://nodejs.org/).

2. **Create a React App**:
   Use the `create-react-app` command to set up a new React project. This tool sets up your development environment so you can use the latest JavaScript features, provides a nice developer experience, and optimizes your app for production. Open your terminal and run:
   ```bash
   npx create-react-app my-first-react-app
   cd my-first-react-app
   npm start
   ```
   This will start the development server and open your new React application in the browser.

#### Understanding JSX

JSX (JavaScript XML) is a syntax extension for JavaScript that looks similar to XML or HTML. React uses JSX for templating instead of regular JavaScript. It is easier to write and understand, and you can use it almost like HTML.

Example of JSX:
```jsx
const element = <h1>Hello, world!</h1>;
```

#### Components

Components are the building blocks of any React application. You can think of them as custom, reusable HTML elements that encapsulate parts of the interface. React components come in two types: Functional and Class components.

- **Functional Components**: These are JavaScript functions that return JSX. They are simpler and preferred for most applications.
  
  Example of a Functional Component:
  ```jsx
  function Welcome(props) {
    return <h1>Hello, {props.name}</h1>;
  }
  ```

- **Class Components**: These are ES6 classes that extend `React.Component` and contain a `render` method which returns JSX.

  Example of a Class Component:
  ```jsx
  class Welcome extends React.Component {
    render() {
      return <h1>Hello, {this.props.name}</h1>;
    }
  }
  ```

#### State and Lifecycle

State offers a way to store and manage data that reacts to user actions or system events. It's confined to the component and can influence the component's output and behavior.

You can initialize state in a class component's constructor and update it with `this.setState()`. However, with the introduction of Hooks, functional components can also manage state using the `useState` hook.

Example using `useState` in a Functional Component:
```jsx
import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

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

#### Props

Props (short for "properties") are a way of passing data from parent to child components. They are read-only and help you create reusable components.

Example of using props:
```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}

function App() {
  return (
    <div>
      <Welcome name="Alice" />
      <Welcome name="Bob" />
      <Welcome name="Charlie" />
    </div>
  );
}
```

#### Rendering Elements

React elements are immutable objects that describe what you see on the screen. Unlike browser DOM elements, React elements are plain objects and are cheap to create. React updates the DOM to match the React elements.

Example of rendering an element:
```jsx
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<App />);
```
This lesson has introduced you to the fundamental concepts of React, including JSX, components, state, and props. These concepts are foundational for building robust applications with React. Start experimenting with the example code provided, modifying components, and observing how React updates the UI efficiently. Your journey into React development begins here, and as you progress, you'll learn more about advanced topics such as context, reducers, and side effects management with hooks.

### Build a React Info Site | Lessons: 35 | 2 hours 55 min

Jump into the Scrimba practice here: https://scrimba.com/playlist/pKNqYAZ

1. Introduction to React | 7:46
2. What we'll learn | 3:38
3. First React | 8:02
4. First React Practice | 1:48
5. Local setup (the quick way) | 1:57
6. Libraries/Frameworks | 7:11
7. Why React? It's Composable! | 4:47
8. Why React? It's declarative | 4:42
9. JSX | 9:39
10. Drag and Drop Deploy with Netlify | 2:34
11. Get detailed reviews of your React projects – Scrimba Bootcamp | 1:53
12. Goodbye, CDNs! | 4:05
13. UPDATE: New React 18 createRoot API | 4:18
14. Thought experiment: use .append() instead of ReactDOM.render()? | 5:28
15. Project part 1 - markup (Update) | 5:33
16. Pop quiz! | 5:08
17. Custom Components | 6:55
18. Custom Components part 2 | 3:57
19. Custom Components Quiz | 2:47
20. Parent/Child Components | 4:54
21. Styling with Classes | 6:43
22. Organize components | 7:41
23. Run React locally with Vite | 9:30
24. Quick mental outline of project | 3:54
25. Project setup | 7:13
26. Quick Figma Walkthrough | 1:40
27. Navbar & Styling | 7:16
28. Main Section | 7:44
29. Color the bullets | 2:23
30. Add background logo | 4:17
31. Why are Solo Projects important? | 5:08
32. Solo Project (PRO) - Digital Business Card | 3:52
33. Deploy Your React App with Netlify | 5:23
34. Get a code review! | 2:39
35. React Section 1 Recap | 2:37