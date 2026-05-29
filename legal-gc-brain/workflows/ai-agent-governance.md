# AI Agent Governance Workflow

## Purpose

Evaluate whether an AI agent can be deployed safely inside a company workflow.

## Agent facts to capture

- agent owner
- intended users
- business purpose
- tools available to the agent
- data sources available to the agent
- external actions the agent can take
- human oversight model
- logging and auditability
- rollback mechanism
- customer or employee impact

## Governance classification

| Level | Description | Example |
| --- | --- | --- |
| 1 | Read-only assistant | Internal policy Q&A |
| 2 | Drafting assistant | Contract redline draft |
| 3 | Internal action agent | Creates tickets or updates records |
| 4 | External action agent | Sends emails or customer notices |
| 5 | Regulated or high-impact agent | Legal, financial, HR or compliance decision support |

## Required controls

```text
Level 1: source citations, logging
Level 2: human review before use
Level 3: permission scoping, rollback, audit log
Level 4: human approval before external action
Level 5: legal, security and executive approval
```

## Output template

```text
Agent governance classification: Level [x]
Deployment recommendation: approved | conditional | blocked

Required controls:
1. ...

Human approval required before:
- ...

Open legal questions:
- ...
```

## Non-negotiable boundary

An agent may support legal judgment. It may not become the accountable legal decision-maker.
