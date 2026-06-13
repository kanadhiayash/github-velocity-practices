# Start Here

This manual defines GitHub velocity practices for repositories that need safe change flow, reliable automation, reviewable releases, and maintainable contributor habits.

## The shortest useful path

For a small public repository, start with:

```text
README.md
SECURITY.md
.github/
  pull_request_template.md
  workflows/
    ci.yml
.github/dependabot.yml
docs/
  releases/
  decisions/
  incidents/
templates/
checklists/
```

## Required setup for every repository

| Required item | Why it exists |
|---|---|
| Protected `main` | Prevents unreviewed or failing changes from entering the stable branch. |
| Pull request template | Makes review intent, risk, and evidence visible. |
| Required checks | Prevents merge when automated quality gates fail. |
| Minimal workflow permissions | Reduces impact if a workflow or action is abused. |
| Secrets policy | Prevents credentials from entering source control or logs. |
| Dependency update policy | Keeps known vulnerabilities and stale packages visible. |
| Release checklist | Prevents public shipping without version, notes, and rollback thinking. |
| Incident path | Defines what happens when a release or workflow fails. |

## Required thinking before implementation

Before implementation begins:

1. Define branch type and expected lifetime.
2. Define the pull request size target.
3. List required checks.
4. Identify security-sensitive files.
5. Identify dependency or migration impact.
6. Define the rollback or recovery path.
7. Mark facts, assumptions, unknowns, and risks.

## Required thinking before merge

Before merge:

1. Confirm the pull request has one clear purpose.
2. Confirm required checks pass.
3. Confirm the diff is reviewable.
4. Confirm secrets are not present.
5. Confirm dependency changes are justified.
6. Confirm release notes or changelog entries are ready when needed.
7. Confirm AI-assisted changes are disclosed where relevant.

## Recommended adoption order

1. Repository settings
2. Branch strategy
3. Commit discipline
4. Pull request template
5. CI gate
6. Security gate
7. Dependency hygiene
8. Release strategy
9. Rollback protocol
10. Stack overlay
11. AI-assisted development policy
12. Velocity metrics

## Common anti-patterns

| Anti-pattern | Better practice |
|---|---|
| Direct pushes to `main` | Require pull requests and checks. |
| Large mixed-purpose pull requests | Keep one purpose per pull request. |
| CI only after merge | Run checks before merge. |
| Workflows with broad permissions | Set minimum required permissions. |
| Dependency updates ignored for months | Use scheduled dependency review. |
| Release notes written from memory | Capture release impact during the pull request. |
| AI-generated code merged unreviewed | Treat AI output like any other untrusted contribution. |
