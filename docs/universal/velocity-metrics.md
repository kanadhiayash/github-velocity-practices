# Velocity Metrics

Velocity metrics should improve flow without rewarding unsafe behavior.

## Required principle

Measure flow and safety together. Do not optimize for more commits, more pull requests, or faster merges if quality and security decline.

## Recommended metrics

| Metric | Useful signal | Failure mode |
|---|---|---|
| Pull request cycle time | How quickly review completes. | Can reward rushed review. |
| Pull request size | Whether work is reviewable. | Can reward artificial splitting. |
| Change failure rate | Whether releases break behavior. | Requires honest incident tracking. |
| Time to restore | How quickly rollback or fix happens. | Can hide preventable failures. |
| Flaky test rate | CI trust level. | Often ignored until CI is bypassed. |
| Dependency update age | Maintenance freshness. | Noise from low-risk updates. |

## Required interpretation model

Use the evidence model:

```text
Fact: Pull request size increased over the last 10 merged changes.
Assumption: Larger pull requests are slowing review.
Unknown: Whether review delay comes from size, unclear scope, or reviewer availability.
Risk: Maintainers may bypass review if feedback feels too slow.
```

## Recommended cadence

- Weekly for active teams.
- Monthly for solo or portfolio repositories.
- Before major releases.
- After incidents or workflow failures.

## Optional practices

- Track DORA-style indicators for production systems.
- Track documentation freshness.
- Track release readiness misses.
- Track review rework causes.
