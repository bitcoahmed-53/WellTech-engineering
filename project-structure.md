# Project Structure

## Root Structure

```
src/
modules/
shared/
core/
infrastructure/
```

---

## Modules

Each feature is a module:

```
modules/
  user/
    user.controller.ts
    user.service.ts
    user.repository.ts
    user.dto.ts
    user.types.ts
```

---

## Shared

Reusable code across the app:

```
shared/
  utils/
  constants/
  helpers/
  validators/
```

---

## Core

Global system logic:

```
core/
  config/
  database/
  middleware/
  errors/
```

---

## Infrastructure

External integrations:

```
infrastructure/
  email/
  payment/
  external-apis/
```

---

## Rules

- Every feature **MUST** be inside a module.
- No loose files in the root directory.
- Shared logic should be placed in `/shared`.
- No cross-module direct access (use services instead).