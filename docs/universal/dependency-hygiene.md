# Dependency Hygiene

Dependency hygiene keeps supply-chain risk visible and manageable.

## Required practices

- Commit lockfiles for package managers that use them.
- Review dependency changes in pull requests.
- Separate dependency-only pull requests from feature work when possible.
- Treat new runtime dependencies as architecture decisions.
- Remove unused dependencies.
- Do not ignore known high-severity vulnerabilities without a documented reason.

## Recommended practices

- Enable Dependabot alerts where available.
- Enable Dependabot security updates where available.
- Configure Dependabot version updates for active package ecosystems.
- Group safe patch updates when noise becomes high.
- Review GitHub Actions dependency updates.
- Add dependency review checks for higher-risk repositories.

## Optional practices

- Maintain an allowlist for high-risk dependency types.
- Use software bill of materials generation for release artifacts.
- Use private registries for internal packages.
- Use license checks when redistribution matters.

## Dependency review template

```text
Package:
Change type:
Reason:
Security impact:
License impact:
Runtime impact:
Alternative considered:
Rollback plan:
Decision:
```

## Risk triggers

Open a risk record when:

- a package has low maintenance activity
- a package runs install scripts
- a package handles auth, crypto, payments, files, network calls, or secrets
- a dependency update requires code migration
- a vulnerability is accepted temporarily
