---
paths:
  - "app/**"
  - "database/**"
  - "test/**"
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

## Eloquent Best Practices:

- Eager loading to prevent N+1

```php
// ✅ Good: Eager loading to prevent N+1
$users = User::with(['posts', 'profile'])->get();

// ❌ Bad: N+1 query problem
$users = User::all();
foreach ($users as $user) {
    echo $user->posts->count(); // Query per user!
}
```

- Constructor Property Promotion

```php
// ✅ PHP 8+ concise
class User
{
    public function __construct(
        public readonly int $id,
        public string $name,
        public string $email,
        private ?string $password = null,
    ) {}
}

// ❌ Old verbose style
class User
{
    public int $id;
    public string $name;

    public function __construct(int $id, string $name)
    {
        $this->id = $id;
        $this->name = $name;
    }
}
```

- Named Arguments:

```php
// Clear intent
$user = new User(
    id: 1,
    name: 'John',
    email: 'john@example.com',
);

// Skip optional params
sendEmail(
    to: $user->email,
    subject: 'Welcome',
    // body uses default
);
```
