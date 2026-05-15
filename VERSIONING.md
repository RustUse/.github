# Versioning

RustUse projects use Semantic Versioning.

## General Rules

Given a version `MAJOR.MINOR.PATCH`:

- `PATCH` releases contain backward-compatible fixes only
- `MINOR` releases add backward-compatible functionality
- `MAJOR` releases contain breaking changes

## Pre-1.0 Policy

Before `1.0.0`, RustUse uses the following policy:

- `PATCH` releases must not contain breaking changes
- `MINOR` releases may contain breaking changes
- Breaking changes should still be documented clearly and intentionally

## Breaking Change Expectations

A change is considered breaking when it can require user code, configuration, behavior assumptions, or documented workflows to change.

When making a breaking change:

- Document it clearly in the changelog and release notes
- Call it out in pull requests
- Use the Conventional Commits `BREAKING CHANGE:` footer when appropriate
