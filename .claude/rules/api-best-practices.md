---
paths:
  - "**"
---

### REST Design (`/api-patterns rest`)

- Resource Naming:
```
GET    /users           # List users
GET    /users/:id       # Get single user
POST   /users           # Create user
PUT    /users/:id       # Replace user
PATCH  /users/:id       # Update user partially
DELETE /users/:id       # Delete user

# Nested resources
GET    /users/:id/posts # User's posts
POST   /users/:id/posts # Create post for user

# Filtering, sorting, pagination
GET    /users?role=admin&sort=-createdAt&page=2&limit=20 // option 1
GET    /users?filter[role]=admin&sort=-createdAt&page=2&limit=20 // option 2
```
