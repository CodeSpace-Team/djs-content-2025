For this challenge, you will be required to use the two supplied video lessons as a reference to create **your own implementation** of a Redux-inspired store to manage the state of a basic counting Tally App. Note that you are not required to render any HTML to the screen, but instead should add subscriptions that merely log the new state to the console if it changes.

Please look at the video below, for a quick overview of the challenge. Check out the video here: https://www.youtube.com/watch?v=xILaC1FTqtU

See below user stories (in Gherkin syntax):

- **SCENARIO: Increment the counter by one**
    
    - GIVEN no interactions have been performed yet
    - WHEN the “getState” method is run
    - AND the result is logged to the console
    - AND the browser console is open
    - THEN the state should show a count of 0
- **SCENARIO: Increment the counter by one**
    
    - GIVEN no interactions have been performed yet
    - WHEN an “ADD” action is dispatched
    - AND another “ADD” action is dispatched
    - AND the browser console is open
    - THEN the state should show a count of 2
- **SCENARIO: Increment the counter by one**
    
    - GIVEN the current count in the state is 2
    - WHEN a “SUBTRACT” action is dispatched
    - AND the browser console is open
    - THEN the state should display a count of 1
- **SCENARIO: Resetting the Tally Counter**
    
    - GIVEN the current count in the state is 1
    - WHEN a “RESET” action is dispatched
    - AND the browser console is open
    - THEN the state should display a count of 0


### Project Brief: Redux-Inspired Store for Tally App

#### Overview

This project challenges you to create your own implementation of a Redux-inspired store to manage the state of a basic counting Tally App. Using the concepts covered in two provided video lessons, your task is to build a simple state management system. This system will not involve rendering HTML but will focus on managing state changes and logging them to the console.

#### Objectives

- Implement a global store to manage the application's state.
- Use functional programming concepts as inspired by Redux to handle state changes.
- Create subscriptions to log state changes to the browser console without rendering any HTML.

#### User Stories

The following scenarios describe the expected functionality of your Tally App:

1. **Increment Counter**
    - Initially, with no interactions, when the "getState" method is run and the result logged, the console should display a count of 0.
    
2. **Increment Counter Twice**
    - Without prior interactions, when an "ADD" action is dispatched twice, the console should display a count of 2.
    
3. **Decrement Counter**
    - Starting with a count of 2, when a "SUBTRACT" action is dispatched, the console should display a count of 1.
    
4. **Reset Counter**
    - With the count at 1, dispatching a "RESET" action should result in a count of 0 displayed in the console.

#### Requirements

- **Global Store:** Implement a store that is globally accessible throughout the application.
- **State Management:** The store should be able to handle actions like "ADD", "SUBTRACT", and "RESET" to adjust the state accordingly.
- **Subscriptions:** Implement a subscription mechanism to log state changes to the console.
- **Functional Programming:** Apply functional programming principles to manage state changes efficiently.

#### Evaluation Criteria

- **Understanding of Concepts:** Demonstrate a solid understanding of state management concepts and functional programming as discussed in the provided video lessons.
- **Implementation:** Your implementation should accurately reflect the user stories and requirements.
- **Code Quality:** Write clear, maintainable code that follows functional programming principles.

#### Resources

- Two video lessons provided as the foundational material for this project.
- [Refactor Guru on Observer Pattern](https://refactorguru.com) for additional insights into the pattern utilised in Redux and similar state management libraries.
- Coaches are available for guidance and to provide further context if you encounter difficulties.

#### Submission Guidelines

Ensure your project meets all the user stories and requirements before submitting it for review. Your understanding of the concepts and ability to apply them practically will be the primary focus of the evaluation.

In your 1-on-1 session with your coach, you will be required to demonstrate your understanding of all concepts covered in this module. It is at the discretion of the coach to determine what they will ask you, and how deeply they require you to understand specific concepts.

Good luck, and remember to reach out to your coach if you need any assistance!