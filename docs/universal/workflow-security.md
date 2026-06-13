# Workflow Security

GitHub Actions workflows are executable infrastructure. Treat them as production-adjacent code.

## Required practices

- Set `permissions` explicitly.
- Use `contents: read` by default.
- Increase permissions only for jobs that require them.
- Store sensitive values in secrets or protected environments, not workflow files.
- Mask non-secret sensitive values before logging.
- Avoid printing environment variables.
- Review third-party actions before use.
- Avoid running untrusted pull request code with write tokens.
- Rotate any exposed secret immediately.

## Recommended practices

- Pin high-risk third-party actions to a commit SHA.
- Use Dependabot updates for GitHub Actions.
- Prefer maintained actions with clear ownership and release history.
- Use separate jobs for read-only validation and write-capable release actions.
- Use protected environments for production deployments.
- Limit deployment secrets to the environment that needs them.

## Optional practices

- Use OpenID Connect for cloud deployments instead of long-lived cloud keys.
- Add policy checks for workflow permissions.
- Add allowed-actions controls in organization settings.
- Use self-hosted runners only with documented isolation and cleanup.

## Required review trigger

A workflow security review is required when a pull request changes:

- `.github/workflows/`
- `.github/actions/`
- deployment scripts
- release automation
- repository secrets usage
- environment secret usage
- dependency installation scripts
- generated code execution paths
