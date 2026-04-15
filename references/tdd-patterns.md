# TDD Patterns for Blueprint Skill

## The RED-GREEN-REFACTOR Cycle

Every feature follows this exact cycle. No exceptions.

```
1. RED   — Write a test that describes desired behavior. Run it. Watch it FAIL.
2. GREEN — Write the minimum code to make it pass. Run it. Watch it PASS.
3. REFACTOR — Clean up. No new behavior. Tests still pass.
4. COMMIT — One commit per cycle completion.
```

If you write code before a failing test exists, delete the code and start over.

---

## Test Structure (Universal)

```
describe("what you're testing") {
  context("given some condition") {
    it("does the expected thing") {
      // Arrange — set up state
      // Act — call the thing
      // Assert — verify result
    }
  }
}
```

---

## What Makes a Good Test

- Tests ONE thing per test case
- Has a clear, descriptive name that reads like a sentence
- Doesn't test implementation details — tests behavior
- Fast (no real network calls, no real DB writes in unit tests)
- Independent — doesn't depend on other tests running first

---

## What to Test First (Priority Order)

1. **Happy path** — does it work when everything is correct?
2. **Edge cases** — empty input, zero, null, max values
3. **Error cases** — what happens when it fails gracefully?
4. **Integration** — does it work end-to-end?

---

## Common Test Types by Layer

### API / Backend
- Unit test each function/method
- Integration test each route/endpoint
- Test auth, validation, error responses

### Frontend / UI
- Component renders correctly
- User interactions trigger correct state changes
- Forms validate and submit properly

### Database
- Use test DB or in-memory DB — never production
- Seed data, run operation, assert result, tear down

---

## When Tests Feel Hard to Write

Hard-to-test code = poorly designed code. If writing the test is painful:
- The function probably does too much — split it
- There are probably hidden dependencies — inject them
- The module is probably tightly coupled — decouple it

The test difficulty is telling you something. Listen to it.
