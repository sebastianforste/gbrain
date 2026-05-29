# Legal Context Server Design

## Purpose

Design a permissioned MCP-style legal context server for a GC brain.

The server should expose trusted legal context to agents without giving every agent raw access to every legal document.

## Resources

```text
legal://policies/privacy-policy
legal://policies/ai-governance-policy
legal://playbooks/customer-contracting
legal://playbooks/vendor-review
legal://regulatory/eu-ai-act
legal://regulatory/gdpr
legal://decisions/product-launches
legal://decisions/vendor-approvals
```

## Tools

```text
legal.search_sources(query, jurisdiction, source_type)
legal.get_playbook(topic)
legal.check_contract_deviation(contract_summary, playbook_id)
legal.classify_agent_risk(agent_capabilities)
legal.prepare_approval_brief(issue_id)
legal.list_open_legal_gaps(owner, age_days)
```

## Permission model

| Scope | Capability |
| --- | --- |
| `legal:read` | Read approved policies and playbooks |
| `legal:context` | Retrieve source-grounded context snippets |
| `legal:decision:read` | Read prior decisions |
| `legal:decision:draft` | Draft new decision records |
| `legal:admin` | Manage schema, sources and permissions |

## Guardrails

The context server should:

- return citations with every substantive answer
- expose only approved sources by default
- separate draft and approved legal positions
- log each retrieval and tool call
- require human approval before external legal communications
- prevent agents from treating draft memos as binding policy

## Example agent flow

```text
1. Agent asks for product launch context.
2. Server returns relevant policies, contract playbook and prior decisions.
3. Agent drafts issue summary.
4. Server classifies missing facts and approval path.
5. Human legal owner reviews final decision.
```

## Design thesis

Legal AI needs controlled context, not unlimited context. The legal context server is the boundary between operational agents and accountable legal judgment.
