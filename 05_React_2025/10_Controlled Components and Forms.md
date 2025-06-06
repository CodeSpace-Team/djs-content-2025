# Controlled Components and Forms

Forms are essential to most web applications — whether you're collecting user input, submitting contact messages, or searching a database. In React, input elements like text fields are managed using **controlled components**, where the input’s value is tied to component state.

In this lesson, you’ll learn how to build controlled form inputs, manage multiple fields in state, and handle form submissions the React way.

## Learning Objectives

By the end of this lesson, you will be able to:

- Understand what a controlled component is in React.
- Use `value` and `onChange` to track user input.
- Store and manage form values in component state.
- Handle form submission events and access form data.

## Controlled Inputs with value and onChange

In React, a **controlled component** is an input element whose value is controlled by React state.

```jsx
import { useState } from "react";

function NameInput() {
  const [name, setName] = useState("");

  return (
    <input
      type="text"
      value={name}
      onChange={(e) => setName(e.target.value)}
      placeholder="Enter your name"
    />
  );
}
```

Here:

- The `value` prop ensures the input always shows the current state.
- The `onChange` handler updates state when the user types.

Without this, React cannot control the input — which is why uncontrolled inputs are generally avoided.

## Managing Form State

When managing a form with multiple fields, you can use one `useState` per field:

```jsx
const [firstName, setFirstName] = useState("");
const [email, setEmail] = useState("");
```

Or use a single object to manage all fields:

```jsx
const [formData, setFormData] = useState({
  firstName: "",
  email: "",
});

function handleChange(e) {
  const { name, value } = e.target;
  setFormData((prevData) => ({
    ...prevData,
    [name]: value,
  }));
}
```

Then connect each input:

```jsx
<input
  type="text"
  name="firstName"
  value={formData.firstName}
  onChange={handleChange}
/>
```

This pattern works well for larger forms.

## Handling Form Submission

To handle a form submission:

- Add `onSubmit` to the `<form>` element.
- Use `event.preventDefault()` to stop the page from reloading.
- Access the state values for processing or API requests.

Example:

```jsx
function ContactForm() {
  const [formData, setFormData] = useState({
    name: "",
    email: "",
  });

  function handleChange(e) {
    const { name, value } = e.target;
    setFormData((prev) => ({ ...prev, [name]: value }));
  }

  function handleSubmit(e) {
    e.preventDefault();
    console.log("Form submitted:", formData);
    // Clear form if needed
    setFormData({ name: "", email: "" });
  }

  return (
    <form onSubmit={handleSubmit}>
      <input
        type="text"
        name="name"
        value={formData.name}
        onChange={handleChange}
        placeholder="Name"
      />
      <input
        type="email"
        name="email"
        value={formData.email}
        onChange={handleChange}
        placeholder="Email"
      />
      <button type="submit">Submit</button>
    </form>
  );
}
```

## Practice Challenge: Build a Contact Form and Track Field Values in State

1. Create a `ContactForm` component.
2. Add two input fields: name and email.
3. Use `useState` to track each field (or a single `formData` object).
4. Display the entered values live below the form.
5. Log the full data on submission and reset the form fields.

## Summary

You’ve now learned how to build and manage **controlled components** in React, allowing you to track and update form input fields using state. You also practiced handling form submissions in a declarative and user-friendly way. This is essential for building robust forms, authentication pages, or search tools.
