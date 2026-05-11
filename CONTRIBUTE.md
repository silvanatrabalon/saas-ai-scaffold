# Contributing
This project follows a spec-driven workflow with OpenSpec, AI chat, agents, and reusable skills. The goal is simple: every feature should go from backlog item to reviewed proposal, then to implementation, then to archive, and finally to a documented commit.

## Core rule

Do not jump from a raw backlog bullet directly into `/opsx:propose` with the entire bullet pasted as-is. First, turn the backlog item into a clearer requirement with AI chat and the right agent review. That extra step avoids vague proposals and usually produces better specs, better tasks, and better tests.

## Recommended flow

<details>
<summary><strong>Step 1. Read the backlog item</strong></summary>

Start with `BACKLOG.md` and read the feature you want to work on.

If the item is short or incomplete, expand it before proposing it by doing the requirement refinement step. For example, if the backlog says:

```md
Protected Routes System:  Route guards, role-based access control, redirect logic, unauthorized handling.
```

do not copy that block directly into `/opsx:propose`. First, clarify what the feature should actually do using the refinement step.

</details>

<details>
<summary><strong>Step 2. Refine the requirement with agents</strong></summary>

Use chat as a requirement-cleanup step. Bring in the **right agent** before proposing the change, depending on the feature type.

Ask the AI (replace the feature, context, and agents):
```text
I want to work on the backlog item: <FEATURE_NAME>.

Context:
<paste the short description from the backlog and any relevant notes from docs/architecture>

Goal:
Use the agent < choose one: #architect.agent.md | #backend-developer.agent.md | #frontend-developer.agent.md > to review the requirement and help me turn it into a clear scope for OpenSpec.

I want you to:
1. Identify ambiguities or gaps in the requirement.
2. Propose a concrete and ordered solution.
3. Indicate if unit tests should be created or updated.
4. Propose a refined version of the requirement.
5. Ask me questions if we need to take some decisions.

Do not implement or apply code changes yet. Do no create changes in the openspec folder, if there are suggestion, must be made on the Backlog.md file.
```

</details>

<details>
<summary><strong>Step 3. Create the proposal with OpenSpec</strong></summary>

Once the requirement is clear, create the proposal using OpenSpec.
Ask the IA:
```text
/opsx:propose <New description generated for the backlog item refined>
```

</details>

<details>
<summary><strong>Step 4. Review the generated proposal before applying anything</strong></summary>

Read the proposal, design, and tasks in the change folder. If something is unclear, go back to chat and ask the AI for corrections.

</details>

<details>
<summary><strong>Step 5. Apply the change only when you are happy with the proposal</strong></summary>

When the proposal is ready, apply it with OpenSpec.
Ask the AI (replace change-name):
```text
/opsx:apply <change-name> The implementation must finish with all tests passing. If tests fail, fix them before considering the change done.
```

</details>

<details>
<summary><strong>Step 6. Review the implementation</strong></summary>

Test the feature manually or by running unit tests. If something is not working, go back to chat and ask the AI to fix it.

</details>

<details>
<summary><strong>Step 7. Commit the changes done</strong></summary>

Ask the AI:
```text
Check that all spec tasks are marked as done. Use the conventional-commit skill to create and commit the change, then update BACKLOG.md with the done status and commit hash.
```

</details>

<details>
<summary><strong>Step 8. Archive only when the change is finished and stable</strong></summary>

Once implementation is complete and you are confident the feature works, archive the change.
Ask the AI (replace change-name):
```text
/opsx:archive <change-name>
```

</details>

<details>
<summary><strong>Step 9. Commit the archive</strong></summary>

Ask the AI:
```text
Use the conventional-commit skill to commit this change.
```

</details>
---
The backlog entry should always reflect the real state of the feature and the commit that closed it.
