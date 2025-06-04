# Lesson: Creating Encapsulation 

In object-oriented programming (OOP), the concept of encapsulation is central to creating abstractions. These abstractions help in solving specific programming problems by allowing us to bundle data (attributes) and methods (functions) that operate on the data into a single unit, known as an object. This approach not only helps in structuring the software in a more logical way but also in safeguarding the internal state of the object from unintended modifications from outside the object.

We need to introduce encapsulation to talk about Object Orientated Programming (OOP). Encapsulation is at the heart of OOP since it allows grouping of related data and behaviour behind an abstracted interface. This enhances code structure, reusability, and maintainability.

Jump into the lesson here: https://www.youtube.com/watch?v=zMxWBV8yn-8

## Understanding Encapsulation

Encapsulation is one of the four fundamental OOP concepts, the others being inheritance, polymorphism, and abstraction. It refers to the bundling of data and methods that operate on the data within one unit, such as a class in Java or a prototype in JavaScript, and restricting access to some of the object's components. This means that the internal state of an object is hidden from the outside, only exposing a controlled interface (for example, public methods) to the outside world.

### Benefits of Encapsulation:
1. **Modularity:** The source code for an object can be written and maintained independently of the source code for other objects.
2. **Information Hiding:** By interacting only with an object's methods, the details of its internal implementation remain hidden from the outside world.
3. **Code Reusability:** Encapsulation also leads to an object-oriented inheritance concept, where classes can inherit common properties from other classes.

### How to Achieve Encapsulation:
1. **Using Classes:** Most OOP languages use classes to encapsulate data and methods. A class serves as a blueprint for creating objects (instances).
2. **Access Modifiers:** Keywords like `private`, `protected`, and `public` in languages such as Java and C++ control access to the object's components.

## Example in JavaScript

JavaScript, being a prototype-based language, has a slightly different approach to OOP. Although it introduced classes in ES6 (ECMAScript 2015), these are primarily syntactical sugar over its existing prototype-based inheritance. Here's a simple example of encapsulation in JavaScript:

```javascript
function createCounter() {
    let value = 0;

    return {
        // Method to increase the counter
        increase() {
            value++;
        },
        // Method to decrease the counter
        decrease() {
            value--;
        },
        // Method to display the counter value
        display() {
            console.log(value);
        }
    };
}

const counter = createCounter();
counter.increase();
counter.display(); // Output: 1
```

In JavaScript, the way objects inherit features and properties from one another is through a system known as "prototype-based inheritance." Before the introduction of classes in ES6 (a version of JavaScript introduced in 2015), JavaScript used prototypes directly for inheritance. This means that objects can have a prototype object, which they can inherit properties and methods from.

The term "syntactical sugar" means making changes or additions to the syntax of a language that don't add new features but make things easier to write or read. So, when we say that classes in JavaScript are "syntactical sugar over its existing prototype-based inheritance," we mean that classes provide a clearer and more straightforward way to set up inheritance in your code. They make the code look cleaner and more like how other programming languages handle object-oriented programming (OOP), but underneath, JavaScript still uses its original prototype-based system to make it all work.

To put it simply, classes in JavaScript offer a nicer, more familiar way to write code that deals with inheritance without changing how inheritance actually works in JavaScript.

The example illustrates the concept of encapsulation, another important idea in object-oriented programming. Encapsulation means bundling the data (variables) and the methods that work on the data into a single unit, or object, and controlling access to that data. This is often used to hide the internal state of an object from the outside world. In the `createCounter` function example, the `value` variable is encapsulated within the function. It cannot be accessed directly from outside the function, thus adhering to the principles of encapsulation. Only the methods `increase`, `decrease`, and `display` are exposed, allowing controlled interaction with `value`. This shows how encapsulation helps in building secure and maintainable code.

Encapsulation is a powerful concept in object-oriented programming that helps developers build more secure, modular, and maintainable code. By hiding the internal state of objects and exposing only what is necessary through a well-defined interface, encapsulation ensures that objects can be used without the need to understand their internal workings. This abstraction makes it easier to develop, test, and maintain complex software systems.


