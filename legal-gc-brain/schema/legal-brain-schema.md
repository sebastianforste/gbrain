# Legal Brain Schema

A legal brain should model legal work as linked operational knowledge rather than loose notes.

## Core entities

| Entity | Purpose |
| --- | --- |
| `product` | Product, feature or agent capability under review |
| `customer` | Customer, prospect or strategic counterparty |
| `contract` | Agreement, order form, DPA, policy or amendment |
| `obligation` | Legal, regulatory, contractual or internal requirement |
| `source` | Statute, regulator guidance, policy, playbook or precedent |
| `decision` | Legal or governance judgment with owner and date |
| `risk` | Classified issue requiring mitigation or acceptance |
| `approval` | Human sign-off event |
| `evidence` | Supporting document, meeting note, email or system record |

## Suggested typed edges

```text
product -> triggers -> obligation
obligation -> derived_from -> source
contract -> deviates_from -> playbook
risk -> mitigated_by -> control
approval -> approves -> decision
decision -> relies_on -> evidence
customer -> negotiated -> contract
agent -> uses -> tool
agent -> accesses -> data_source
```

## Minimal frontmatter shape

```yaml
type: decision
owner: legal
status: draft | approved | escalated | rejected
risk_level: low | medium | high | critical
jurisdiction: EU | US | global
source_confidence: low | medium | high
human_approval_required: true
```

## Rule of thumb

Every legal answer should be traceable to:

```text
claim -> source -> evidence -> decision -> accountable owner
```
