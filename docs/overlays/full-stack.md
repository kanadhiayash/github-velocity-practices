# Stack Overlay: Full-stack products

Use this overlay after applying the universal GitHub velocity rules.

## Required CI gate

The pull request gate should include:

```text
frontend checks, backend checks, integration tests, migration review, deployment dry run
```

## Required practices

- Separate frontend and backend environment variables.
- Review API contracts when either side changes.
- Review migrations before release.
- Review auth and data access across the full path.
- Keep pull requests small enough for meaningful review.
- Document release and rollback impact when behavior changes.
- Run the same gates for AI-assisted changes.

## Recommended practices

- Use path-aware workflows where appropriate.
- Use staging before production for high-risk changes.
- Add smoke tests after deployment.
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
