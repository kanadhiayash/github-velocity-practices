# Security Policy

## Scope

This repository contains documentation, templates, checklists, and workflow examples. It should never contain live credentials, exploit payloads, private infrastructure details, or real incident data.

## Supported versions

Only the current `main` branch is supported.

## Reporting a vulnerability

Report security concerns by opening a private security advisory if available, or by contacting the maintainer through the repository owner profile.

Do not publish live exploit details in a public issue.

## Required security standards

- No real secrets in examples.
- No private tokens, API keys, credentials, certificates, or connection strings.
- No internal machine paths.
- No customer, client, user, employee, or private contributor data.
- No live incident logs from real systems.
- No instructions that bypass repository safety controls.

## Workflow security baseline

Required:

- Set workflow permissions to the minimum required level.
- Avoid storing sensitive values in workflow files.
- Use repository or environment secrets for sensitive values.
- Rotate exposed secrets immediately.
- Treat third-party actions as supply-chain dependencies.
- Pin high-risk actions where appropriate.
- Review workflows that run on pull requests from forks.

Recommended:

- Use Dependabot for GitHub Actions updates where supported.
- Use code scanning where appropriate for the stack.
- Use secret scanning and push protection where available.
- Review workflow logs for accidental disclosure.

## Security review trigger

Create a security review when a change affects:

- authentication
- authorization
- secrets
- deployment credentials
- CI/CD permissions
- production environment access
- dependency trust boundaries
- release automation
- AI-generated code in security-sensitive paths
