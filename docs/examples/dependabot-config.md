# Example: Dependabot Configuration

```yaml
version: 2
updates:
  - package-ecosystem: "github-actions"
    directory: "/"
    schedule:
      interval: "weekly"

  - package-ecosystem: "npm"
    directory: "/"
    schedule:
      interval: "weekly"
    open-pull-requests-limit: 5
```

Required:

- Adjust package ecosystems to the repository.
- Review dependency pull requests before merge.
- Do not auto-merge major updates without validation.
