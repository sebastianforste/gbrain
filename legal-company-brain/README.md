# Legal Company Brain Layer

A legal company brain is a source-grounded memory layer for General Counsel and product counsel work.

It should help a legal team answer operational questions with citations, context, uncertainty and escalation logic.

## Use cases

| Use case | What the brain should retrieve | Output shape |
|---|---|---|
| Product launch review | product specs, prior legal decisions, privacy reviews, jurisdiction notes | launch risks, missing facts, escalation triggers |
| Vendor renewal review | DPA, security review, subprocessor record, prior negotiations | renewal constraints, stale checks, negotiation points |
| Customer commitment analysis | MSA, order form, security addendum, product notes | commitments that limit roadmap or operations |
| Regulatory horizon review | regulatory sources, internal memos, issue decisions | changes, affected products, owner, due date |
| Board legal risk brief | open matters, incident notes, vendor risk, regulatory changes | executive risk summary with source links |
| AI governance review | model use case, data categories, human review, logs | control gaps and approval path |

## Design principles

1. Every consequential claim should cite a source.
2. The answer should say what it does not know.
3. The answer should separate facts, assumptions and judgment.
4. The system should preserve the history of legal decisions, not merely final documents.
5. Access controls matter because legal memory contains sensitive context.
6. Privilege and confidentiality rules should be visible in the workflow.
7. Human review is mandatory for external advice, regulatory filings and board-level conclusions.

## Folder contents

- [`memory-model.md`](memory-model.md) defines legal entities and relationships.
- [`source-classification.md`](source-classification.md) classifies source types by trust and sensitivity.
- [`query-patterns.md`](query-patterns.md) gives reusable GC queries.
- [`fixtures/product-launch-memory.json`](fixtures/product-launch-memory.json) provides synthetic sample memory.
- [`reviewer-checklist.md`](reviewer-checklist.md) provides an answer-quality checklist.

## Non-goals

This layer is not a legal-advice product, not a substitute for counsel and not a production deployment. It is a public-safe design scaffold for legal AI memory, retrieval and governance workflows.
