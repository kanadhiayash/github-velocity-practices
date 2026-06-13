# Security Gate Checklist

## Required

- [ ] No secrets in diff.
- [ ] No private local paths.
- [ ] No private user, client, or environment data.
- [ ] Workflow permissions reviewed.
- [ ] Third-party actions reviewed.
- [ ] Dependency changes reviewed.
- [ ] Auth and permission changes reviewed.
- [ ] Release notes avoid sensitive details.

## Recommended

- [ ] Code scanning reviewed where available.
- [ ] Secret scanning reviewed where available.
- [ ] Dependabot alerts reviewed.
- [ ] Security exception recorded if risk is accepted.
