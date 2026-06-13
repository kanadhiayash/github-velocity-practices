# Stack Overlay: Jetpack Compose

Use this overlay after applying the universal GitHub velocity rules.

## Required CI gate

The pull request gate should include:

```text
Gradle test, lint, assemble debug, dependency resolution
```

## Required practices

- Keep signing files out of source control.
- Review manifest permission changes.
- Document build variants and release signing.
- Review networking and storage permission changes.
- Keep pull requests small enough for meaningful review.
- Document release and rollback impact when behavior changes.
- Run the same gates for AI-assisted changes.

## Recommended practices

- Run unit tests for view models and repositories.
- Run Compose UI tests for critical flows where available.
- Use release checklist before APK or Play track distribution.
- Keep dependency updates separate from feature work where possible.
- Add stack-specific release notes before public release.

## Optional practices

- Add code owner review for critical paths.
- Add deployment environments for staging and production.
- Add artifact signing where distribution risk justifies it.
- Add scheduled dependency review.

## Required architecture and operations decisions

Record these decisions before the first public release:

- branch flow
- required status checks
- dependency update policy
- release path
- rollback path
- secrets handling
- AI-assisted development policy

## Review checklist

```text
Fact:
Assumption:
Unknown:
Risk:
Decision:
Next action:
```
