# Senior Engineer Review Checklist

Use this checklist to inspect whether a repository can move changes safely.

## Security maturity

- [ ] `SECURITY.md` exists and defines reporting boundaries.
- [ ] Workflow permissions are explicit and minimal.
- [ ] Secrets policy is clear.
- [ ] Dependency review is documented.
- [ ] Security-sensitive changes require extra review.

## Architecture thinking

- [ ] Branch flow is documented.
- [ ] Required checks match the stack.
- [ ] Environments and release path are documented where applicable.
- [ ] Rollback protocol exists.

## Product judgment

- [ ] Release impact is reviewed before public release.
- [ ] User-facing changes require release notes.
- [ ] Risk is classified before merge.
- [ ] Incidents produce process updates.

## Discipline and execution hygiene

- [ ] Pull requests have one clear purpose.
- [ ] Commit messages are meaningful.
- [ ] CI failures block merge.
- [ ] Dependency updates have a maintenance path.
- [ ] Release notes and tags are consistent.

## AI workflow maturity

- [ ] AI-assisted changes are disclosed.
- [ ] AI output is verified by checks or human review.
- [ ] AI-generated workflow changes require security review.
- [ ] AI is never allowed to bypass gates.
