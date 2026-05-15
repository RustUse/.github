# Releasing

RustUse projects should keep releases simple, repeatable, and easy to audit.

## Release Checklist

- Update the changelog for user-facing changes
- Confirm the version bump is correct
- Ensure CI is passing on `main`
- Run `cargo fmt --all --check`
- Run `cargo clippy --workspace --all-targets --all-features -- -D warnings`
- Run `cargo test --workspace --all-features`
- Run `cargo doc --workspace --all-features --no-deps`
- Run `cargo publish --dry-run`
- Create and push a tag in the format `v0.1.0`
- Create a GitHub Release with concise release notes

## crates.io Publishing

Before publishing:

- Verify crate metadata is complete
- Confirm included files are correct
- Check feature flags and default features carefully
- Make sure the changelog and README reflect the released behavior

Publish from a clean, reviewed state. If publishing multiple crates, release in dependency order.
