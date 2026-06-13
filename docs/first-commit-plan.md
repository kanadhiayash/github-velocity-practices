# First Commit Plan

Use this plan when creating a new `github-velocity-practices` repository.

## Required repository creation steps

```bash
mkdir github-velocity-practices
cd github-velocity-practices
git init
```

Copy the scaffold into the repository, then run:

```bash
git status
git add .
git commit -m "docs(repo): add GitHub velocity practices manual"
git branch -M main
git remote add origin https://github.com/<owner>/github-velocity-practices.git
git push -u origin main
```

## Required GitHub settings after push

Configure repository settings after the first push:

1. Protect `main` or create a ruleset for `main`.
2. Require pull requests before merge.
3. Require status checks before merge.
4. Disable force pushes to `main`.
5. Enable Dependabot alerts.
6. Enable Dependabot security updates where available.
7. Enable secret scanning where available.
8. Add topics that describe the repository accurately.
9. Add a concise repository description.

## Recommended repository description

```text
A public manual for GitHub velocity, branch discipline, PR review, CI/CD gates, releases, dependency hygiene, security gates, and AI-assisted development.
```

## Recommended topics

```text
github-actions, ci-cd, pull-requests, branch-strategy, release-management, dependency-management, security, code-review, developer-workflow, ai-assisted-development
```

## First release

Tag the first usable public scaffold:

```bash
git tag v0.1.0
git push origin v0.1.0
```

Create release notes using `templates/RELEASE_NOTES.md`.
