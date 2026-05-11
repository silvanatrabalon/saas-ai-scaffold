# Backlog Template

Spec-driven feature backlog ordered by dependency.

Use this file as the single source of truth for implementation order and tracking.

## How to Use

- Keep features in dependency order (foundational first).
- Each feature has a unique number for references in chat/PRs.
- After implementation, replace placeholder status with OpenSpec change and commit hash.

Status format:

- Pending: `- [ ]`
- Completed: `- [x] `change-name` (abc1234)`

---

## Phase 1: Foundation

### 1. Project Bootstrap
Description: Initialize project scaffold, base tooling, and environment validation.
- [ ]

### 2. Auth Setup
Description: Configure authentication provider and session handling.
- [ ]

### 3. Role System
Description: Define base roles and authorization model.
- [ ]

### 4. App Shell
Description: Create navigation, layout shell, and basic route structure.
- [ ]

### 5. Protected Routes
Description: Enforce route access by role/auth state.
- [ ]

## Phase 2: Core Domain

### 6. Domain Model Setup
Description: Define core business entities and relationships.
- [ ]

### 7. Core CRUD Flows
Description: Build create/read/update/delete flows for primary entities.
- [ ]

### 8. Core Validation Rules
Description: Add server/client validation and edge-case handling.
- [ ]

### 9. Permissions Hardening
Description: Apply RLS/policy rules to enforce data boundaries.
- [ ]

## Phase 3: Operations

### 10. Notifications
Description: Add transactional notifications and templates.
- [ ]

### 11. Dashboard
Description: Build basic operational metrics and overview panels.
- [ ]

### 12. Settings
Description: Add configurable business/system settings.
- [ ]

## Phase 4: Quality and Deployment

### 13. QA Edge Cases
Description: Validate concurrency, timezones, and failure modes.
- [ ]

### 14. Security Review
Description: Verify authz, data isolation, and abuse protections.
- [ ]

### 15. Deployment Pipeline
Description: Finalize environment management and release workflow.
- [ ]

---

## Mapping Example

### 1. Project Bootstrap
Description: Initialize project scaffold, base tooling, and environment validation.
- [x] `project-bootstrap` (9d01ca2)
