# Source Classification Rules

A legal company brain should classify every source by trust level, sensitivity and operational use.

## Trust levels

| Level | Source type | Typical use |
|---|---|---|
| 1 | Primary legal source | Regulation, statute, regulator guidance, official filing |
| 2 | Binding internal source | Signed contract, approved policy, board minute, final legal memo |
| 3 | Controlled operational source | Product spec, security review, privacy assessment, ticket, issue tracker |
| 4 | Informal internal source | Slack thread, draft note, meeting transcript, email discussion |
| 5 | External commentary | Blog post, news article, vendor marketing, conference note |

## Sensitivity labels

| Label | Meaning |
|---|---|
| `public` | Safe for public examples and open-source fixtures. |
| `internal` | Internal company context, not for public disclosure. |
| `confidential` | Commercial, strategic or security-sensitive material. |
| `privileged` | Attorney-client or legal work-product material. |
| `personal-data` | Contains personal data or employee/customer identifiers. |
| `regulated-data` | Financial, health, payments, crypto, security or other regulated data. |

## Retrieval rules

1. Prefer primary legal sources and final internal decisions for legal conclusions.
2. Use informal sources for context, not as sole authority for legal conclusions.
3. Flag contradictions between newer operational facts and older legal decisions.
4. Flag stale sources when the review date has passed or facts may have changed.
5. Do not expose privileged or confidential sources to users without appropriate access.
6. Do not use personal data in public demos or eval fixtures.
7. If the source mix is weak, the answer must say so explicitly.

## Output rule

Every answer should include:

```text
Sources used
Sources not available
Stale or conflicting sources
Assumptions
Escalation trigger
```

## Example classification

```yaml
source_id: src_001
title: AI Support Assistant Launch Memo
type: final_legal_memo
trust_level: 2
sensitivity: privileged
owner: legal
review_by: 2026-09-30
can_use_for_public_demo: false
```
