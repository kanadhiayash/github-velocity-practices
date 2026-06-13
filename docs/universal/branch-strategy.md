# Branch Strategy

Branch strategy controls how change enters the repository.

## Required model

Use a simple GitHub Flow default:

```text
main                 stable, protected, release-ready
feat/<short-name>    feature work
fix/<short-name>     bug fixes
docs/<short-name>    documentation changes
chore/<short-name>   tooling, maintenance, dependencies
security/<short-name> security-sensitive changes
```

## Required practices

- Branch from `main`.
- Keep one mission per branch.
- Keep branches short lived.
- Open a pull request before merging.
- Rebase or update branches before review when drift is high.
- Delete merged branches.
- Never use `main` as an experiment branch.

## Recommended practices

- Keep feature branches under three working days where possible.
- Use draft pull requests for early design review.
- Use `security/` branch prefix for sensitive fixes.
- Use `release/` branches only when release stabilization requires them.
- Avoid long-lived `dev` unless the team has a clear reason.

## Optional practices

- Use stacked pull requests for large work split into reviewable steps.
- Use branch naming enforcement in repository rulesets.
- Use protected release branches for mobile app store submissions.

## Branch decision record

Record a branch decision when a repository uses a flow beyond simple GitHub Flow:

```text
Decision:
Reason:
Release risk:
Rollback impact:
Maintenance cost:
Review owner:
```
