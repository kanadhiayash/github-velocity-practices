# Release Strategy

Release strategy defines how reviewed changes become usable versions.

## Required practices

- Release from protected `main` or a documented release branch.
- Use version tags for public releases.
- Write release notes before publishing.
- Identify breaking changes.
- Identify migration steps.
- Identify rollback or recovery path.
- Do not publish release artifacts from unreviewed code.

## Recommended version model

Use semantic-style versioning for public releases:

```text
v<major>.<minor>.<patch>
```

Examples:

```text
v0.1.0
v1.0.0
v1.1.0
v1.1.1
```

## Required release note sections

```text
Summary
Changes
Security notes
Migration notes
Known issues
Rollback plan
Verification
```

## Recommended release stages

| Stage | Purpose |
|---|---|
| Alpha | Internal or early validation. |
| Beta | Wider testing with known risk. |
| Release candidate | Final validation before public release. |
| Stable | Public release considered ready. |
| Patch | Small fix to stable release. |

## Optional practices

- Generate release notes automatically from pull requests.
- Sign tags.
- Publish artifacts through a release workflow.
- Require environment approval before production deployment.
- Use feature flags for risky features.
