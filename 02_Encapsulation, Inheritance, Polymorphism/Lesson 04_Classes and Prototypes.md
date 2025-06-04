### Classes and Prototypes

This lesson will look at built-in prototypal chaining on which JavaScript classes are built. We will specifically look at how prototypes are used in the JavaScript DOM and utilise this functionality to extend the HTML. This gives us the means to create custom, fully-encapsulated HTML elements.

In this lesson, we will look at how to use classes and the concept of inheritance to create objects with defined structure and behaviour quickly.

Jump into the lesson here: https://www.youtube.com/watch?v=M-3pDasXgBY

#### Encapsulation in OOP

Encapsulation is a fundamental concept in object-oriented programming (OOP). It involves bundling the data (attributes) and methods (functions) that operate on the data into a single unit, known as an object. Additionally, encapsulation restricts direct access to some of an object's components, which is a way of preventing accidental modification of data. This concept helps in maintaining code by:

- **Hiding the internal state**: Only necessary information is exposed, reducing complexity.
- **Reducing interdependencies**: Changes in one part of the system minimally affect others.

#### Factory Functions and Encapsulation

A factory function is a way to create objects. It can encapsulate and return an object with methods and properties. Here's an example illustrating encapsulation through a factory function for a tally app:

```javascript
function createTally() {
    let count = 0; // Encapsulated variable
    return {
        increment() { count += 1; },
        decrement() { count -= 1; },
        getCount() { return count; }
    };
}
```

This pattern allows for the creation of encapsulated modules or components, like the tally app, where the `count` variable is not directly accessible from the outside, ensuring maintainability and modular code.

#### Classes in JavaScript

JavaScript classes are syntactic sugar over the existing prototype-based inheritance and offer a clearer, more object-oriented syntax for creating objects and dealing with inheritance.

```javascript
class Counter {
    constructor() {
        this.value = 0;
    }

    increase(amount) {
        this.value += amount;
    }

    decrease(amount) {
        this.value -= amount;
    }

    display() {
        console.log(this.value);
    }
}
```

A class encapsulates data for the object and methods to interact with that data. It simplifies the creation of objects and managing inheritance.

#### Prototypal Inheritance Versus Classical Inheritance

JavaScript utilises prototypal inheritance, which differs from classical inheritance found in languages like Java or C++. In prototypal inheritance:

- Objects inherit from other objects directly.
- It allows for more flexible and dynamic relationships.

In contrast, classical inheritance is more structured but can become rigid and complex, leading to difficulties in maintenance and understanding.

In programming, understanding how objects or classes share properties and methods is fundamental. Two primary models of inheritance help facilitate this: prototypal inheritance and classical inheritance. Below, we'll explore the differences between these two models, focusing on their implementation in JavaScript (for prototypal inheritance) and in languages like Java or C++ (for classical inheritance).

#### What is Prototypal Inheritance?

Prototypal inheritance is a feature of JavaScript and other similar languages. It operates on the principle that objects can inherit properties and methods directly from other objects. Here are the key characteristics:

- **Direct Inheritance**: Objects can directly inherit from other objects. There is no need for classes as a middleman.
- **Dynamic Relationships**: Because objects inherit directly from other objects, you can create and modify inheritance relationships at runtime, making it very flexible.
- **Simpler and More Flexible**: Prototypal inheritance can be more straightforward to understand and use because it involves less boilerplate than classical inheritance systems.

#### What is Classical Inheritance?

Classical inheritance, on the other hand, is a model used by languages like Java, C++, and C#. It's characterized by a more rigid, class-based structure. Here's how it differs:

- **Class-Based**: Inheritance is defined through classes. A subclass inherits from a superclass, defining a clear hierarchy.
- **Static Structure**: The inheritance relationships are defined at compile time and cannot be changed at runtime. This leads to a more predictable structure but reduces flexibility.
- **Complexity with Deep Hierarchies**: As projects grow and hierarchies deepen, classical inheritance can become complex, making it harder to manage and understand.

#### Comparison Table

To further clarify the differences, here's a comparison table:

| Feature | Prototypal Inheritance | Classical Inheritance |
|---------|------------------------|-----------------------|
| Structure | Based on objects | Based on classes |
| Flexibility | High, allows for dynamic changes | Lower, due to static definition |
| Complexity | Lower, with less boilerplate | Can become high in deep hierarchies |
| Use Case | JavaScript and similar languages | Java, C++, C#, and similar languages |

Both inheritance models have their advantages and suitable use cases. Prototypal inheritance offers flexibility and simplicity, making it ideal for dynamic and less complex systems. Classical inheritance provides a clear and structured hierarchy, beneficial for large-scale applications where predictability and traditional object-oriented programming patterns are preferred. The choice between prototypal and classical inheritance ultimately depends on the specific requirements of the project and the language being used.

### Connecting Web Components with Class-Based Inheritance

Building on our understanding of prototypal versus classical inheritance, let's explore how class-based inheritance is applied in the development of web components. Web components represent a powerful standard in web development, allowing for the creation of custom, reusable, and fully encapsulated HTML elements. These are made possible through the use of class-based inheritance.

#### What Are Web Components?

Web components are a set of web platform APIs that allow you to create new custom, reusable, encapsulated HTML tags to use in web pages and web applications. They consist of three main technologies:

1. **Custom Elements**: Enable the creation of custom HTML elements.
2. **Shadow DOM**: Provides encapsulation for the JavaScript and CSS in a web component.
3. **HTML Templates**: Facilitate the declaration of the structure of a web component.

#### Using Class-Based Inheritance in Web Components

When defining a web component, developers use the class syntax introduced in ES6 (ECMAScript 2015), which is syntactical sugar over JavaScript's prototypal inheritance model, to create a more familiar class-based inheritance structure. Here's a simplified breakdown:

- **Class Syntax**: Utilises the `class` keyword to define a new custom element as a class.
- **Extending HTML Elements**: By extending the `HTMLElement` class, custom elements can inherit properties and methods from it, allowing them to behave like standard HTML elements.
- **Constructor and Super**: The `constructor` method is a special method for creating and initialising an object created with a class. Calling `super()` within it is crucial as it calls the constructor of the parent class (`HTMLElement` in this case), ensuring the custom element has all the necessary initialisation from its HTML element lineage.

#### Example Explained

The example code snippet demonstrates how to define a new web component:

```javascript
class CustomElement extends HTMLElement {
    constructor() {
        super(); // Calls the parent class's constructor
        // Define functionality specific to this custom element
    }
}
```

- This class `CustomElement` extends `HTMLElement`, indicating that it inherits from the basic HTML element class, allowing it to act like a native HTML element.
- The `constructor` calls `super()`, ensuring that the element is properly set up according to the standards of HTML elements.
- After calling `super()`, you can add custom functionality specific to the new element.

#### Practical Implications

Using class-based inheritance to define web components showcases how classical inheritance principles are applied in modern web development:

- **Encapsulation**: Web components encapsulate their structure, style, and behaviour, leading to cleaner and more maintainable codebases.
- **Reusability**: By defining custom elements, developers can reuse these components across different projects or within different parts of the same project, promoting efficiency and consistency.
- **Extensibility**: Extending from existing HTML elements allows for enhancing and customising elements without starting from scratch, leveraging the built-in functionality of the web platform.

While JavaScript primarily uses prototypal inheritance, the class syntax offers a way to employ classical inheritance principles, as demonstrated in the creation of web components. This synergy allows developers to benefit from the structured, hierarchical approach of classical inheritance when building complex and maintainable web applications.

The concepts of encapsulation and inheritance in OOP are pivotal for creating maintainable and modular code. JavaScript's approach, involving prototypal inheritance and the syntactic sugar of classes, offers flexibility and dynamism. Through factory functions, classes, and web components, developers have powerful tools for developing structured, encapsulated, and reusable code, catering to the modern web's demands.