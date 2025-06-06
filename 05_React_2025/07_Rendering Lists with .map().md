# Rendering Lists with .map()

Up until now, you’ve likely built individual components and manually repeated them to simulate multiple entries. But in real applications, UI elements are often generated from structured data. React provides an efficient and expressive way to handle this pattern using JavaScript’s `.map()` method.

In this lesson, you’ll learn how to render components dynamically from a data array, passing information through props, and making your UI scalable and maintainable.

## Learning Objectives

By the end of this lesson, you will be able to:

- Render components dynamically from an array of data.
- Use the `.map()` method to iterate over a dataset in React.
- Assign unique `key` props when rendering lists.
- Understand how component reusability scales with dynamic rendering.

## Dynamic Rendering from Arrays

Imagine you have a dataset stored in a separate file like `data.js`:

```js
// data.js
export default [
  {
    id: 1,
    title: "Mount Fuji",
    location: "Japan",
    imageUrl: "https://source.unsplash.com/WLxQvbMyfas",
    description: "A beautiful view of Mount Fuji...",
    googleMapsUrl: "https://goo.gl/maps/MountFuji",
    startDate: "2021-01-12",
    endDate: "2021-01-24",
  },
  {
    id: 2,
    title: "Sydney Opera House",
    location: "Australia",
    imageUrl: "https://source.unsplash.com/sydney",
    description: "Iconic landmark with stunning views...",
    googleMapsUrl: "https://goo.gl/maps/Sydney",
    startDate: "2021-02-01",
    endDate: "2021-02-10",
  },
];
```

This array contains structured data about travel entries.

## Using `.map()` to Render Multiple Components

To render a component for each object in the array, you use `.map()` inside your parent component — often `App.jsx`.

Here’s how:

```jsx
import data from "./data";
import TravelEntry from "./components/TravelEntry";

function App() {
  const entries = data.map((item) => <TravelEntry key={item.id} {...item} />);

  return (
    <div>
      <Header />
      {entries}
    </div>
  );
}
```

This will dynamically render one `TravelEntry` component per item in the array. Using `{...item}` spreads the object’s properties as props.

You can also write it out explicitly for clarity:

```jsx
<TravelEntry
  key={item.id}
  title={item.title}
  imageUrl={item.imageUrl}
  location={item.location}
  description={item.description}
  startDate={item.startDate}
  endDate={item.endDate}
  googleMapsUrl={item.googleMapsUrl}
/>
```

## Using Key Props

React requires a `key` prop when rendering lists to track which items change, update, or are removed.

- A `key` must be unique **among siblings**.
- Ideally, use a unique `id` from your data.

Avoid using the array index as a key unless there’s no other option.

```jsx
data.map((item) => <TravelEntry key={item.id} {...item} />);
```

## Practice Challenge: Render a List of Entries from data.js

1. Create a `data.js` file with at least 3 destination objects (see structure above).
2. In your `App.jsx`, import `data.js`.
3. Map over the data array to generate multiple `<TravelEntry />` components.
4. Pass props from each object into the component.
5. In `TravelEntry.jsx`, display the props dynamically:

   ```jsx
   function TravelEntry(props) {
     return (
       <article>
         <img src={props.imageUrl} alt={props.title} />
         <h2>{props.title}</h2>
         <p>{props.location}</p>
         <p>{props.description}</p>
         <a href={props.googleMapsUrl}>View on Google Maps</a>
       </article>
     );
   }

   export default TravelEntry;
   ```

6. Add a `key` to each rendered entry in your `.map()` call.

## Summary

You’ve now learned how to render lists of components using `.map()` and pass dynamic data using props. This approach unlocks React’s real power: building flexible, data-driven interfaces from reusable components. This technique is fundamental for building apps like product catalogs, dashboards, media galleries, and more.
