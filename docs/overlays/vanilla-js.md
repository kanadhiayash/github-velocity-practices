# Stack Overlay: Vanilla JavaScript

Use this overlay after applying the universal GitHub velocity rules.

## Required CI gate

The pull request gate should include:

```text
HTML validation where available, lint, unit tests if configured, static build check
```

## Required practices

- Keep examples free of real API keys.
- Review DOM injection and unsafe HTML changes.
- Validate forms client-side and server-side when a backend exists.
- Do not treat static hosting as a security boundary.
- Keep pull requests small enough for meaningful review.
- Document release and rollback impact when behavior changes.
- Run the same gates for AI-assisted changes.

## Recommended practices

- Add accessibility checks for interactive UI.
- Use lightweight tests for critical calculations.
- Document deployment target and rollback path.
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
