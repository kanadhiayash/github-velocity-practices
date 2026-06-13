# Stack Overlay: Node and Express

Use this overlay after applying the universal GitHub velocity rules.

## Required CI gate

The pull request gate should include:

```text
install, lint, test, build or start check, dependency audit
```

## Required practices

- Validate required environment variables at startup.
- Review auth, session, cookie, CORS, rate limit, and logging changes.
- Never expose stack traces in production behavior.
- Treat migration scripts as release-sensitive files.
- Keep pull requests small enough for meaningful review.
- Document release and rollback impact when behavior changes.
- Run the same gates for AI-assisted changes.

## Recommended practices

- Run integration tests for public routes.
- Add dependency review for package changes.
- Use separate deploy and test jobs.
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
