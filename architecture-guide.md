# Architecture Guide

## Architecture Style

We use:
**Modular Architecture** (Simple Clean Structure)

---

## Layer Responsibilities

### Controller
- Handles HTTP requests
- Validates input
- Calls service
- Returns response

---

### Service
- Contains business logic
- Coordinates between modules
- Calls repositories

---

### Repository
- Handles database queries
- No business logic

---

## Feature Development Rules

Every feature must:

1. Have its own module.
2. Include:
   - **controller**
   - **service**
   - **dto**
3. Follow naming conventions.
4. Follow the project structure.

---

## Data Flow

```
Request → Controller → Service → Repository → Database
Response ← Controller ← Service
```

---

## Dependency Rules

- **Controller → Service** ✅
- **Service → Repository** ✅
- **Controller → Repository** ❌
- **Repository → Service** ❌

---

## Business Logic Rules

- MUST be inside **services**.
- MUST NOT be inside **controllers**.
- MUST NOT be inside **repositories**.

---

## Reusability

Before creating new logic:
- Check `/shared/`.
- Check existing **services**.

---

## Scaling Rules

- Split large modules into sub-modules.
- Extract shared logic early.
- Avoid tight coupling.