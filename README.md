# GitHub Velocity Practices

A public field manual for moving code through GitHub with small changes, fast feedback, reviewable automation, and security-aware release discipline.

This manual is a separate repository from `project-practices`. It does not define project folder architecture as its main subject. It defines how work moves after a repository exists: branches, commits, pull requests, status checks, CI/CD gates, dependency updates, releases, incidents, rollback, and AI-assisted changes.

## Purpose

Velocity is not speed without control. Velocity means a repository can accept frequent change without losing review quality, security posture, release confidence, or historical traceability.

This repository defines practices that reduce these failures:

- long-lived branches that drift from `main`
- unclear commit intent
- large pull requests that reviewers cannot reason about
- CI workflows that run too late or too broadly
- security checks treated as optional cleanup
- release notes written after memory fades
- dependency updates allowed to rot
- AI-generated changes bypassing normal review
- rollback plans missing until an incident starts

## How this complements Repo 1

| Repository | Primary job | Boundary |
|---|---|---|
| `project-practices` | Structure, naming, documentation, audit, project memory, and maintenance. | Defines how a project is organized and kept understandable. |
| `github-velocity-practices` | Branch discipline, pull request flow, CI/CD gates, release hygiene, dependency review, and safe automation. | Defines how change moves through GitHub. |

Repo 1 answers: where should work live, how should it be named, and how should decisions be recorded.

Repo 2 answers: how should work enter, be reviewed, tested, merged, released, monitored, and corrected.

## Audience

This manual is written for:

- builders maintaining public portfolio repositories
- maintainers running small teams
- contributors proposing changes through pull requests
- senior reviewers checking GitHub maturity before an interview
- teams adding CI/CD without turning every change into process theater
- AI-assisted development workflows that still require human accountability

## Rule levels

| Level | Meaning |
|---|---|
| Required | Must be present for any serious public repository or production-adjacent project. |
| Recommended | Strong default unless project constraints justify a simpler path. |
| Optional | Useful for larger teams, regulated domains, high-risk deployments, or public releases. |

## Evidence model

All operational claims should be marked as one of four types:

| Type | Definition |
|---|---|
| Fact | Verified from a source, artifact, test result, workflow run, release, log, or working system. |
| Assumption | Believed to be true, but not yet verified. |
| Unknown | Important missing information that blocks or weakens judgment. |
| Risk | A possible failure mode with impact, likelihood, owner, and mitigation. |

## Repository map

```text
github-velocity-practices/
├── README.md
├── LICENSE
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── SECURITY.md
├── docs/
│   ├── start-here.md
│   ├── universal/
│   ├── overlays/
│   └── examples/
├── templates/
└── checklists/
```

## Start here

Read these files first:

1. [`docs/start-here.md`](docs/start-here.md)
2. [`docs/universal/repository-settings.md`](docs/universal/repository-settings.md)
3. [`docs/universal/branch-strategy.md`](docs/universal/branch-strategy.md)
4. [`docs/universal/pr-review-protocol.md`](docs/universal/pr-review-protocol.md)
5. [`docs/universal/ci-cd-gates.md`](docs/universal/ci-cd-gates.md)
6. [`docs/universal/security-gates.md`](docs/universal/security-gates.md)
7. [`checklists/senior-engineer-review-checklist.md`](checklists/senior-engineer-review-checklist.md)

## 30-second review signal

A reviewer should be able to see these five signals quickly:

| Rank | Signal | What to inspect |
|---:|---|---|
| 1 | Security maturity | `SECURITY.md`, security gates, secrets handling, dependency review, workflow permissions. |
| 2 | Architecture thinking | branching model, workflow boundaries, environment separation, release and rollback plans. |
| 3 | Product judgment | release criteria, feature flags, risk classification, user impact review. |
| 4 | Discipline and execution hygiene | commits, pull request size, status checks, maintenance cadence, release notes. |
| 5 | AI workflow maturity | AI changes are labeled, reviewed, tested, and never exempt from security gates. |

## Reviewer path

For a fast senior-reviewer pass, inspect this sequence:

1. Read the README for purpose, scope, rule levels, and relationship to `project-practices`.
2. Open `SECURITY.md` and `docs/universal/security-gates.md` for safety posture.
3. Open `docs/universal/repository-settings.md` for branch protection, rulesets, and required checks.
4. Open `docs/universal/pr-review-protocol.md` for pull request discipline.
5. Open `docs/universal/ci-cd-gates.md` for automation quality.
6. Open `docs/universal/release-strategy.md` and `docs/universal/rollback-protocol.md` for shipping discipline.
7. Open the relevant stack overlay.
8. Use `checklists/senior-engineer-review-checklist.md` as the final inspection path.

## Public copy standards

Public examples should avoid personal details, private project names, unsupported performance claims, real credentials, client data, internal paths, and invented metrics.

## Core documents

| Area | File |
|---|---|
| Repository settings | [`docs/universal/repository-settings.md`](docs/universal/repository-settings.md) |
| Branch strategy | [`docs/universal/branch-strategy.md`](docs/universal/branch-strategy.md) |
| Commit discipline | [`docs/universal/commit-discipline.md`](docs/universal/commit-discipline.md) |
| Pull request review | [`docs/universal/pr-review-protocol.md`](docs/universal/pr-review-protocol.md) |
| CI/CD gates | [`docs/universal/ci-cd-gates.md`](docs/universal/ci-cd-gates.md) |
| Workflow security | [`docs/universal/workflow-security.md`](docs/universal/workflow-security.md) |
| Dependency hygiene | [`docs/universal/dependency-hygiene.md`](docs/universal/dependency-hygiene.md) |
| Release strategy | [`docs/universal/release-strategy.md`](docs/universal/release-strategy.md) |
| Rollback protocol | [`docs/universal/rollback-protocol.md`](docs/universal/rollback-protocol.md) |
| Incident response | [`docs/universal/incident-response.md`](docs/universal/incident-response.md) |
| Velocity metrics | [`docs/universal/velocity-metrics.md`](docs/universal/velocity-metrics.md) |
| AI-assisted development | [`docs/universal/ai-assisted-development.md`](docs/universal/ai-assisted-development.md) |

## Stack overlays

Use the universal rules first, then apply the relevant overlay.

| Stack | Overlay |
|---|---|
| Swift and iOS | [`docs/overlays/swift-ios.md`](docs/overlays/swift-ios.md) |
| React Native | [`docs/overlays/react-native.md`](docs/overlays/react-native.md) |
| Node and Express | [`docs/overlays/node-express.md`](docs/overlays/node-express.md) |
| Jetpack Compose | [`docs/overlays/jetpack-compose.md`](docs/overlays/jetpack-compose.md) |
| Vanilla JavaScript | [`docs/overlays/vanilla-js.md`](docs/overlays/vanilla-js.md) |
| Full-stack products | [`docs/overlays/full-stack.md`](docs/overlays/full-stack.md) |

## Templates

Templates are provided for repeatable GitHub operations:

- velocity brief
- branch plan
- pull request review
- CI gate review
- workflow security review
- dependency review
- release plan
- release notes
- rollback plan
- incident response
- AI change log

## Not covered

This manual does not replace:

- official GitHub documentation
- company policy
- legal, privacy, compliance, or security counsel
- production incident procedures for regulated systems
- stack-specific framework documentation

Use this manual as a baseline, then add stricter rules where project risk requires them.
