# Lesson Plan — Deep Dive into SOLID Principles & Abstraction in JavaScript

---

## 1. Why This Lesson?

Before diving into frameworks like React or Vue, it’s crucial to understand how to **design clean, adaptable code**. This lesson focuses on the **SOLID principles** and **modular abstraction** in JavaScript—ideas that empower you to build systems that are easy to extend, debug, and test.

"Good design is not about perfection—it's about flexibility and clarity."

---

## 2. Learning Outcomes

By the end of this session, you should be able to:

| #   | You will be able to …                                                                  |
| --- | -------------------------------------------------------------------------------------- |
| 1   | Organize code into well-named, reusable modules.                                       |
| 2   | Apply the **Single Responsibility Principle (SRP)** to create focused functions.       |
| 3   | Design abstractions that follow the **Dependency Inversion Principle (DIP)**.          |
| 4   | Implement the **Liskov Substitution Principle (LSP)** using interfaces and base types. |
| 5   | Identify and avoid overengineering when applying SOLID.                                |

---

## 3. Prerequisites

- JavaScript functions, objects, and modules
- Basic understanding of callbacks and data flow
- Familiarity with a Todo-style or user-driven app (e.g. event, task, or list manager)

---

## 4. Setup — Module-Based Organization

Start with a project structured like this:

```
/src
  ├── index.js
  ├── helpers/
  │     └── dom.js
  ├── core/
  │     └── taskManager.js
  │     └── eventManager.js
  └── models/
        └── attendee.js
        └── employee.js
```

Each module:

- Has a **single responsibility**
- Exports only what’s necessary
- Avoids mixing DOM, data, and control logic

---

## 5. Principle 1: SRP (Single Responsibility Principle)

### Example: `addTask`

```js
function addTask({ title }, repo, render) {
  const task = { id: Date.now(), title, done: false };
  repo.save(task);
  render(task);
}
```

- One function = one responsibility (coordinating task creation).
- Avoid combining `querySelector`, `localStorage`, and `appendChild` in one place.

  _SRP is about clarity and testability. If you can test it without DOM or state, you’re doing it right._

---

## 6. Principle 2: DIP (Dependency Inversion Principle)

Design from the **top down**—from _use_, not _implementation_:

```js
// High-level function
function sendInvites(attendees, inviteFn) {
  attendees.forEach((att) => inviteFn(att));
}
```

Rather than:

```js
function sendInspectorInvites(inspectors) {
  inspectors.forEach((i) => sendSMS(i.phone));
}
```

- External code supplies the dependency (`inviteFn`)
- _Caller decides how to handle it_ = more reusable and testable code

---

## 7. Principle 3: LSP (Liskov Substitution Principle)

If `Inspector` and `Colleague` are both `Attendee`s, they should work interchangeably:

```js
// Shared interface
function invite(attendee) {
  console.log(`Inviting ${attendee.name}`);
  if (attendee.notify) attendee.notify();
}

// Both follow the same structure
const colleague = { name: "Sam", notify: () => alert("Email sent!") };
const inspector = { name: "Ada", notify: () => sendSMS("...") };

invite(colleague);
invite(inspector);
```

- Swap roles without breaking logic
- Avoid `if (role === 'inspector')` checks in multiple places

---

## 8. Abstract First, Then Implement

"Think about how you'd _use_ this function first. Then write it."

Designing APIs by expected use prevents overengineering and poor naming.

Example:

```js
// Bad: exposes too much internal logic
taskRepo.processTask(task, false, true);

// Good: intent is clear
taskRepo.markDone(task.id);
```

---

## 9. Discussion: When NOT to Apply These Principles

- Don’t apply every principle to every project
- Don’t split files just for the sake of it
- Avoid building rigid inheritance trees (favor composition)

**Instead:**

- Use principles as _guides_, not rules
- Start simple; refactor toward abstraction when duplication appears
- Balance extensibility with clarity

---

## 10. Group Activity (30–45 min)

**Goal:** Build an `EventManager` with SRP, DIP, and LSP in mind.

| Task | Description                                                              |
| ---- | ------------------------------------------------------------------------ |
| 1.   | Create a module to manage `attendees`                                    |
| 2.   | Create a base type (object literal or factory) that supports `.invite()` |
| 3.   | Create `EventManager` that takes any `attendee` and calls `.invite()`    |
| 4.   | Extend it to support RSVP status tracking                                |
| 5.   | Refactor with TS-style JSDoc or `@ts-check` for type safety              |

---

## 11. Debrief & Reflection

| Question                                 | Reflection Prompt                            |
| ---------------------------------------- | -------------------------------------------- |
| When did abstraction help?               | Identify one place it reduced complexity     |
| When did it hurt?                        | Did you abstract too early? Too generically? |
| What principle made your design cleaner? | SRP, DIP, LSP? Why?                          |

---

## 12. Further Reading & Exercises

- Robert C. Martin – _SOLID Principles_
- Kent C. Dodds – _“Write Code for the User First”_
- Refactor a nested `switch/case` logic using LSP-style interfaces
- Revisit an older project and identify SRP/DIP violations

---

## Summary Board

| Principle | Motto                   | Example                                  |
| --------- | ----------------------- | ---------------------------------------- |
| SRP       | “One function, one job” | `addTask()` only coordinates             |
| DIP       | “Design from use”       | `sendInvites(attendees, fn)`             |
| LSP       | “Swap parts freely”     | `invite(attendee)` with shared interface |

---

## Your Turn

Let me know if you'd like:

- Skeleton files and starter repo
- Homework or assignment version of this lesson
- A follow-up lesson on composition vs inheritance
