# Repository Settings

Repository settings define the default safety rail for change flow.

## Required settings

- Protect `main` or apply a ruleset to `main`.
- Require pull requests before merge.
- Require required checks before merge.
- Disable force pushes to protected branches.
- Require branch to be up to date before merge when the repository has shared ownership or high deployment risk.
- Require conversation resolution before merge.
- Keep repository visibility intentional.
- Enable vulnerability reporting where available.
- Enable dependency graph and Dependabot alerts where available.

## Recommended settings

- Use rulesets for branch and tag protection when available.
- Require signed commits for higher-risk repositories.
- Require linear history when release traceability matters.
- Restrict who can push to protected branches.
- Protect version tags such as `v*`.
- Disable auto-merge for security-sensitive repositories unless dependency-only criteria are explicit.

## Optional settings

- Require code owner review.
- Add deployment environments with reviewers.
- Add environment-specific secrets.
- Add branch naming rules.
- Add tag naming rules.

## Required evidence

Before declaring settings complete, record:

| Evidence | Required status |
|---|---|
| Protected branch or ruleset screenshot or note | Fact |
| Required checks list | Fact |
| Merge method policy | Fact |
| Dependabot status | Fact or Unknown |
| Secret scanning status | Fact or Unknown |
| Remaining gaps | Risk |

## Review prompt

```text
Fact:
Assumption:
Unknown:
Risk:
Decision:
Next action:
```
