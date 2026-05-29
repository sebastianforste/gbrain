# Product Launch Review Workflow

## Purpose

Create a repeatable legal review workflow for AI product launches.

## Trigger

A team wants to launch, materially change or expand an AI product feature.

## Required context

- feature description
- intended users and jurisdictions
- data categories processed
- model or agent capabilities
- customer-facing claims
- applicable contract terms
- privacy policy and DPA impact
- internal AI governance policy
- security and vendor dependencies

## Review steps

1. Identify product surface.
2. Map product facts to applicable obligations.
3. Compare claims against customer terms and public policies.
4. Identify gaps, contradictions and stale assumptions.
5. Assign risk level.
6. Route to required approver.
7. Generate source-grounded launch note.

## Example output

```text
Recommendation: conditional approval.

The feature may launch for internal beta users only. External enterprise rollout requires an updated DPA annex, clarified customer notice and security confirmation for the new subprocessors.

Open issues:
1. No current evidence for data retention period.
2. Marketing copy implies autonomous decisioning.
3. Customer terms do not yet cover agent tool use.

Required approvals:
- Legal
- Security
- Product owner
```

## Human approval boundary

The system may prepare the recommendation. Final launch approval remains with the accountable human owner.
