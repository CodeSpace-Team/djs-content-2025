https://www.youtube.com/watch?v=xuSWzsjQP4o
https://scrimba.com/playlist/pKNqYAZ



#### Lesson Objectives:
- Understand the foundational concepts of React, focusing on components, JSX, and state management.
- Learn how to set up a React development environment in a browser-based tool like CodePen, including configuring Babel.
- Explore creating components as functions and the significance of PascalCase naming convention for components.
- Discover the role of ReactDOM for targeting the browser and rendering components.
- Gain insights into handling events and updating component state using React Hooks.
- Delve into performance considerations and optimizing React applications with React.memo and useState.


------------------

### Introduction to React Components

#### Understanding Components as Functions
In React, components are the heart of the application's UI. They are essentially JavaScript functions or classes that return HTML elements. The beauty of components lies in their ability to encapsulate and manage their own state and logic, making the UI highly modular and reusable across the application.

Components defined as functions are known as functional components. They are simpler and intended for components that mainly focus on the UI aspect. Here's a basic example of a functional component:

```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

This `Welcome` component accepts `props` (short for properties) as its argument and returns a React element that describes what should appear on the screen. The curly braces `{}` within the JSX allow JavaScript expressions to be embedded, making the code dynamic and reusable.

#### Naming Conventions for Components (PascalCase)
When naming React components, the convention is to use PascalCase. This means the first letter of every word in the component's name is capitalized. This convention helps differentiate React components from regular HTML elements, which are usually written in lowercase.

For example:
- Correct: `UserProfile`, `ShoppingCart`
- Incorrect: `userprofile`, `shopping_cart`

Using PascalCase for component names indicates that they are custom components, distinguishing them from standard HTML tags. It also aligns with the convention that classes in JavaScript are named using PascalCase, reinforcing the idea that components are seen as custom, reusable building blocks of the UI.

### Understanding ReactDOM and Its Purpose

#### Difference Between React and ReactDOM Libraries
React and ReactDOM are two separate libraries that work closely together. React provides the core functionality for defining components, managing state, and handling props. It is concerned with the logic and structure of UI components.

ReactDOM, on the other hand, deals specifically with rendering components to the DOM. It provides the glue between React's abstract components and the browser's DOM, allowing React elements to be displayed on the web page.

#### How to Use ReactDOM for Rendering Components to the Browser
To use ReactDOM for rendering components, you'll typically use the `ReactDOM.render()` method. This method takes two arguments: the React element or component you want to render and the DOM node where you want to mount or render the component.

For example, to render the `App` component from the previous section to the browser, you would use:

```jsx
ReactDOM.render(<App />, document.getElementById('root'));
```

This tells ReactDOM to render the `App` component inside the DOM element with the ID of `root`. This element acts as the entry point for your React application and is usually found in your HTML file:

```html
<div id="root"></div>
```

Understanding the roles of React and ReactDOM is crucial for effectively building and rendering UI components in a React application.


### Managing State with Hooks

#### Introduction to Hooks for State Management and Automatic Re-rendering
React Hooks, introduced in React 16.8, fundamentally changed how developers can manage state and side effects in functional components. Before Hooks, state management and lifecycle methods were capabilities reserved only for class-based components. Hooks brought the ability to use state and other React features without writing a class, making code more readable and maintainable.

A Hook is a special function that lets you "hook into" React features. For example, the `useState` Hook allows you to add React state to functional components. When state changes, the component automatically re-renders, updating the UI based on the new state.

Here's a simple example of using the `useState` Hook:

```jsx
import React, { useState } from 'react';

function Counter() {
  // Declare a new state variable, which we'll call "count"
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

In this example, `useState` is called within a functional component to add some local state. `useState` returns a pair: the current state value and a function that lets you update it. You can call this function from an event handler or somewhere else. It’s similar to `this.setState` in a class, except it does not merge the old and new state together.

The only argument to `useState` is the initial state. In the example above, it is `0` because our counter starts from zero. React will preserve this state between re-renders. `useState` returns a pair: the current state value and a function that lets you update it. This is why we write `const [count, setCount] = useState()`.

#### Transition from Class-based Components to Functional Components with Hooks
Prior to Hooks, class-based components were the only way to manage state and lifecycle methods in React applications. This often led to more complex and less intuitive code, especially for developers new to React or those who preferred the simplicity of functional programming patterns.

Hooks allow for a more functional approach to component architecture, enabling state management, side effects, context, and more in functional components. This has several benefits:
- **Simplification of code:** By using Hooks, you can extract stateful logic from a component so it can be tested independently and reused. Hooks allow you to reuse stateful logic without changing your component hierarchy.
- **Reduction of boilerplate:** Class components require binding event handlers in the constructor or using class field syntax. Hooks eliminate this need, making your code cleaner and less prone to errors.
- **Enhanced code splitting:** Hooks encourage smaller, function-based components that are easier to maintain, test, and debug. This can lead to improved performance as smaller components are easier for React to render and update.

Here's how you might convert a class component with state to a functional component using Hooks:

**Class Component:**
```jsx
class Counter extends React.Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
  }

  render() {
    return (
      <div>
        <p>You clicked {this.state.count} times</p>
        <button onClick={() => this.setState({ count: this.state.count + 1 })}>
          Click me
        </button>
      </div>
    );
  }
}
```

**Functional Component with Hooks:**
```jsx
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

The functional component with Hooks is more concise and easier to read, making the codebase more maintainable and scalable. This transition towards functional components with Hooks is a testament to React's commitment to improving the developer experience without sacrificing the power or flexibility of the library.



### 5. Creating an Interactive Application: Tally App

#### Building a Simple Tally Application to Understand State Management and Event Handling
To solidify our understanding of state management and event handling in React, let's build a simple tally application. This application will have a counter that increments or decrements based on user interaction.

```jsx
import React, { useState } from 'react';

function TallyApp() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <h1>Tally Counter</h1>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
      <button onClick={() => setCount(count - 1)}>Decrement</button>
    </div>
  );
}
```

In this example, the `useState` Hook is used to keep track of the count state. We render the current count and provide two buttons: one to increment the count and another to decrement it. The `onClick` handlers on these buttons call `setCount` with the new count value based on whether we're incrementing or decrementing.

#### Interpolating Variables in JSX and Attaching Event Listeners
Interpolation in JSX allows us to embed expressions like variables within our JSX markup. In the example above, `{count}` within the `<p>` tag is an example of interpolation, dynamically rendering the value of the `count` variable.

Event listeners in React, such as `onClick`, allow us to attach interactions to elements. The syntax for attaching event listeners in JSX is similar to HTML but uses camelCase. For example, `onClick` in JSX corresponds to `onclick` in plain HTML. Event handlers in React are passed as functions, as seen in the `onClick` event handlers above.

### 6. Optimizing React Applications

#### Performance Considerations in React Applications
As React applications grow in size and complexity, performance considerations become increasingly important. React's efficient update mechanism through the virtual DOM ensures high performance for most use cases. However, unnecessary re-renders can lead to performance bottlenecks in larger applications.

To diagnose and avoid unnecessary re-renders, developers can use React's built-in Profiler in the React DevTools. It's also crucial to optimize component updates by carefully managing state and props to ensure that components only re-render when truly necessary.

#### Use of React.memo for Optimizing Re-renders Based on Props
`React.memo` is a higher-order component that memoizes a component, meaning React will skip rendering the component if its props have not changed. This can lead to significant performance improvements in applications with many components or complex UIs.

```jsx
const MemoizedComponent = React.memo(function MyComponent(props) {
  /* render using props */
});
```

By wrapping a component in `React.memo`, React will perform a shallow comparison of the current and new props. If they are the same, React skips rendering the component and reuses the last rendered result, reducing the work needed to update the DOM.

It's important to note that `React.memo` only performs a shallow comparison. For deeper comparison, you may need to provide a custom comparison function as the second argument to `React.memo`.

In conclusion, understanding and implementing performance optimization techniques such as `React.memo` is crucial for building efficient, fast-reacting applications. While React provides a solid foundation for performance, mindful use of these techniques ensures that your applications remain responsive and enjoyable for users.


#### Introduction to Creating Custom React Hooks for Reusable Logic
One of the powerful features of Hooks in React is the ability to create your own custom Hooks. This enables you to extract component logic into reusable functions. Custom Hooks allow you to share logic across multiple components, making your codebase DRY (Don't Repeat Yourself) and easier to maintain.

**Creating a Custom Hook:**

Suppose you have a common functionality in your application where components need to subscribe and unsubscribe to a particular browser event, such as resizing the window. You can create a custom Hook that abstracts this logic:

```jsx
import { useState, useEffect } from 'react';

function useWindowSize() {
  const [size, setSize] = useState([window.innerWidth, window.innerHeight]);

  useEffect(() => {
    const handleResize = () => {
      setSize([window.innerWidth, window.innerHeight]);
    };

    window.addEventListener('resize', handleResize);
    return () => window.removeEventListener('resize', handleResize);
  }, []);

  return size;
}
```

This custom Hook, `useWindowSize`, uses `useState` to track the window's width and height and `useEffect` to manage side effects (subscribing and unsubscribing to the `resize` event). The Hook returns the current size, making it easy to use in any component:

```jsx
function App() {
  const [width, height] = useWindowSize();

  return (
    <div>
      <p>Window width: {width}</p>
      <p>Window height: {height}</p>
    </div>
  );
}
```

**Advantages of Custom Hooks:**

- **Reusability:** Custom Hooks can be used in any component, allowing you to reuse stateful logic without tightly coupling it to a specific component.
- **Separation of Concerns:** By abstracting logic into Hooks, components become simpler and only concerned with rendering UI, making them more readable and maintainable.
- **Composability:** Custom Hooks can be composed together in components or even within other Hooks, enabling more complex logic to be built from simpler, reusable pieces.

In summary, the `useState` hook revolutionizes state management in functional components by providing a straightforward way to introduce state. Furthermore, the ability to create custom Hooks extends React's capabilities, allowing for the creation of reusable, composable, and maintainable code. This combination of simplicity and power makes React a highly effective tool for building dynamic web applications.




Here are the video timestamps for the key concepts outlined in the lesson on creating a React application:

1. **Introduction to React Components**
   - Components as functions: 00:01:00
   - Naming conventions for components (PascalCase): 00:00:00

2. **Setting Up React with Babel on CodePen**
   - Configuring Babel on CodePen: 00:01:30
   - Creating and rendering components: 00:02:10

3. **Understanding ReactDOM and Its Purpose**
   - Difference between React and ReactDOM: 00:03:00
   - Using ReactDOM for rendering: 00:04:00

4. **Managing State with Hooks**
   - Introduction to Hooks: 00:06:30
   - Transition from class components to functional components: 00:07:00

5. **Creating an Interactive Application: Tally App**
   - Building a simple tally application: 00:10:10
   - Interpolating variables and attaching event listeners: 00:10:50, 00:11:40

6. **Optimizing React Applications**
   - Performance considerations: 00:18:00, 00:19:30
   - Using React.memo: 00:20:30

7. **Advanced State Management**
   - Exploring useState hook: 00:23:00
   - Introduction to creating custom React Hooks: 00:25:00

These timestamps correspond to the sections in the video that cover each key concept, providing a structured approach to learning about creating a React application from scratch.




### Build a React info site
- Lessons: 35
- Duration: 2 hours 55 min

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