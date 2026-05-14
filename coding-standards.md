# Coding Standards

## 1. Naming Conventions

- **Variables:** camelCase
- **Functions:** camelCase
- **Classes:** PascalCase
- **Interfaces/Types:** PascalCase
- **Files:** kebab-case
- **Constants:** UPPER_SNAKE_CASE

---

## 2. General Rules

- Code must be readable before being clever.
- Avoid unnecessary abstractions.
- Keep functions small and focused.
- Prefer explicit over implicit.

---

## 3. File Organization

Each module should contain:

- **controller**
- **service**
- **repository** (if needed)
- **dto**
- **types/interfaces**

---

## 4. Controllers

- Controllers must **NOT** contain business logic.
- Controllers should only:
  - Handle request.
  - Validate input.
  - Call the respective service.
  - Return response.

---

## 5. Services

- Contain all business logic.
- Must be reusable.
- Should not depend on controllers.

---

## 6. Repositories

- Repositories handle **database operations only**.
- No business logic allowed.

---

## 7. DTOs (Data Transfer Objects)

- Every API must use **DTOs**.
- Validate all incoming data.
- **Never** trust raw input.

---

## 8. Error Handling

- Use a centralized error handler.
- Do not return raw errors to clients.
- Adhere to the following standard error format:

  ```json
  {
    "success": false,
    "message": "Error message",
    "code": "ERROR_CODE"
  }
  ```

---

## 9. Logging

- Log all critical operations.
- Log errors with context.
- Avoid logging sensitive data.

---

## 10. Code Reuse

- Do not duplicate logic.
- Always check the shared folder first.
- Extract reusable utilities.

---

## 11. Comments

- Write comments only when necessary.
- Explain **WHY**, not **WHAT**.

---

## 12. Formatting

- Use consistent linting rules.
- Use Prettier (or an equivalent tool).
- Do not include unused imports.