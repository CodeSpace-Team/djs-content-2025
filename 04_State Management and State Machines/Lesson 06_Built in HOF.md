https://www.youtube.com/watch?v=2GAINTytqxs


### Lesson on Built-in Higher-Order Functions in JavaScript

#### Introduction

In this lesson, we will explore JavaScript's built-in higher-order functions (HOFs) that operate on arrays. These functions are essential for writing concise and expressive code. By understanding these functions, you can efficiently perform operations like searching, sorting, filtering, and transforming data within arrays.

#### Understanding Higher-Order Functions

Higher-order functions are functions that take other functions as arguments or return functions as their result. This characteristic makes them incredibly powerful for creating flexible and reusable code. In JavaScript, arrays come equipped with several higher-order functions that simplify complex operations.

#### Common Higher-Order Functions on Arrays

1. **`Array.prototype.map()`**
   - **Purpose**: Transforms each element in the array according to the function passed to it.
   - **Example Usage**: Convert all names in an array to uppercase.
     ```javascript
     const names = ['Alice', 'Bob', 'Charlie'];
     const upperCaseNames = names.map(name => name.toUpperCase());
     ```

2. **`Array.prototype.filter()`**
   - **Purpose**: Creates a new array with all elements that pass the test implemented by the provided function.
   - **Example Usage**: Filter out all scores that are below 50.
     ```javascript
     const scores = [45, 75, 62, 37, 89];
     const passingScores = scores.filter(score => score >= 50);
     ```

3. **`Array.prototype.reduce()`**
   - **Purpose**: Reduces an array to a single value by applying a function to each element and carrying over the return value from the computation.
   - **Example Usage**: Calculate the total sum of an array of numbers.
     ```javascript
     const numbers = [1, 2, 3, 4, 5];
     const total = numbers.reduce((accumulator, currentValue) => accumulator + currentValue, 0);
     ```

4. **`Array.prototype.forEach()`**
   - **Purpose**: Executes a provided function once for each array element.
   - **Example Usage**: Print each element in the array.
     ```javascript
     const array = ['a', 'b', 'c'];
     array.forEach(element => console.log(element));
     ```

5. **`Array.prototype.some()`**
   - **Purpose**: Tests whether at least one element in the array passes the test implemented by the provided function.
   - **Example Usage**: Check if any elements are odd in the array.
     ```javascript
     const array = [2, 4, 6, 8, 9];
     const hasOdd = array.some(num => num % 2 !== 0);
     ```

6. **`Array.prototype.every()`**
   - **Purpose**: Checks if all elements in the array pass the test implemented by the provided function.
   - **Example Usage**: Verify that all numbers are positive.
     ```javascript
     const allPositive = numbers.every(num => num > 0);
     ```

7. **`Array.prototype.find()`**
   - **Purpose**: Finds the first element in the array that satisfies the provided testing function.
   - **Example Usage**: Find the first number greater than 10.
     ```javascript
     const firstHighNum = numbers.find(num => num > 10);
     ```

8. **`Array.prototype.findIndex()`**
   - **Purpose**: Returns the index of the first element in the array that satisfies the provided testing function.
   - **Example Usage**: Find the index of the first number greater than 10.
     ```javascript
     const index = numbers.findIndex(num => num > 10);
     ```

#### Practical Exercise

- Create an array of student objects with properties `name` and `grade`.
- Use `map()` to create an array of names.
- Use `filter()` to extract students with grades above 75.
- Use `find()` to search for the first student who has failed (assuming a passing grade is 60).
- Use `reduce()` to calculate the average grade of the class.


Built-in higher-order functions in JavaScript provide powerful tools for manipulating arrays without writing extensive boilerplate code. By leveraging these functions, developers can write more readable, maintainable, and concise code. Practice using these functions to become proficient in handling common data manipulation tasks in JavaScript.