---
paths:
  - "src/**"
---

# Security Rules

- Never log sensitive information such as API keys, secrets, or personally identifiable information (PII).
- Validate and sanitize all inputs to prevent injection attacks (e.g., SQL injection, command injection).
- Use HTTPS for all external API calls to ensure data is encrypted in transit.
- Implement rate limiting on API endpoints to prevent abuse and denial-of-service (DoS) attacks.
- Use environment variables to store sensitive configuration values, and never hard-code them in the source code.
- Implement proper error handling to avoid exposing stack traces or sensitive information in error responses.
- Use secure headers (e.g., Content-Security-Policy, X-Content-Type-Options) to protect against common web vulnerabilities.
- Ensure that any third-party libraries or APIs used are reputable and maintained, and review their security practices.
- Avoid eval(): Never use eval() as it poses severe security risks and prevents engine optimizations.
