---
paths:
  - "**"
---

# Security Rules

- Never log sensitive information such as API keys, secrets, or personally identifiable information (PII).
- Never commit .env.
- Always use Eloquent ORM to prevent SQL injection
- Explicitly define $fillable or $guarded in your models to prevent users from modifying sensitive fields (e.g., is_admin).
- File Upload Validation: Always validate file type (MIME) and size (e.g., 'photo' => 'file|max:2048|mimes:jpg,png') to prevent remote code execution and DoS attacks.
- Encrypt Sensitive Data: Use the Crypt facade for encrypting data at rest and ensure the APP_KEY is rotated periodically for high-security apps.
- Rate limit login, reset, token and other open endpoints 
- Use starter kits to create authentication and authorization, for example: Laravel Breeze, Laravel Jetstream, etc.
- API Authentication: Use Laravel Sanctum for API token authentication or Laravel Passport for OAuth2 authentication to secure API endpoints.
- Never get request->all(), always get only the necessary data, for example: `$request->only(['name', 'email', 'password'])` to prevent mass assignment vulnerabilities.
- Avoid use raw queries like `User::whereRaw('email = "'.$request->input('email').'"')->get();`.
- Prevent path transversal in file uploads by validating file paths and using Laravel's storage system to manage file uploads securely.
- Use Laravel's built-in CSRF protection for all forms and AJAX requests to prevent cross-site request forgery attacks.
- Command injection: When using Artisan commands, ensure that any user input is properly sanitized and validated to prevent command injection vulnerabilities.

