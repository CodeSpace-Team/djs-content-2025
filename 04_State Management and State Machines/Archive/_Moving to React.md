# Lesson: From Vanilla to React

When transitioning from managing state in vanilla JavaScript to using React, there are several key concepts and practices that are relevant to understand. React introduces a more structured approach to state management, leveraging its component-based architecture. Here are some essential points to grasp:

### 1. Component State

In React, each component can maintain its own state, which is an object that determines how that component behaves and renders. State in React is more structured compared to the loose handling of state objects in vanilla JavaScript.

- **Local State**: This is the state that is local to a component and not shared with others unless passed down as props. It can be managed using the `useState` hook in functional components or `this.state` in class components.

### 2. Props and State Lifting

- **Props**: In React, data can be passed from parent to child components via props. This is a one-way data flow that helps maintain the unidirectional data flow pattern.
- **State Lifting**: When multiple components need to access the same state, it's common to lift the state up to their closest common ancestor. This practice is known as "lifting state up" and helps in managing shared state across different components.

### 3. State Immutability

React emphasizes the immutability of state. This means that state should not be directly modified. Instead, updates should create new objects based on the previous state.

- **Functional Updates**: Using functions like `setState` in class components or the setter function from `useState` in functional components ensures that the state is updated immutably and React can manage rerenders optimally.

### 4. UseEffect Hook

The `useEffect` hook in functional components allows you to perform side effects in your component. It's a powerful tool for working with component lifecycle events, such as fetching data on component mount, which can affect the component's state.

### 5. Global State Management

For larger applications, local and lifted state might not be enough. React supports several ways to manage global state:

- **Context API**: This provides a way to share values like state between components without having to explicitly pass a prop through every level of the tree.
- **Redux**: A popular library for managing application state in a centralized store, which components can access as needed. Redux introduces actions, reducers, and the store, adding a more formal state management framework.
- **Other Libraries**: Other libraries like MobX or Recoil also provide ways to manage state in React apps.

### 6. Reactivity and Rendering

React's reactivity system is built around the concept of the Virtual DOM. When state changes, React compares the new Virtual DOM with the previous one and only updates the real DOM where changes have occurred. This makes React efficient at updating the UI in response to state changes.

Understanding these concepts will make your transition from vanilla JavaScript to React smoother. In React, state management is more about understanding the flow of data between components and managing changes in a predictable way. React's tools and patterns for state management aim to ensure that your application's state is scalable, maintainable, and easy to debug.