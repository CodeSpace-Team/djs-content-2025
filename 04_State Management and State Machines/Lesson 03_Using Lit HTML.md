### Using Lit HTML

Lit HTML is a powerful library for building web applications with a focus on efficient rendering of dynamic HTML. This guide will introduce you to Lit HTML, explain how to set it up, and demonstrate how to create a basic web application using this technology. Jump into the walkthrough below:

EMBED: https://www.youtube.com/watch?v=iZW3T-TfRW0

#### 1. Introduction to Lit HTML

Lit HTML is a simple yet powerful library for creating and updating HTML in web applications. It leverages JavaScript's template literals to allow developers to write HTML templates in a clean and expressive syntax, which is then efficiently rendered and re-rendered as data changes. This approach is particularly efficient because Lit HTML only updates the parts of the template that change, rather than re-rendering the entire DOM.

#### 2. Setting Up Lit HTML

To begin using Lit HTML, you need to include it in your project. You can install it via npm or include it directly from a CDN. For simplicity, this guide will use the CDN approach.

##### Installing via CDN:

Include the following script tag in the header of your HTML document:

```html
<script type="module">
  import {html, render} from 'https://unpkg.com/lit-html?module';
</script>
```

#### 3. Creating a Basic Template

Lit HTML uses JavaScript template literals to define templates. Here's a simple template:

```javascript
import {html, render} from 'https://unpkg.com/lit-html?module';

const myTemplate = (name) => html`<p>Hello, ${name}!</p>`;

render(myTemplate('World'), document.body);
```

This code defines a template that receives a name and renders a greeting. The `render` function then applies this template to the `body` of the document, displaying "Hello, World!".

#### 4. Interacting with Templates

Lit HTML makes it easy to interact with templates by re-rendering them when data changes. Here’s how you can update the content dynamically:

```javascript
let userName = 'World';

const updateContent = (name) => {
  userName = name;
  render(myTemplate(userName), document.body);
};

setTimeout(() => updateContent('Lit HTML User'), 3000);
```

This example updates the displayed name to "Lit HTML User" after 3 seconds.

#### 5. Using Expressions and Conditions

You can use JavaScript expressions and conditions within your templates to control what gets rendered. Here's an example with a conditional rendering:

```javascript
const myConditionalTemplate = (user) => html`
  <div>
    ${user.loggedIn ? html`<p>Welcome back, ${user.name}!</p>` : html`<p>Please log in.</p>`}
  </div>
`;

const user = { loggedIn: true, name: 'Alice' };
render(myConditionalTemplate(user), document.body);
```

This template displays different messages based on whether the user is logged in.

#### 6. Looping and Lists

Rendering lists dynamically is straightforward with Lit HTML. Use standard JavaScript array methods like `map`:

```javascript
const users = ['Alice', 'Bob', 'Charlie'];

const userListTemplate = (users) => html`
  <ul>
    ${users.map(user => html`<li>${user}</li>`)}
  </ul>
`;

render(userListTemplate(users), document.body);
```

This code will render an unordered list of user names.

#### 7. Handling Events

Handling events in Lit HTML is done by directly embedding event listeners in the template:

```javascript
const buttonTemplate = () => html`
  <button @click="${() => alert('Clicked!')}">Click me!</button>
`;

render(buttonTemplate(), document.body);
```

This template renders a button that shows an alert when clicked.

#### Conclusion

Lit HTML offers a modern and efficient way to handle dynamic HTML content in your web applications. Its use of template literals and efficient updating strategy makes it a great choice for projects where performance and readability are crucial. With the basics covered in this guide, you can begin to explore more complex components and application structures using Lit HTML.