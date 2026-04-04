---
paths:
  - "src/**"
---

# Development Rules

- Use Clean Code principles
- Use SOLID principles
- Write modular, reusable code
- Keep one level identiation per function, avoid nested code use early returns
- Use descriptive variable and function names
- Should not use comments to explain code
- Create functions with camelCase pattern
- Create variables with camelCase pattern
- Create classes with PascalCase pattern
- Destructure Objects & Arrays: Extract properties directly into variables `const { name, age } = user;`.
- Use named parameters for functions with multiple arguments: `function createDeck({ name, arena, cards }) { ... }`.

# Performance Rules

- Avoid unnecessary computations: Cache results of expensive operations when possible.
- Use efficient data structures: Choose the right data structure for the task (e.g., Map for key-value pairs, Set for unique values).
- If the loop can be break early, use a for loop instead of forEach or map.
- Avoid deep nesting: Refactor code to reduce nesting levels, which can improve readability and performance.
- Use asynchronous programming: For I/O operations, use async/await or Promises to avoid blocking the main thread.

