### Lesson: Utility Functions

Utility functions are fundamental building blocks in software development. They are small, reusable functions designed to perform common tasks that are used across different parts of an application. This lesson will explore the concept of utility functions, demonstrate how to create them, and show their practical uses in programming. Jump in here:

EMBED: https://www.youtube.com/watch?v=YeZe06M4Rgk

#### What Are Utility Functions?

Utility functions are typically short functions that encapsulate a specific operation or frequently used routine. These functions help keep your codebase DRY (Don't Repeat Yourself), meaning you write the function once and reuse it wherever needed, rather than rewriting the same code multiple times.

#### Characteristics of Utility Functions:
- **Reusability**: They can be used in various parts of an application or even across multiple projects.
- **Single Responsibility**: Each function performs a specific task and does it well.
- **Independence**: Functions are generally independent of the application's business logic.
- **Simplicity**: They are straightforward to implement and understand.

#### Example of a Basic Utility Function

Consider a simple utility function that checks if an array is empty:

```javascript
function isArrayEmpty(arr) {
  return arr.length === 0;
}
```
This function takes an array as an argument and returns `true` if the array is empty and `false` otherwise. You can use this function anywhere in your application where you need to check for an empty array.

#### Building a Utility Function: Case Study

Let's create a utility function that merges two arrays and removes all duplicate items. This is a common task when dealing with data in many applications.

1. **Define the Function**: First, we define the function `mergeArraysDedupe` which takes two arrays as parameters.
2. **Merge and Dedupe Logic**: Use the `Set` object to remove duplicates since a `Set` automatically removes duplicate entries.

```javascript
function mergeArraysDedupe(array1, array2) {
  const merged = [...array1, ...array2];
  return [...new Set(merged)];
}
```

3. **Usage**: This utility function can now be used in any part of the application to merge two arrays and eliminate duplicates.

```javascript
const array1 = [1, 2, 3];
const array2 = [2, 3, 4, 5];
const result = mergeArraysDedupe(array1, array2);
console.log(result); // Output: [1, 2, 3, 4, 5]
```

#### Advanced Utility Functions: Creating a Higher-Order Function

Higher-order functions are functions that operate on other functions, either by taking them as arguments or by returning them. These are especially useful in creating more dynamic and flexible utility functions.

Let's create a higher-order function that allows for customization of how arrays are merged:

```javascript
function createArrayMerger(joinFunction) {
  return function(array1, array2) {
    return joinFunction(array1, array2);
  };
}

const sumMerge = createArrayMerger((a, b) => a.concat(b));
const uniqueMerge = createArrayMerger((a, b) => [...new Set([...a, ...b])]);

const numbers1 = [1, 2, 3];
const numbers2 = [3, 4, 5];
console.log(sumMerge(numbers1, numbers2)); // Output: [1, 2, 3, 3, 4, 5]
console.log(uniqueMerge(numbers1, numbers2)); // Output: [1, 2, 3, 4, 5]
```

Utility functions streamline the development process by reducing redundancy and increasing the maintainability of your code. By abstracting common tasks into utility functions, developers can ensure that their codebase is cleaner, easier to manage, and less prone to errors. As we've seen, utility functions can range from simple tasks like checking array lengths to more complex operations facilitated by higher-order functions, making them an invaluable tool in the developer's toolkit.