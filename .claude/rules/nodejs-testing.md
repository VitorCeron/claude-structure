---
paths:
  - "src/**"
---

# Testing Rules

- Use pattern AAA (Arrange, Act, Assert) for structuring tests to improve readability and maintainability.
- Write tests to guarantee that business rules are correctly implemented and that edge cases are handled gracefully.
- Use test description in English.
- Use mocks for external services.
- Use test data builders to create complex test data.
- Avoid testing implementation details; focus on testing the behavior of the code.
- Use code coverage tools to ensure that critical paths are tested, but do not aim for 100% coverage at the expense of meaningful tests.
- Run tests in isolation to ensure that they do not depend on the state of other tests or external systems.
- Use continuous integration (CI) to run tests automatically on every commit to catch issues early in the development process.