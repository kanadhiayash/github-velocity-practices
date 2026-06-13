# Rollback Protocol

Rollback planning keeps incidents from becoming improvisation.

## Required rollback thinking

A pull request needs a rollback note when it changes:

- user-facing behavior
- database schema
- authentication or authorization
- deployment configuration
- workflow permissions
- package versions
- release automation
- production environment behavior

## Required rollback options

At least one option should be documented:

| Option | When useful |
|---|---|
| Revert pull request | Small reversible code change. |
| Revert release tag | Release artifact should no longer be promoted. |
| Disable feature flag | Feature can be turned off without deploy. |
| Roll back deployment | Previous artifact is safe and available. |
| Forward fix | Rollback is riskier than a targeted patch. |
| Manual mitigation | Operational action is needed before code fix. |

## Required rollback plan format

```text
Trigger:
Rollback owner:
Rollback method:
Expected time:
Data risk:
User impact:
Verification after rollback:
Follow-up review:
```

## Recommended practices

- Test rollback paths for production-adjacent systems.
- Keep migrations backward compatible where possible.
- Avoid irreversible changes without explicit risk acceptance.
- Keep previous release artifacts available.
- Record rollback decisions in incident notes.
