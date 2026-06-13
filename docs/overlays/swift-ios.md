# Stack Overlay: Swift and iOS

Use this overlay after applying the universal GitHub velocity rules.

## Required CI gate

The pull request gate should include:

```text
xcodebuild test, SwiftLint if configured, dependency resolution, simulator build
```

## Required practices

- Protect signing files and provisioning profiles.
- Never commit `GoogleService-Info.plist` unless the project intentionally uses a public sample file.
- Separate Debug, Staging, and Release schemes where project risk requires it.
- Document TestFlight or App Store release steps when used.
- Keep pull requests small enough for meaningful review.
- Document release and rollback impact when behavior changes.
- Run the same gates for AI-assisted changes.

## Recommended practices

- Run unit tests for view models, validators, and services.
- Archive builds through a release workflow only after signing risk is reviewed.
- Keep bundle identifiers and environment files documented.
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
