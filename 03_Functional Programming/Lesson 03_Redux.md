
Redux is a popular state management library used in JavaScript applications, particularly with libraries like React. It provides a way to manage the state of your app in a predictable way. This lesson will guide you through the key concepts of Redux, including stores, actions, reducers, and how they work together to manage state in your applications.

### What is Redux?

[Redux](https://redux.js.org/) is a library that helps manage the state of your application. The state refers to the data or the current conditions of your app at any given time. Redux ensures that your state changes are predictable and easy to track.

### Key Concepts

1. **Store**: A store holds the whole state tree of your application. There can only be a single store in a Redux application.
2. **Actions**: Actions are payloads of information that send data from your application to your store. They are the only source of information for the store.
3. **Reducers**: Reducers specify how the application's state changes in response to actions sent to the store.

### How Does Redux Work?

At its core, Redux revolves around a strict unidirectional data flow, meaning that all data in the application follows the same lifecycle pattern, making the logic of your app more predictable and easier to understand. This process involves three main steps:

1. **Dispatching an Action**: An action is dispatched when you want to change the state. This action describes what happened, but doesn't describe how the application's state changes.

2. **Handling Actions with Reducers**: A reducer is a function that determines how the state should change in response to an action. Reducers are pure functions, meaning they should not have any side-effects or mutate the state directly; instead, they return a new state object based on the incoming action.

3. **Subscribing to the Store**: Components can subscribe to the store, so they can be updated when the state changes. When the state is updated, the store notifies all subscribed components, prompting them to re-render with the new state.

### Example

Let's consider a simple example of a counter application with actions to increment and decrement the count.

- **Action**: Actions for incrementing and decrementing the count might look like this:
  ```javascript
  { type: 'INCREMENT' }
  { type: 'DECREMENT' }
  ```

- **Reducer**: The reducer for this application might look like this:
  ```javascript
  function counter(state = 0, action) {
    switch (action.type) {
      case 'INCREMENT':
        return state + 1;
      case 'DECREMENT':
        return state - 1;
      default:
        return state;
    }
  }
  ```

- **Store**: You create a store that holds the application's state, and you use the reducer to manage state changes when actions are dispatched:
  ```javascript
  let store = Redux.createStore(counter);
  ```

- **Subscribing**: You can subscribe to the store to update your UI when the state changes:
  ```javascript
  store.subscribe(() => console.log(store.getState()));
  ```

- **Dispatching Actions**: You change the state by dispatching actions:
  ```javascript
  store.dispatch({ type: 'INCREMENT' });
  ```

### Benefits of Using Redux

- **Predictability of state**: You can predict how your application state changes by looking at your actions and reducers.
- **Maintainability**: Having a predictable state flow makes it easier to understand, maintain, and debug applications.
- **Server-side rendering**: Redux works with server-side rendering, allowing you to preload data and generate the initial state on the server.
- **Developer tools**: Redux offers developer tools that make it easier to track dispatched actions and state changes.

Redux offers a robust solution for managing state in JavaScript applications. By understanding and applying the concepts of actions, reducers, and the store, you can more effectively manage and track state changes across your app, leading to more predictable, maintainable, and debuggable code.

# Notes on the video lesson

In this lesson, we learn how to manage global state in a JavaScript application using a pattern similar to Redux, a popular library for state management. This involves creating a store, actions, and reducers to manage and update the state based on actions dispatched. The example used is a simplified version that demonstrates the core concepts without the complexity of Redux itself.

Jump into the lesson here: https://www.youtube.com/watch?v=gfuIP_clEVY&t=1s

1. **The Store**: It's a central place where the application's state lives. The store exposes a method to get the current state (`getState`), subscribe to changes (`subscribe`), and dispatch actions (`dispatch`).

2. **Actions**: These are plain JavaScript objects that represent an intention to change the state. Actions have a `type` property that indicates the kind of action being performed. Optional data can also be passed along with actions.

3. **Reducers**: Functions that take the current state and an action as arguments and return a new state. They describe how the state changes in response to actions sent to the store. Reducers must be pure functions, meaning they do not modify the arguments directly, have no side effects, and always produce the same output for the same input.

The lesson starts by setting up a simple state structure for tasks, filters, and app phases (e.g., idle, adding a task). It then moves on to defining actions that can be dispatched to change this state, such as adding a task or changing a sort order.

To make these updates, action creators are defined. These are helper functions that return action objects. When an action is dispatched to the store, a reducer function processes this action along with the current state to produce a new state. The lesson demonstrates setting up a single reducer function that handles different types of actions using a switch statement. Based on the action type, the reducer updates the state accordingly.

Throughout the lesson, emphasis is placed on the functional programming paradigm, highlighting its principles like avoiding side effects, using pure functions, and treating data immutably. This approach, as the lesson suggests, helps make the code more predictable, easier to debug, and scalable.

Finally, the lesson concludes by testing the store's functionality in a script, demonstrating subscribing to the store, dispatching actions, and observing how the state changes in response. The use of `console.log` is employed to visualize these changes and understand how the store, actions, and reducers work together to manage state in an application.