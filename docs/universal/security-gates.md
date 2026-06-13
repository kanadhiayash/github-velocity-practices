# Security Gates

Security gates prevent avoidable exposure before merge, release, and deployment.

## Required pre-merge gate

Before merge, verify:

- no secrets in diff
- no real credentials in examples
- no private local paths
- no private user or client data
- no broad workflow permissions without reason
- no dependency changes without review
- no auth or permission change without security review
- no debug logs that reveal sensitive values

## Required pre-release gate

Before release, verify:

- branch or tag points to reviewed code
- required checks passed
- dependency vulnerabilities reviewed
- secrets scan completed where available
- release notes do not disclose sensitive details
- rollback path exists
- incident contact path exists

## Recommended gates

- code scanning for supported stacks
- secret scanning and push protection where available
- dependency review for dependency pull requests
- environment protection for production deployment
- manual approval for production release

## Optional gates

- threat model for public APIs
- software bill of materials for release artifacts
- signed release artifacts
- provenance attestation for packages

## Security exception protocol

A security exception must include:

```text
Exception:
Reason:
Risk accepted:
Expiration date:
Owner:
Mitigation:
Follow-up issue:
```

No exception should be permanent by default.
