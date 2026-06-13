# Commit Discipline

Commits are the audit trail of intent.

## Required format

Use concise conventional-style commits:

```text
<type>(optional-scope): <short description>
```

Examples:

```text
feat(auth): add session expiry check
fix(api): validate object id before lookup
docs(readme): clarify local setup
ci(actions): add dependency audit job
chore(deps): update patch versions
```

## Required practices

- Use present-tense descriptions.
- Keep the subject under 72 characters where possible.
- Avoid vague subjects such as `update`, `fix stuff`, `wip`, or `final`.
- Keep unrelated changes in separate commits or separate pull requests.
- Do not hide risky changes inside broad cleanup commits.

## Recommended practices

- Squash merge small feature branches when repository history should stay simple.
- Preserve commit history for complex migrations when intermediate steps matter.
- Include issue references where useful.
- Include breaking-change notes in the pull request and release notes.

## Optional practices

- Require signed commits.
- Add commit linting.
- Use semantic release tooling when package publishing requires automation.

## Commit review questions

- Does the commit explain intent?
- Can the change be reverted safely?
- Is the commit hiding unrelated work?
- Does a security-sensitive commit need a second review?
