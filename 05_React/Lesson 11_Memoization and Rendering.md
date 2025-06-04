### Lesson: Rendering and Memoization

### Understanding React Re-Renders

React's efficiency in updating the user interface to reflect application state changes lies in its rendering cycle. However, understanding how and when React decides to re-render components is crucial for optimizing application performance and creating a smooth user experience.

Check out this video where CodeSketched takes you through Rendering in React: https://www.youtube.com/watch?v=mECV6nGOqNo&list=PLTkAV9HwDLLDrT32MxxSeBDLWD4okCiVI&index=3

Next up go a little deeper and check out CodeSketched explain how rendering works: https://www.youtube.com/watch?v=AwW7olQ84Qs

## Articles
- Intro to re-renders by Developer Way: https://www.youtube.com/watch?v=qTDnwmMF5q8
- Mastering memoization in React by Developer Way: https://www.youtube.com/watch?v=huBxeruVnAM
- Josh Comeau explains why React Re-renders here: https://www.joshwcomeau.com/react/why-react-re-renders/
- Check out this guide to React re-renders: https://www.developerway.com/posts/react-re-renders-guide

#### The React Rendering Cycle

The rendering cycle in React is a series of steps the library takes to update the DOM in response to state or prop changes within components. Here's a simplified overview of how it works:

1. **Initial Render**: When a React application loads for the first time, React runs the render method of each component to determine what the DOM should look like based on the component's props and state. This process constructs the initial UI of the application.

2. **State or Prop Changes**: Whenever there's a change in a component's state or props (e.g., due to user interaction or data fetching), React triggers a re-render. This isn't an immediate process of changing the DOM but rather a calculation to determine what needs to change.

3. **Reconciliation**: React compares the newly returned elements from the render method with the previous ones. This process, known as reconciliation, identifies differences and determines the most efficient way to update the DOM to match the new state of the application.

4. **DOM Updates**: Once React knows what changes are needed, it updates the DOM accordingly. This step is optimized to be as efficient as possible, minimizing updates to the actual DOM, which are costly performance-wise.

By only updating what's necessary, React keeps the application fast, even as it grows in complexity. However, unnecessary re-renders can still occur, which is why understanding the causes and solutions is important.

#### Re-rendering vs. Re-painting

Understanding the difference between re-rendering and re-painting is crucial for diagnosing and improving the performance of a React application:

- **Re-rendering** in React context means recalculating the component's output — running the render method again — when its state or props change. This process is about determining the new structure of the UI but doesn't directly involve any changes to the actual UI visible to the user.

- **Re-painting**, however, is a browser process that occurs when the visible UI needs to be updated. After React decides what the updated UI looks like (re-rendering), the browser applies those changes to the screen, a process that might involve re-painting pixel values on the display.

Optimizing for fewer re-renders directly contributes to less re-painting, leading to better performance, as re-painting can be an expensive operation in terms of browser resources.

#### Role of State Changes in Triggering Re-renders

In React, re-renders are primarily triggered by changes to a component's state or props:

- **State Changes**: The React state is designed to be the single source of truth for component data that can change over time. Using  setter function from `useState` in functional components, or context updates informs React that the component needs to re-render to reflect the new state.

- **Props Changes**: Similarly, when a component receives different props from its parent, it will also trigger a re-render. This ensures that the component reflects the latest data it's supposed to display.

Understanding that not all state or props changes require a UI update is key to optimizing React applications. For instance, if a state change does not affect the output of the render method, it's an unnecessary re-render.

React provides tools like `React.memo`, `useMemo`, and `useCallback` to help developers control and minimize unnecessary re-renders, ensuring that components only update when absolutely necessary. By carefully managing state and props, and understanding how they trigger re-renders, developers can significantly improve their application's performance.

In this section, we explored the core concepts underlying React's rendering mechanism, including the distinction between re-rendering and re-painting and the pivotal role of state changes in initiating the rendering process. This knowledge forms the foundation for optimizing React applications, which we'll build upon by introducing specific memoization techniques in the following section.

#### Memoization

Memoization is a programming technique designed to increase the efficiency of applications by storing the results of expensive function calls and returning the cached result when the same inputs occur again. This concept is particularly useful in React, a library where component re-renders are a common occurrence. React's rendering mechanism, while efficient, can lead to performance bottlenecks if components are unnecessarily re-rendered without any actual changes to their state or props. To mitigate this, React offers several memoization tools: `React.memo`, `useCallback`, and `useMemo`. Each tool serves a specific purpose in optimizing component performance by reducing unnecessary re-renders.

Check out this video about Memoization and How to Memoize by Dave Gray: https://www.youtube.com/watch?v=TWUV_LRVX24

### **`React.memo`**

- **Definition**: `React.memo` is a higher-order component (HOC) designed to wrap around functional components. This tool memorizes the rendered output of a component and only triggers a re-render when it detects changes in the component's props that would result in a different output. It's a form of optimization that prevents functional components from re-rendering when their props remain the same between renders.
  
- **Purpose**: The main goal of `React.memo` is to boost application performance by cutting down on unnecessary re-renders. By doing so, it helps keep the application responsive and ensures smoother user interactions, especially in parts of the UI that remain static or change infrequently.

- **Example Usage**: Consider a component that renders a user's profile information, which typically remains constant. Wrapping this component in `React.memo` prevents it from re-rendering every time the parent component updates, provided the profile data passed as props hasn't changed. This is particularly beneficial in scenarios like rendering lists where the individual list items don't change often but the list itself might re-render due to other state changes in the application.

### **`useCallback`**

- **Definition**: `useCallback` is a hook that memoizes callback functions. This means that the function defined within `useCallback` will persist between renders unless a value in its dependency array changes. This hook is useful for passing callbacks to deeply nested child components that rely on reference equality to prevent unnecessary renders.

- **Purpose**: The primary use of `useCallback` is to ensure that functions, especially those passed as props to child components, don't get recreated on every render. This is crucial for performance when dealing with components that only need to re-render in response to actual changes in the functions they rely on.

- **Example Usage**: If a parent component passes a click handler function to a child component and that child component is wrapped with `React.memo`, using `useCallback` for the click handler ensures that the child component does not re-render unless the click handler function's dependencies change. This prevents unnecessary re-renders and maintains performance across the application.

### **`useMemo`**

- **Definition**: Similar to `useCallback`, `useMemo` is a hook that memoizes values. However, instead of memoizing functions, `useMemo` is used to memoize the result of a function. This hook re-computes the memoized value only when one of its dependencies changes, thus avoiding costly calculations on each render.

- **Purpose**: `useMemo` aims to improve performance by storing computationally expensive values and only recalculating them when necessary. This is especially useful for data transformations, computations, and other operations that are expensive to perform and result in the same output for the same inputs.

- **Example Usage**: In a component that displays a filtered list of items based on user input, using `useMemo` to memoize the filtered list ensures that the filtering operation is only performed when the list of items or the filter criteria changes. This prevents the filtering logic from executing on every render, which can significantly enhance performance, especially with large datasets.

By leveraging these memoization tools, developers can significantly improve the responsiveness and efficiency of React applications, ensuring a smoother experience for end-users by minimizing unnecessary work.