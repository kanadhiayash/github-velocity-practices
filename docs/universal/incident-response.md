# Incident Response

An incident is any failure that affects release safety, workflow safety, repository integrity, user trust, or production behavior.

## Incident triggers

Create an incident response record when:

- a secret is exposed
- CI/CD deploys the wrong artifact
- a release breaks critical behavior
- dependency update introduces a vulnerability or outage
- workflow permissions allow unintended access
- branch protection is bypassed
- production data is affected
- AI-generated code introduces a serious defect

## Required response phases

1. Triage.
2. Containment.
3. Communication.
4. Fix or rollback.
5. Verification.
6. Post-incident review.
7. Prevention update.

## Required incident record

```text
Incident title:
Date:
Detected by:
Impact:
Current status:
Facts:
Assumptions:
Unknowns:
Risks:
Actions taken:
Verification:
Follow-up owners:
```

## Recommended severity levels

| Severity | Meaning |
|---|---|
| SEV1 | Active security exposure, production outage, or data integrity risk. |
| SEV2 | Major user impact or broken release path. |
| SEV3 | Limited impact with known mitigation. |
| SEV4 | Low impact issue worth tracking. |

## Required post-incident update

Every serious incident should update at least one of:

- checklist
- workflow
- template
- repository setting
- release process
- dependency policy
- AI review policy
