# CI/CD Readiness Checklist

## Required

- [ ] Workflow triggers are explicit.
- [ ] Workflow permissions are explicit.
- [ ] Required job names are stable.
- [ ] Checks run on pull requests to `main`.
- [ ] Secrets are not printed.
- [ ] Build or test failure blocks merge.
- [ ] Release jobs do not run on unreviewed pull request code.

## Recommended

- [ ] Slow jobs are separated from fast feedback jobs.
- [ ] Concurrency cancels stale runs where appropriate.
- [ ] Cache usage is documented.
- [ ] Deployment uses protected environments where needed.
