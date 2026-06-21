---
name: "solomon-relationship-graph-seed"
description: "Turn credits, collaborators, trusted people, target rooms, and sensitive exclusions into a simple Solomon relationship-edge list that can honestly return no known path."
compatibility: "Created for Zo Computer"
metadata:
  author: "solomonos1.zo.computer"
  category: Solomon
---

# Solomon Relationship Graph Seed

## Must read first

- `Once & For All/Solomon/docs/CANON.md`
- `Once & For All/Solomon/docs/DOCUMENTATION-MAP.md`
- `Once & For All/Solomon/docs/plans/2026-05-12-openhuman-mvp-hardening-design.md`
- `Once & For All/Solomon/docs/CAREER-SUPPORT-ONTOLOGY.md`
- `Once & For All/Solomon/docs/DP-DIAGNOSTIC-V0.md`
- `Once & For All/Solomon/docs/flows/dp-support-suite-first-useful-move.md`

## Canon guardrails

Solomon is representation infrastructure for creative careers. Once & For All builds Solomon. One product, one wedge, one number: 10,000 Solomon clients with at least one accepted, double-opt-in intro or useful career move.

First cohort: DPs / cinematographers.

Current v1 loop:

```text
structured intake → thin profile → relationship graph seed → Jordan-authored support map → one provenance-backed move → client/operator approval → double opt-in → dispatch → outcome tracking
```

Never expose internal agents, support-suite mechanics, harness names, or runtime details to clients. No outbound action without consent. No support-map judgement is presented as autonomous truth before Jordan/operator approval. No provenance, no recommendation.

## Purpose

Use this skill to seed the first relationship graph from known context.

The graph is not a claim of access. It is a trust map with confidence and consent state.

## Inputs

- credits
- call sheets or project histories if already available
- collaborators
- trusted people
- current representatives
- target rooms / companies / people
- sensitive exclusions
- source files or notes
- recency context

## Minimum edge shape

```yaml
person_a: [client or contact]
person_b: [contact]
context_project: [project / room / company / unknown]
context_role: [DP / producer / director / agent / etc.]
context_year: [year / unknown]
relationship_type: [worked together / represented by / referred by / wants to know / sensitive / avoid / unknown]
strength: [strong / medium / weak / unknown]
source: [client stated / credit / call sheet / operator note / public source]
confidence: [high / medium / low]
consent_state: [approved / not approved / sensitive / do not contact / unknown]
notes: [short handling note]
```

## Output format

```markdown
# relationship graph seed - [client]

## known trusted nodes
- [person] - [relationship_type] - [strength] - [source] - [consent_state]

## target rooms / people
- [target] - [why relevant] - [known path or no known path]

## sensitive exclusions
- [person/context] - [handling note]

## candidate paths
1. [client] → [bridge] → [target] - [confidence] - [source]
2. no known path: [target] - [what is missing]

## edge list
[structured edge rows using minimum shape]

## what could be wrong
[uncertainty or missing evidence]
```

## Rules

- It is acceptable and often correct to return `no known path`.
- Do not treat public credits as permission to contact someone.
- Do not infer friendship from shared credits.
- Sensitive exclusions override all other routing.
- Every path needs confidence, source, and consent state.
## MCP Power Layer

These skills are the judgment layer. MCPs and integrations are the hands. Use them when they give Solomon real access, durable records, or live operating context. Do not use an MCP just to look sophisticated.

### Preferred connectors

- Notion MCP or Notion integration for support maps, client rooms, knowledge bases, SOPs, and operating records.
- Google Drive for source docs, onboarding forms, EPKs, contracts, resumes, call sheets, and shared folders.
- Google Sheets or Airtable for support queues, client status, outcome tracking, and relationship records.
- Gmail integration for inbox context, client communication history, and draft support replies.
- Google Calendar for availability, reviews, follow-ups, check-ins, and operating rhythm.
- Linear MCP or Linear integration for support bugs, client requests, and product feedback routing.
- Sentry MCP and Logfire MCP for technical incidents that affect client-facing surfaces.

### Use MCP when

- the skill needs to read or maintain the living record of a client, relationship, outcome, support issue, or incident.
- the work must preserve provenance, consent, and follow-up state.

### Fallback if unavailable

Create or update workspace markdown records only, with clear provenance notes and a list of missing integrations. Do not infer private relationship facts from public data alone.

### Confirmation gates

Ask Jordan before using any connector to:

- send emails, DMs, SMS, or public posts.
- publish, deploy, merge, delete, or overwrite public or production surfaces.
- buy domains, change DNS, rotate secrets, modify billing, or create payment links.
- write private relationship intelligence into a public or shared system.
- commit Jordan, Once & For All, Solomon, or a client to an external obligation.

If the connector is not connected, say so plainly and either use the fallback or surface the correct connect path. Do not simulate external execution.

