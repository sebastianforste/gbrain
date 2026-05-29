# Legal GC Brain

This fork adds a legal engineering layer on top of GBrain for general counsel, product counsel, privacy, regulatory and AI governance workflows.

The goal is simple: turn private legal knowledge into a permissioned, queryable and auditable brain for a modern AI company.

## Why this matters

Legal work inside an AI company is not only document review. It is a system of linked decisions:

- product feature
- customer promise
- regulatory source
- risk classification
- approval owner
- escalation path
- contractual fallback
- audit trail

A normal RAG system retrieves fragments. A legal GC brain should answer with sourced reasoning, stale-context warnings and explicit escalation logic.

## Dust-facing signal

This repository is useful as a portfolio signal because it shows three things at once:

1. Senior legal judgment can be encoded as workflows.
2. Legal context can be structured as a graph instead of a folder of memos.
3. AI agents need guardrails, handoffs and human approval for legal decisions.

## What this fork adds

The additions live in `legal-gc-brain/`:

```text
legal-gc-brain/
  README.md
  schema/legal-brain-schema.md
  workflows/product-launch-review.md
  workflows/vendor-and-dpia-review.md
  workflows/ai-agent-governance.md
  queries/sample-gc-queries.md
  scorecard/gc-brain-eval-rubric.md
  mcp/legal-context-server-design.md
```

## Core design principle

The brain does not replace the lawyer. It does the preparation work:

- finds the relevant source material
- identifies legal and commercial gaps
- links people, products, contracts, policies and regulatory obligations
- drafts a decision brief
- highlights stale or missing evidence
- routes the final judgment to the responsible human

## Example use cases

### Product counsel

Ask:

```text
Can we launch this AI assistant feature for EU enterprise customers under our current DPA, privacy policy and internal AI governance policy?
```

The brain should return:

- relevant product facts
- applicable privacy and AI governance obligations
- missing information
- red flags
- suggested approval path
- source citations

### General counsel

Ask:

```text
What are the top unresolved legal risks before signing this strategic customer contract?
```

The brain should return:

- unresolved negotiation points
- deviations from playbook
- business owner context
- precedent from similar deals
- required approvals
- recommended fallback position

### Regulatory strategy

Ask:

```text
Which product features may create MiCAR, DORA, PSD2 or AI Act exposure in the next release?
```

The brain should return:

- mapped obligations
- impacted product surfaces
- required owner input
- supervisory risk note
- implementation checklist

## Why a graph is essential

Legal work is graph-shaped:

```text
source -> obligation -> product surface -> decision -> owner -> approval -> evidence
```

The legal brain should expose those relationships instead of only storing notes.

## Human approval boundary

A legal GC brain may draft, compare, classify and escalate. It should not autonomously:

- approve regulated product launches
- waive contractual protections
- send legal advice externally
- make employment, litigation or regulatory commitments
- sign filings or customer documents

Those actions require an accountable human decision.

## Portfolio positioning

This fork tells a coherent story for an AI-operator company:

```text
gstack -> legal GC workflows
gbrain-evals -> legal AI evaluation discipline
gbrain -> legal institutional memory and permissioned GC brain
```

That is the intended signal: not just legal AI enthusiasm, but legal infrastructure design.