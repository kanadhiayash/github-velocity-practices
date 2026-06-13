# Pull Request Review Protocol

Pull requests are the main review boundary for quality, security, architecture, and product impact.

## Required pull request content

Every pull request should include:

- summary
- change type
- reason for change
- affected files or modules
- validation evidence
- risks
- rollback note when behavior changes
- AI assistance note when relevant

## Required review gates

A pull request must not merge until:

- required checks pass
- secrets are absent
- the diff has one clear purpose
- reviewer comments are addressed or explicitly deferred
- security-sensitive files receive security review
- release notes are updated when user-facing behavior changes

## Recommended pull request size

Use small pull requests by default.

| Pull request size | Review posture |
|---|---|
| Under 300 effective lines | Preferred. Usually reviewable in one pass. |
| 300 to 800 effective lines | Acceptable with clear structure and test evidence. |
| Over 800 effective lines | Split unless the change is generated, mechanical, or migration-only. |

## Required review categories

| Category | Review question |
|---|---|
| Purpose | Does the pull request do one coherent thing? |
| Correctness | Does the change satisfy the stated behavior? |
| Security | Does it introduce secret, auth, permission, dependency, or workflow risk? |
| Architecture | Does it fit the repository boundaries? |
| Product impact | Does it change user behavior, setup, or release promises? |
| Tests | Do checks cover the important behavior? |
| Docs | Are setup, release, or operational docs updated? |
| Rollback | Can the change be reverted or mitigated? |

## Recommended review language

Use labels to separate blocking and non-blocking feedback:

```text
Blocker: must change before merge.
Question: clarification needed.
Suggestion: improvement, not required.
Nit: small style issue, not blocking.
```

## Optional practices

- Require code owner review for critical paths.
- Add review rotation for team repositories.
- Add automated pull request labeling.
- Add pull request size checks.
