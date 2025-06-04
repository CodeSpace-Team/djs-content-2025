

### Introduction to Web Components

Web components allow developers to encapsulate and reuse code in web applications by creating custom, reusable HTML tags. They consist of three main technologies: Custom Elements, Shadow DOM, and HTML templates.

In this lesson, we will explore using what we've learnt about inheritance to build custom web components. Then, we can use these custom components in our websites, just like the standard ones.

Check out the lesson here: https://www.youtube.com/watch?v=XjMOPMZI98o

### Custom Elements

Custom elements enable developers to define new HTML tags with custom behaviour. In the lesson, a `Task` component is created to demonstrate how to convert a factory function into a class-based component. This conversion illustrates the use of classes in JavaScript as syntactic sugar over traditional functions, making code more intuitive and organised.

#### Creating a Custom Element

1. **Define the Class**: The `Task` class is defined with properties and methods. Properties like `id`, `title`, and `completed` are defined within the constructor.

2. **Export the Class**: The class is exported to be used in other parts of the application.

3. **Register the Custom Element**: The custom element is registered using `customElements.define('element-name', ClassName)`, ensuring the name contains a dash (`-`) to avoid conflicts with future HTML elements.

### Shadow DOM

The Shadow DOM provides encapsulation for web components, keeping the component's internal features separate from the main document DOM. This encapsulation prevents styles from leaking out of the component and external styles from affecting the component.

#### Using Shadow DOM

1. **Attach Shadow DOM to Element**: Use `element.attachShadow({ mode: 'open' })` to attach a shadow root to the custom element. The mode can be 'open' or 'closed'.

2. **Add Content to Shadow DOM**: Content is added to the shadow root using regular DOM methods like `appendChild` or by setting the `innerHTML`.

### HTML Templates

HTML templates are used to define the markup structure of web components in a more efficient and performant manner.

#### Creating and Using Templates

1. **Define Template in HTML**: Use the `<template>` tag to define a chunk of HTML markup that will not be rendered until the template is used.

2. **Clone and Insert the Template**: In JavaScript, clone the template content using `template.content.cloneNode(true)` and insert it into the shadow DOM or the main document.

### Example Implementation

The lesson concludes with implementing a task management application using these concepts. It demonstrates creating tasks, encapsulating each task in a web component, and managing the application's state.

#### Key Operations

- **Adding a Task**: Users can add tasks through an input form, which is also encapsulated as a web component.
- **Displaying Tasks**: Tasks are displayed in a list, with each task as a custom element.
- **Interacting with Tasks**: Tasks can be marked as completed, edited, or deleted through user interactions.

Web components offer a powerful way to create encapsulated, reusable, and maintainable code structures in web development. By understanding and applying custom elements, the Shadow DOM, and HTML templates, developers can build complex web applications more efficiently.

