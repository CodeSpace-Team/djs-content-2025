# Lesson Plan — Practical OOP in JavaScript _without_ Classes

_(Built around the Todo-app refactor shown in the video)_

---

## 1. Why This Lesson?

Most people meet “OOP” through **classes** and theory first, then fight their way toward practical value.  
Today we’ll **reverse that**: start with code you already understand, feel its pain points, and _then_ reach for object-oriented ideas—implemented with **object literals & factory functions**, not classes.

---

## 2. Learning Outcomes

By the end you should be able to:

| #   | You will be able to …                                                                                     |
| --- | --------------------------------------------------------------------------------------------------------- |
| 1   | Spot the limits of a purely procedural DOM-driven approach.                                               |
| 2   | Apply **@ts-check** and TypeScript utility types (`Pick`, `Partial`) in plain JS for early bug detection. |
| 3   | Refactor code using **Single Responsibility** & **Dependency Inversion** principles.                      |
| 4   | Build lightweight OOP structures with factory functions & object literals.                                |
| 5   | Judge when an abstraction _clarifies_ vs. _obscures_ your codebase.                                       |

---

## 3. Prerequisites

- Comfortable with vanilla JavaScript & the DOM
- VS Code (or another editor with TypeScript IntelliSense)
- A starter “procedural” Todo app (HTML, CSS, and a single `index.js`)

---

## 4. Warm-up — The Procedural Baseline

### `index.html` Excerpt

```html
<ul id="list"></ul>
<input id="newTitle" />
<button id="addBtn">Add</button>
```

### `index.js` (Procedural Version)

```js
/** @type {{id:number,title:string,done:boolean}[]} */
const tasks = [];

document.getElementById("addBtn").addEventListener("click", () => {
  const title = /** @type {HTMLInputElement} */ (
    document.getElementById("newTitle")
  ).value;
  const li = document.createElement("li");
  li.textContent = title;
  document.getElementById("list").appendChild(li);
  tasks.push({ id: Date.now(), title, done: false });
});
```

### Discussion:

- Where can bugs creep in?
- What happens to `tasks` if we manipulate the DOM directly elsewhere?

## 5. Add Safety Nets with Static Type Checks

1. Add `// @ts-check` to every JS file
2. Use assertive DOM helpers

```js
/** @template {keyof HTMLElementTagNameMap} T */
function getEl(tag, id) {
  const el = document.getElementById(id);
  if (!el) throw new Error(`#${id} not found`);
  return /** @type {HTMLElementTagNameMap[T]} */ (el);
}

const $list = getEl("ul", "list");
const $newTitle = getEl("input", "newTitle");
const $addButton = getEl("button", "addBtn");
```

_Try it:_ mistype an ID and watch VS Code scream before the browser does.

## 6. Refactor with SOLID Principles

### 6.1 Single Responsibility Principle (SRP)

Split concerns into clear functions:

| Concern               | Function                     |
| --------------------- | ---------------------------- |
| Render one task       | `renderTask(task)`           |
| Persist / mutate data | `taskRepository.add(task)`   |
| Wire UI events        | `setupAddTaskForm(ui, repo)` |

## 6.2 Dependency Inversion Principle (DIP)

Design from the caller’s perspective:

```js
// good
repo.add({ title: "Milk" }); // readable

// avoid
repo.save({ todo: "Milk" }, true); // boolean flags muddy intent
```

## 7. Introduce Factory Functions — Lightweight OOP

```js
function createTask({ id = Date.now(), title, done = false }) {
  return {
    id,
    title,
    done,
    toggle() {
      this.done = !this.done;
    },
    update(patch) {
      Object.assign(this, patch);
    },
  };
}

function createTaskRepo(initial = []) {
  /** @type {ReturnType<typeof createTask>[]} */
  const list = [...initial];

  return {
    all() {
      return [...list];
    },
    add(data) {
      list.push(createTask(data));
    },
    find(id) {
      return list.find((t) => t.id === id);
    },
  };
}
```

**Key Point:** Encapsulation & behavior without class Task {}.

## 8. TypeScript Utility Types for Safe Updates

```js
/** @typedef {ReturnType<typeof createTask>} Task */
/** @typedef {Pick<Task,'id'> & Partial<Omit<Task,'id'>>} TaskPatch */

function safeUpdate(repo, patch /** @type {TaskPatch} */) {
  const t = repo.find(patch.id);
  if (t) t.update(patch);
}
```

Allows safe, flexible updates with static guarantees.

## 9. Hands-On Lab (30–45 min)

| Step | Activity                                                                     |
| ---- | ---------------------------------------------------------------------------- |
| 1    | Clone / fork the starter repo                                                |
| 2    | Enable` @ts-check`, replace raw `getElementById` with `getEl`                |
| 3    | Split the `addBtn` click handler’s responsibilities                          |
| 4    | Implement `createTask` & `createTaskRepo`                                    |
| 5    | Replace DOM manipulation with `renderTask(`) logic                           |
| 6    | Use `safeUpdate()` to implement task editing                                 |
| 7    | **Stretch Goal:** Persist tasks via `localStorage` using a DIP-style factory |

## 10. Debrief & Discussion

- When did the refactor feel clearer vs. heavier?
- Did SRP ever feel “too many files”? Where’s the sweet spot?
- How might **classes** help or hinder here?

## 11. Further Reading / Next Steps

- Robert C. Martin, Clean Code
- Eric Elliott’s blog: “You Might Not Need Classes”
- TypeScript Utility Types
- Refactor another UI component (e.g. stopwatch, tabbed view) from procedural → factory-function OOP
