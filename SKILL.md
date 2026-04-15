---
name: jo-blueprint
description: Structured coding workflow for agent sessions. Use BEFORE writing any code — when building new features, apps, or systems. Forces agents to clarify, plan, and test before implementing. Triggers on: "build me", "create a", "make a", "I need a website", "set up a system", "develop a", "code a", or any request to build software from scratch or add significant new functionality.
---

# Blueprint — Structured Build Workflow

Stop. Don't write code yet. Follow this workflow every time.

## The Rule

**No implementation until you have a signed-off spec and plan.** This applies to everything — a full website, a single function, a small script. The smaller it seems, the more likely you'll waste time on wrong assumptions.

---

## Phase 1 — Clarify

Ask questions **one at a time** until you understand:

1. What problem does this actually solve?
2. Who uses it and how?
3. What does "done" look like? (Success criteria)
4. What already exists that this connects to?
5. What are the hard constraints? (Tech stack, deadline, existing codebase)

**Hard gate:** Do NOT propose a design, scaffold anything, or write a line of code until you've asked at least 3 clarifying questions and confirmed understanding.

---

## Phase 2 — Design

Present 2–3 approaches with trade-offs. Include your recommendation and why.

```
Option A: [Name]
- What it does
- Trade-offs
- Best when: [context]

Option B: [Name]
- What it does
- Trade-offs
- Best when: [context]

My recommendation: [Option X] because [reason]
```

Get explicit approval before moving to Phase 3.

Save design doc to: `docs/blueprint/specs/YYYY-MM-DD-<name>-spec.md`

---

## Phase 3 — Plan

Break work into tasks small enough for one focused session (aim for 2–5 min per task).

Each task must include:
- **What:** Exact action
- **Where:** File paths involved
- **How:** Specific implementation notes
- **Test:** How to verify it worked

Enforce these defaults:
- **TDD:** Write the failing test first, then the code to pass it
- **YAGNI:** Don't build what wasn't asked for
- **DRY:** No copy-paste — abstract shared logic
- **Commit often:** One commit per completed task

Save plan to: `docs/blueprint/plans/YYYY-MM-DD-<name>-plan.md`

---

## Phase 4 — Execute

Work through the plan task by task:

1. Read the task spec
2. Write the test (RED)
3. Write the minimum code to pass (GREEN)
4. Refactor if needed (REFACTOR)
5. Commit
6. Mark task complete, move to next

If a task reveals something the plan didn't account for — **stop and surface it** before continuing. Don't silently improvise.

---

## Phase 5 — Review

After all tasks complete:

- Run the full test suite
- Verify success criteria from Phase 1
- List anything deferred, skipped, or left TODO
- Ask: "Does this actually solve the original problem?"

---

## Quick Reference

| Phase | Gate | Output |
|---|---|---|
| Clarify | 3+ questions answered | Shared understanding |
| Design | User approves approach | Spec doc saved |
| Plan | User approves plan | Plan doc saved |
| Execute | Task-by-task with tests | Working code, commits |
| Review | All tests pass | Sign-off or issue list |

See `references/tdd-patterns.md` for test-driven development patterns.
