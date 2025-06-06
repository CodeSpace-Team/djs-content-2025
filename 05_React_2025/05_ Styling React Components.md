# Styling React Components

Styling in React follows many of the same principles as traditional web development, but with some important distinctions. While you still use CSS, the way you reference styles in JSX and the way you manage assets like images and fonts is slightly different.

In this lesson, you'll learn how to style your React components using both external and inline CSS, and apply responsive design principles with Flexbox.

## Learning Objectives

By the end of this lesson, you will be able to:

- Use `className` correctly in JSX for applying CSS styles.
- Import and organize CSS files in a React project.
- Understand when to use inline styles vs. external stylesheets.
- Apply Flexbox for responsive layout and alignment.

## Using className Instead of class

In JSX, you can't use `class` like you would in HTML because `class` is a reserved keyword in JavaScript. Instead, you must use `className`.

**Example:**

```jsx
function Header() {
  return <h1 className="site-title">Welcome to My Site</h1>;
}
```

React automatically translates `className` into `class` in the final HTML output.

## Importing CSS

React allows you to import CSS files directly into your component files.

You can create a `styles.css` (or any `.css` file) and import it like this:

```jsx
import "./styles.css";
```

If you're following a modular approach, you might have individual CSS files for each component (e.g., `Header.css`, `Main.css`, etc.), and import them into their respective components.

```jsx
// Header.jsx
import "./Header.css";

function Header() {
  return <header className="header">React App</header>;
}
```

## Inline vs. External Styles

You can also use inline styles in JSX. These are defined using JavaScript objects, with camelCase property names.

**Example:**

```jsx
const buttonStyles = {
  backgroundColor: "blue",
  color: "white",
  padding: "10px 20px",
  borderRadius: "5px",
};

function MyButton() {
  return <button style={buttonStyles}>Click Me</button>;
}
```

### When to use inline styles:

- Dynamic styles based on props or state
- Simple one-off adjustments
- Prototyping or debugging

### When to use external styles:

- Theming and consistent styling
- Reusability and separation of concerns
- Complex layouts and media queries

## Responsive Layout with Flexbox

Flexbox is ideal for building layouts that adapt to different screen sizes.

**Basic Flexbox Example (CSS):**

```css
.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

**In your JSX:**

```jsx
function Navbar() {
  return (
    <nav className="container">
      <h1>Logo</h1>
      <ul className="nav-links">
        <li>Home</li>
        <li>About</li>
        <li>Contact</li>
      </ul>
    </nav>
  );
}
```

You can combine Flexbox with media queries in your external CSS for full responsiveness.

## Practice Challenge: Style a Multi-Part Layout

Try the following:

1. Create or reuse components: `Header, Main`, and `Footer`.
2. Add class names to each section for styling.
3. Create a CSS file (e.g., `App.css` or individual files per component).
4. Add styling rules to:
   - Apply padding/margins
   - Use Flexbox in the header for layout
   - Set fonts, background colors, etc.
5. Import the CSS into your component files.

## Summary

In this lesson, you learned how to apply styles in React using `className`, CSS imports, and inline style objects. You also practiced building responsive layouts using Flexbox. Styling in React supports both traditional CSS workflows and component-scoped designs.
