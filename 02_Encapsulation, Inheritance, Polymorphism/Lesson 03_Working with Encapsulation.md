# Lesson: Working with Encapsulation

Encapsulation in web development involves creating components with private internal states that can only be interacted with through a public interface. This concept, fundamental to object-oriented programming (OOP), ensures the component's internal workings are hidden, safeguarding from external changes unless through specified methods. JavaScript offers various ways to achieve encapsulation, crucial for developing maintainable and scalable web applications.

Jump into the lesson here: https://www.youtube.com/watch?v=Z_deOSGzwKk

## Implementing Encapsulation

### 1. Creating Components with Private States
Encapsulation in web components involves defining properties and methods that are only accessible within the component. This can be achieved using closures, classes, or the newer Web Components standards which use the Shadow DOM.

### 2. Web Components and Encapsulation
Web Components provide a standard way to create encapsulated, reusable custom elements. These components encapsulate their HTML structure, CSS styles, and JavaScript functionality, preventing external interference and clashes with other parts of a web application.

### 3. Using Classes for Encapsulation
JavaScript classes, introduced in ECMAScript 2015 (ES6), offer a more traditional OOP approach to encapsulation. By using classes, developers can define private properties and methods that are not accessible from outside the class instance.

### Example: Encapsulating a Task Component
Consider a task management application where each task is a component with properties such as title, due date, and urgency. Encapsulation allows these properties to be modified only through the component's methods, preventing direct access to the component's internal state.

```javascript
class Task {
    constructor(title, dueDate) {
        let _title = title;
        let _dueDate = dueDate;

        // Public method to get the task's title
        this.getTitle = function() {
            return _title;
        };

        // Public method to set the task's title
        this.setTitle = function(newTitle) {
            _title = newTitle;
        };
    }
}
```

In this example, `_title` and `_dueDate` are private variables accessible only within the `Task` class. The public methods `getTitle` and `setTitle` provide a controlled way to access and modify these properties.

## Advantages of Encapsulation in Web Development

1. **Modularity:** Encapsulation helps in building web applications with well-defined, modular components that are easy to understand, develop, and test.
2. **Maintainability:** By restricting access to the internal state of components, encapsulation makes it easier to debug and maintain web applications.
3. **Reusability:** Encapsulated components are more reusable across different parts of a web application or even across projects.

Encapsulation is a powerful concept in web development that aids in creating robust, maintainable, and scalable web applications. Whether using traditional OOP techniques with classes or leveraging Web Components, encapsulation ensures that components are well-protected and interact with the rest of the application in a controlled manner. As web development evolves, understanding and applying encapsulation principles becomes increasingly important for building sophisticated web applications.

# Further reading

To extend your learning of concepts covered in this module, you are required to work through the following resources:

           - JavaScript Factory Functions with ES6+ by Eric Elliot: https://medium.com/javascript-scene/javascript-factory-functions-with-es6-4d224591a8b1

           - JAVASCRIPT.INFO: Property getters and setters: https://javascript.info/property-accessors

           - WATCH: Factory Functions in JavaScript by Fun Fun Function: https://www.youtube.com/watch?v=ImwrezYhw4w

           - WATCH: JavaScript getters and setters by Bro Code: https://www.youtube.com/watch?v=QSbl0Y-5aSM