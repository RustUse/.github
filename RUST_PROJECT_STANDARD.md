# Rust Project Standard

This document defines the baseline standard for RustUse repositories.

## Required Baseline Files

Each RustUse repository should include, at minimum:

- `README.md`
- `LICENSE-MIT`
- `LICENSE-APACHE`
- `Cargo.toml`
- `CHANGELOG.md` for user-facing projects

Projects should use `MIT OR Apache-2.0` unless there is a documented exception.

## Recommended Workspace Structure

Use a simple layout that matches the size of the project.

For a single crate:

- `Cargo.toml`
- `src/`
- `tests/` when integration tests are needed
- `examples/` when examples add value

For a workspace:

- Workspace `Cargo.toml` at the root
- Crates under `crates/` when multiple packages are present
- Shared configuration kept at the root
- Keep internal tools or experiments clearly separated from published crates

## Required Quality Gates

RustUse repositories should pass:

```bash
cargo fmt --all --check
cargo clippy --workspace --all-targets --all-features -- -D warnings
cargo test --workspace --all-features
cargo doc --workspace --all-features --no-deps
```

## Recommended Linting

- Enable useful Clippy lints and keep warnings at zero in CI
- Prefer explicit, readable code over overly clever abstractions
- Avoid unnecessary dependencies and feature complexity

## Documentation Expectations

- Public crates should have a clear README
- Public items should be documented
- Add examples where they make the API easier to understand
- Keep doctests and examples accurate

## Testing Expectations

- Add unit tests for core behavior
- Add integration tests where component interaction matters
- Cover edge cases and numeric behavior where relevant
- Fix flaky tests before merging

## Public API Expectations

- Keep APIs focused and composable
- Prefer clear naming over short naming
- Avoid surprising implicit behavior
- Treat breaking changes deliberately and document them clearly
