---
paths:
  - "test/**"
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
- Use traits for testing common behaviors across multiple test classes to reduce code duplication and improve maintainability, like authentication.
- Keep headers variable enabled to use in all tests, for example: `$this->headers = ['Authorization' => 'Bearer ' . $this->token];` in setUp method.
- Use testdox to document the test method.
- Use factories to create test data, for example: `User::factory()->create();`.
- Mock only external services, for example: `Http::fake();` to mock HTTP requests.

## Unit tests

- Use unit tests to test individual functions or methods in isolation, ensuring that they work as expected under various conditions.
- Focus on testing the smallest units of code, such as individual functions or methods, to ensure that they behave correctly in isolation from the rest of the application.
- Use in utils methods for example.

## Feature tests

- Should use to test complete endpoint.
- Validate input and response data.
- Validate the whole feature, for example: create user, login, etc.
- Validate json structure in response, for example: `->assertJsonStructure(['data' => ['id', 'name', 'email']])`.
