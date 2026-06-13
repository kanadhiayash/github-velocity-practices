# Contributing

## Scope

Contributions should improve GitHub velocity practices, CI/CD discipline, pull request quality, release hygiene, dependency maintenance, security gates, or AI-assisted development review.

## Required contribution standards

- Keep neutral manual voice.
- Avoid first-person and third-person manifesto framing.
- Avoid private names, private project details, client data, credentials, and local paths.
- Mark claims as Fact, Assumption, Unknown, or Risk where relevant.
- Use Required, Recommended, and Optional consistently.
- Do not add unsupported benchmark, market, security, or performance claims.
- Prefer small pull requests with one clear purpose.

## Recommended pull request shape

1. Summary of the change.
2. Reason for the change.
3. Files changed.
4. Evidence used.
5. Risks introduced.
6. Review checklist completed.

## Documentation style

Use direct manual language:

```text
Required: Protect `main` with required checks.
Recommended: Keep feature branches short lived.
Optional: Add deployment environments for staging and production.
```

Avoid:

```text
A visionary system that transforms delivery forever.
```

## Local checks

Before opening a pull request, inspect for:

- em dashes
- private details
- secret-like strings
- hardcoded local paths
- unsupported claims
- inconsistent rule levels
- outdated GitHub behavior
