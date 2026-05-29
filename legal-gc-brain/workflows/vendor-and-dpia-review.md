# Vendor and DPIA Review Workflow

## Purpose

Prepare a structured legal, privacy and security review for vendors that process customer, employee or confidential data.

## Trigger

A team wants to onboard a new vendor, expand an existing vendor use case or connect a vendor to internal AI systems.

## Required context

- vendor name and product description
- business owner
- processing purpose
- data categories
- data subjects
- jurisdictions
- subprocessors
- security review
- DPA status
- transfer mechanism
- retention period
- AI or automated processing features

## Review steps

1. Classify vendor risk.
2. Identify whether a DPIA is required.
3. Check DPA completeness.
4. Map subprocessors and transfer exposure.
5. Compare actual use case against contractual scope.
6. Identify required remediation actions.
7. Prepare approval brief.

## Output template

```text
Vendor: [name]
Risk rating: low | medium | high | critical
DPIA required: yes | no | unclear
Approval status: approved | conditional | blocked

Key risks:
- ...

Required remediation:
- ...

Decision owner:
- ...
```

## Escalation triggers

Escalate to legal and security when:

- sensitive data is processed
- customer data leaves approved regions
- subprocessors are not disclosed
- AI training rights are ambiguous
- retention terms are missing
- the vendor can act autonomously inside internal systems
