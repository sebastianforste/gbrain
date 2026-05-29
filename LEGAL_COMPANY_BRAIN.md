# Legal Company Brain

This fork adds a public, legal-engineering layer on top of GBrain.

The aim is to explore how a General Counsel, product counsel team, or legal operations function could use a company-brain architecture for regulated AI, fintech, crypto, payments and enterprise software companies.

The core thesis is simple:

> A legal team should not merely answer recurring questions. It should preserve context, map obligations, remember decisions, surface gaps and turn repeated legal judgment into safer internal workflows.

## Why this matters

Fast-moving AI companies accumulate legal context across many places:

- product launch discussions
- customer contracts
- vendor reviews
- privacy assessments
- regulatory memos
- board materials
- security reviews
- incident postmortems
- investor and commercial commitments
- jurisdictional launch decisions

Traditional legal knowledge management stores documents. A legal company brain should answer operational questions with cited context, missing-information warnings and escalation triggers.

## Example questions

A legal company brain should support questions such as:

```text
What changed since our last review of this AI feature?
Which customer commitments limit how we can change retention defaults?
What regulatory assumptions did we make before launching in France?
Which vendor reviews are stale and need renewal before renewal season?
What open legal risks should the board see this month?
Which product counsel decisions were based on facts that are now outdated?
```

## Added in this fork

This fork adds a dedicated legal layer under [`legal-company-brain/`](legal-company-brain/):

- legal memory model
- entity and relationship map
- source classification rules
- confidentiality and privilege handling notes
- query patterns for General Counsel work
- sample memory fixture
- reviewer checklist for answer quality

## Public-data boundary

All examples in this fork are public-safe and synthetic. They are not legal advice and do not contain client matter data, privileged information, personal data or confidential commercial information.

## Intended signal

This layer is meant to show practical legal-engineering judgment:

- legal work as institutional memory, not one-off documents
- source-grounded answers instead of fluent guesses
- explicit uncertainty and gap analysis
- access-aware company knowledge
- human escalation for consequential legal decisions
- reusable playbooks for recurring legal operations
