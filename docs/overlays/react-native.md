# Stack Overlay: React Native

Use this overlay after applying the universal GitHub velocity rules.

## Required CI gate

The pull request gate should include:

```text
install, TypeScript check, lint, unit tests, Expo or native build check
```

## Required practices

- Keep `.env` ignored and provide `.env.example`.
- Separate Expo, Android, and iOS build concerns.
- Review native permission changes.
- Review OTA update policy when used.
- Keep pull requests small enough for meaningful review.
- Document release and rollback impact when behavior changes.
- Run the same gates for AI-assisted changes.

## Recommended practices

- Run typecheck before merge.
- Use EAS or documented local build steps for release candidates.
- Record app config changes in pull requests.
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
