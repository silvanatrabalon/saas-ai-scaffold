# Contributing

This repository uses a spec-driven workflow with OpenSpec, agents, and skills.

## Workflow

1. Pick next feature from BACKLOG.md
2. Run `/opsx:propose <change-name>`
3. Review output and refine in Copilot chat
4. Optionally request agent review (architect/backend/frontend/qa)
5. Run `/opsx:apply <change-name>`
6. Commit with conventional-commit skill
7. Update BACKLOG.md status with change name and commit hash

Short flow:

`BACKLOG.md -> /opsx:propose -> review -> /opsx:apply -> commit -> update BACKLOG.md`

## OpenSpec Commands

- `/opsx:propose` Create full planning artifacts
- `/opsx:explore` Clarify scope and constraints before proposing
- `/opsx:apply` Implement pending tasks from a change
- `/opsx:archive` Archive completed changes

## Agent Usage (Optional)

- `@architect` Architecture/dependency review
- `@backend-developer` Data/RLS/integration review
- `@frontend-developer` UI/component review
- `@qa-test-engineer` Tests, risk, and edge-case review

## Commit Format

Use the `conventional-commit` skill for consistent commit messages.

Examples:

- `feat(auth): add Google OAuth login flow`
- `fix(booking): prevent duplicate slot reservation`
- `docs(workflow): document backlog-driven process`

## Backlog Update Rule

After each completed feature, update the corresponding item in BACKLOG.md:

- From: `- [ ]`
- To: `- [x] `change-name` (abc1234)`

This keeps traceability between backlog item, OpenSpec change, and git history.
