# Lesson 6: Understanding and Using Props

One of React’s greatest strengths is its ability to create reusable components. Rather than duplicating the same component structure with different content, you can pass data into components using **props**. Props make your components flexible, scalable, and easier to maintain.

In this lesson, you'll learn what props are, how to use them, and how they support the idea of building dynamic and reusable UI components.

## Learning Objectives

By the end of this lesson, you will be able to:

- Define what props are and how they function in React.
- Pass data into a component using props.
- Refactor static components to accept dynamic content.
- Understand the difference between hardcoded values and props-driven design.

## Learning Resource (Lessons 6 - 8)

**Scrimba Course**: [Data-Driven React](https://scrimba.com/learn-react-c0e/~02fp)

## What Props Are and How to Use Them

**Props** (short for "properties") are arguments passed into React components. They allow you to customize a component’s behavior and appearance from the outside.

Props are passed like HTML attributes and received as parameters in a function component.

**Example:**

```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}!</h1>;
}

// In App.jsx
<Welcome name="Chris" />
<Welcome name="Sasha" />
```

Here, `name` is a prop passed to the `Welcome` component. You can reuse the same component but render different content based on its props.

## Reusability Through Dynamic Inputs

Using props, you can build a single component structure and reuse it multiple times with different data.

This is especially useful for components like:

- Cards
- List items
- Product previews
- Blog post summaries
- Travel entries

Example:

```jsx
function Card(props) {
  return (
    <div className="card">
      <img src={props.image} alt={props.title} />
      <h2>{props.title}</h2>
      <p>{props.description}</p>
    </div>
  );
}

// Usage in App.jsx
<Card
  image="paris.jpg"
  title="Trip to Paris"
  description="A lovely journey through the city of lights."
/>
<Card
  image="tokyo.jpg"
  title="Exploring Tokyo"
  description="Tech, tradition, and great food!"
/>
```

## Props vs. Hardcoded Content

Hardcoding content limits your ability to scale or adapt your UI.

**Hardcoded (inflexible):**

```jsx
function Entry() {
  return (
    <div>
      <h2>Trip to Paris</h2>
      <p>A lovely journey through the city of lights.</p>
    </div>
  );
}
```

**With props (reusable):**

```jsx
function Entry(props) {
  return (
    <div>
      <h2>{props.title}</h2>
      <p>{props.description}</p>
    </div>
  );
}
```

This small change enables you to reuse the component multiple times, each with different data.

## Practice Challenge: Refactor a Static Component to Use Props

Try this:

1. Start with a component like `TravelEntry.jsx` or `Card.jsx` that has hardcoded values.
2. Replace those hardcoded values with `props`:

   -` props.image, props.title, props.description`, etc.

3. In `App.jsx`, render that component multiple times with different props.

Example:

```jsx
// TravelEntry.jsx
function TravelEntry(props) {
  return (
    <div className="entry">
      <img src={props.image} alt={props.title} />
      <h2>{props.title}</h2>
      <p>{props.description}</p>
    </div>
  );
}

export default TravelEntry;

// App.jsx
import TravelEntry from "./TravelEntry";

function App() {
  return (
    <div>
      <TravelEntry
        image="nyc.jpg"
        title="New York Adventure"
        description="Visited Central Park and Broadway!"
      />
      <TravelEntry
        image="rome.jpg"
        title="Roman Holiday"
        description="History and architecture galore."
      />
    </div>
  );
}
```

## Summary

Props allow you to build flexible, reusable components that can display different content based on the data they receive. This aligns with React’s core idea of composability — building large UIs from small, data-driven pieces.
