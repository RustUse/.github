# Contributing

RustUse welcomes contributions across its `use-*` sets, supporting crates,
documentation, and tooling.

## Open an issue

- Use GitHub Issues for bugs, feature requests, documentation issues, and crate
  proposals.
- Open issues in the affected repository when possible.
- Keep issue reports concrete and include reproduction details, expected
  behavior, and actual behavior when relevant.

## Propose a new crate

- Open a crate proposal issue with the proposed crate name, parent set, problem
  statement, proposed primitives, and dependency considerations.
- Favor crates that are small, composable, and clearly scoped.
- Avoid proposals that depend on broad framework-style abstractions.

## Open a pull request

- Keep changes focused and reviewable.
- Link the related issue when one exists.
- Update documentation and examples when public behavior changes.
- Follow any repository-specific contribution guidance when present.

## Expected Rust checks

```sh
cargo fmt --all -- --check
cargo clippy --workspace --all-targets --all-features -- -D warnings
cargo test --workspace --all-features
cargo doc --workspace --all-features --no-deps
```

## API expectations

RustUse crates should stay:

- small
- documented
- tested
- composable
- minimal in dependencies

## Project conventions

- Rust edition: `2024`
- License: `MIT OR Apache-2.0`
- Prefer practical primitives over framework design.
- Avoid broad framework-style dependencies unless they are clearly justified.
