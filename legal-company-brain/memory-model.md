# Legal Memory Model

This model describes the minimum useful structure for a legal company brain.

## Core entities

| Entity | Description | Example |
|---|---|---|
| `Product` | Product, feature, service or workflow under legal review | AI assistant for customer support |
| `LegalDecision` | A recorded legal judgment or approval | Approved launch in Germany with human review |
| `RegulatoryObligation` | Rule, obligation, deadline or supervisory expectation | DORA register update obligation |
| `ContractCommitment` | Promise made to a customer, vendor or partner | Data retention limited to 30 days |
| `Vendor` | Third-party provider or processor | Cloud OCR provider |
| `Jurisdiction` | Country, state or regulatory market | Germany, France, EU |
| `DataCategory` | Personal, confidential, financial, client or telemetry data | customer support transcripts |
| `Risk` | Legal, privacy, security, regulatory or commercial risk | unapproved model training on customer data |
| `Control` | Mitigation, approval step or monitoring requirement | human review before external response |
| `Source` | Underlying evidence for any answer | memo, contract, ticket, filing, policy |

## Relationship types

| Relationship | Meaning |
|---|---|
| `product_has_risk` | Product or feature is linked to a risk. |
| `risk_mitigated_by_control` | Risk is mitigated by a control. |
| `decision_based_on_source` | Legal decision depends on one or more sources. |
| `decision_applies_to_jurisdiction` | Legal decision applies to a specific market. |
| `contract_commitment_limits_product` | Contract commitment limits roadmap or operations. |
| `vendor_processes_data_category` | Vendor handles a relevant data type. |
| `obligation_requires_owner` | Obligation requires a responsible person or team. |
| `source_supersedes_source` | Later source overrides or updates earlier context. |
| `risk_requires_escalation` | Risk must be escalated to legal, security, DPO or board. |

## Decision record fields

A legal decision should preserve:

```yaml
decision_id: string
title: string
summary: string
owner: string
date: ISO-8601
status: proposed | approved | rejected | superseded
jurisdictions: string[]
products: string[]
sources: string[]
facts_relied_on: string[]
assumptions: string[]
controls_required: string[]
escalation_triggers: string[]
review_by: ISO-8601 | null
```

## Why structure matters

A legal memory system fails if it only stores prose. It needs structured links so an agent can answer questions such as:

- Which decisions depend on a superseded product fact?
- Which vendors process customer data without an up-to-date review?
- Which customer commitments restrict a roadmap change?
- Which jurisdictions were excluded from a launch decision?
- Which board risks lack an owner or deadline?
