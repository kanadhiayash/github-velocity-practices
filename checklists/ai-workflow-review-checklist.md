# AI Workflow Review Checklist

## Required

- [ ] AI-assisted changes are labeled.
- [ ] Generated code reviewed as untrusted code.
- [ ] No private data appears in prompts, examples, or comments.
- [ ] AI did not add unreviewed dependencies.
- [ ] AI did not weaken validation, auth, tests, or error handling.
- [ ] Behavior verified through tests, build, logs, or manual run.
- [ ] Workflow or release changes receive security review.

## Recommended

- [ ] AI summary checked against actual diff.
- [ ] Edge cases reviewed manually.
- [ ] Rollback note reviewed by a human.
- [ ] Follow-up limitations recorded.
