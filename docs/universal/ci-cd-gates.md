# CI/CD Gates

CI/CD gates provide fast, repeatable feedback before merge and release.

## Required baseline

Every serious repository should define at least one workflow that runs on pull requests to `main`.

Required checks depend on stack, but the gate should usually include:

- install or dependency restore
- lint or static checks
- tests where available
- build where applicable
- security or dependency check where applicable
- documentation check for documentation repositories

## Required workflow qualities

- Use explicit triggers.
- Set minimal permissions.
- Fail fast for invalid configuration.
- Keep secrets out of logs.
- Avoid unnecessary write permissions.
- Use caching only when cache poisoning risk is understood.
- Keep job names stable when used as required checks.

## Recommended workflow shape

```yaml
name: CI

on:
  pull_request:
    branches: [main]
  push:
    branches: [main]

permissions:
  contents: read

jobs:
  quality:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: echo "Add stack-specific checks here"
```

## Recommended gate levels

| Gate level | Checks |
|---|---|
| Local gate | format, lint, unit tests. |
| Pull request gate | install, lint, tests, build, security check. |
| Release gate | full test pass, release notes, artifact check, rollback plan. |
| Production gate | environment approval, migration check, monitoring note. |

## Optional practices

- Use workflow concurrency to cancel stale runs.
- Split slow jobs from fast required jobs.
- Use matrix builds for multi-version support.
- Use deployment environments for staging and production.
- Add smoke tests after deployment.

## CI failure handling

Required:

- Do not merge around failing required checks.
- Identify whether the failure is product code, test code, infrastructure, or flaky behavior.
- Record repeated flaky failures as risks.
- Fix or quarantine flaky tests with owner and deadline.
