# Commit Convention

RustUse repositories use Conventional Commits.

## Format

```text
type(scope): summary
```

## Supported Types

- `feat`
- `fix`
- `docs`
- `test`
- `refactor`
- `perf`
- `chore`
- `ci`
- `build`
- `release`

## Examples

- `feat(core): add checked angle conversion`
- `fix(cli): return nonzero exit code on invalid input`
- `docs(readme): add quickstart example`
- `chore(ci): add cargo deny check`

## Guidance

- Use the imperative mood
- Keep summaries lowercase unless using proper nouns
- Do not end the summary with a period
- Use a scope when it improves clarity
- Keep the subject concise and specific

## Breaking Changes

Use a `BREAKING CHANGE:` footer when a commit introduces a breaking change.

Example:

```text
feat(api): simplify matrix constructor

BREAKING CHANGE: remove the unchecked constructor overload
```
