# AI-Assisted Development

AI-assisted development can improve throughput, but AI output is not evidence by itself.

## Required practices

- Label AI-assisted changes when AI materially influenced the diff.
- Review AI-generated code as untrusted code.
- Run the same CI, security, and release gates.
- Do not let AI write or expose secrets.
- Do not paste private data into public prompts or public examples.
- Do not accept generated dependency additions without review.
- Do not accept generated workflow changes without permission review.
- Verify behavior through tests, build output, manual checks, or working artifacts.

## Recommended practices

- Ask AI for a plan before multi-file changes.
- Keep AI-assisted pull requests small.
- Use AI to draft tests, then inspect edge cases manually.
- Use AI to summarize diffs, but verify the summary against the actual diff.
- Use AI to propose rollback plans, but treat them as assumptions until verified.

## Optional practices

- Keep an AI change log for major changes.
- Add prompt risk notes for security-sensitive work.
- Use separate AI review passes for architecture, security, and test coverage.
- Use generated code provenance notes for regulated or high-risk contexts.

## Required AI change note

```text
AI assistance used:
Files affected:
Human verification performed:
Known limitations:
Risk level:
```

## AI review questions

- Does the diff contain behavior not requested?
- Did AI add dependencies?
- Did AI weaken validation, auth, tests, or error handling?
- Did AI hallucinate APIs or configuration keys?
- Did AI modify workflows or release scripts?
- Is the result verified by a source or running system?
