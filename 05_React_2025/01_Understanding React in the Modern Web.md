# Understanding React in the Modern Web

React has become the standard for building modern web user interfaces. But before writing our first line of JSX, it’s essential to understand **what React is**, **why it exists**, and **how it differs from other tools** in the web development ecosystem. In this lesson, we'll explore the landscape of front-end libraries and frameworks, and make a case for React.

## Learning Objectives

By the end of this lesson, you will be able to:

- Distinguish between **libraries** and **frameworks** in web development.
- Explain what React is and how it fits into the JavaScript ecosystem.
- Understand why React has become the **industry standard** for UI development.
- Identify situations where using React is (and isn’t) beneficial.
- Recognize React’s core philosophies: **composability** and **declarative programming**.

## Learning Resource (Lessons 1 - 5)

**Scrimba Course**: [Static Pages](https://scrimba.com/learn-react-c0e/~044d)

## Libraries vs. Frameworks

- **Library**: A collection of reusable code that gives you tools to solve specific problems. You stay in control of the flow (e.g., React, jQuery).
- **Framework**: An opinionated system that dictates how your app should be structured. The framework is in control (e.g., Angular, Next.js).

> _"Libraries give you tools; frameworks give you structure."_

React defines itself as a **library**, but with its ecosystem (React Router, Redux, etc.), it often behaves like a framework.

## Why Use React?

React is favored by developers and employers for several reasons:

- **Declarative syntax**: Tell React _what_ you want, not _how_ to do it.
- **Component-based**: Break your UI into independent, reusable pieces.
- **Ecosystem**: Massive library support and a large, active community.
- **Job demand**: React consistently ranks as one of the most in-demand skills in front-end development.
- **Community**: Discords, subreddits, and open source packages make learning and problem-solving easier.

## A Brief History of UI Development

- **2006** – jQuery simplifies DOM manipulation across browsers.
- **2010–2013** – Frameworks like AngularJS, Backbone, and Ember dominate.
- **2013** – React is released by Facebook. JSX and virtual DOM change how we build interfaces.
- **2016+** – Ecosystem explodes: Next.js, Gatsby, Remix, Solid, and more emerge.

React helped shift the web from monolithic HTML/CSS/JS files to **modular, reactive components**.

## When You Might _Not_ Need React

React is powerful, but not always necessary. Avoid it if:

- You're building a simple, one-page landing site.
- You want minimal bundle size and fastest loading time (especially on poor networks).
- You’re working on a legacy codebase incompatible with modern frameworks.

> React comes with a learning curve and setup complexity — it’s best used when you need its power.

## React’s Core Philosophies

### Composability

Build UIs from small, independent, **reusable components** — just like LEGO bricks.  
React encourages building apps as trees of encapsulated components.

### Declarative Programming

Describe _what_ the UI should look like for a given state — React handles the DOM updates.  
This contrasts with the **imperative** approach (manually selecting elements, updating the DOM).

```js
// Imperative (Vanilla JS)
const h1 = document.createElement("h1");
h1.textContent = "Hello!";
document.getElementById("root").appendChild(h1);

// Declarative (React JSX)
ReactDOM.createRoot(document.getElementById("root")).render(<h1>Hello!</h1>);
```

## Summary

In this foundational lesson, we explored how React differs from traditional JavaScript tools, why it’s considered the industry standard, and what philosophies make it powerful. React’s component-based and declarative model is what makes it both intuitive and scalable.
