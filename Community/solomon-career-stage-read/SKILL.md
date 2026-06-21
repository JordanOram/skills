---
name: "solomon-career-stage-read"
description: "Classify a Solomon client's role, career stage, bottleneck, strongest proof, missing proof, and recommended support function. Use for first-cohort DP/cinematographer reads and support-map prep."
compatibility: "Created for Zo Computer"
metadata:
  author: "solomonos1.zo.computer"
  category: Solomon
---

# Solomon Career Stage Read

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

Use this skill to produce the first clean read on a client before a support map or intro rationale is drafted.

The read is not a personality profile. It is an operating read: where they are, what proof they have, what is missing, and which support function should help first.

## Inputs

Collect only what is needed:

- name
- primary role
- market / geography
- years or career arc
- top credits / strongest projects
- reel, site, IMDb, social, or portfolio links if available
- current ambition
- current constraints
- current representation
- strongest trusted relationships
- sensitive exclusions

If information is missing, say so. Do not invent proof.

## Career stages

Use the active canon stage model:

1. **0 → 1: identity and first proof** - talented but not yet legible.
2. **1 → 2: proof into momentum** - credible work exists, but momentum is not repeatable.
3. **2 → 5: momentum into demand** - working and credible, but not yet strongly pulled by the market.
4. **5 → retirement: demand into infrastructure and legacy** - established, high-signal, reputation-rich, operationally exposed.

## Output format

```markdown
# career stage read - [client]

## role
[primary creative role + adjacent roles]

## current stage
[0→1 / 1→2 / 2→5 / 5→retirement]

## stage evidence
- [specific proof]
- [specific proof]
- [specific proof]

## current ambition
[what they are trying to move toward]

## strongest proof
[the strongest credible signal already present]

## missing proof
[what would make the next stage believable]

## bottleneck
[one bottleneck, not a list]

## recommended support function
[one of: opportunity, representation, money, reputation, assets, legal / rights, network, operations]

## what could be wrong
[uncertainty, missing context, or possible misread]

## next useful move candidate
[one candidate move, clearly marked unapproved]

## approval state
operator review required before client-visible use
```

## Rules

- One bottleneck beats five insights.
- Use the client's language where possible.
- Tie every read to evidence.
- If the relationship path is unclear, say `no known path`.
- Do not recommend outreach until the support map and intro rationale include provenance and consent state.
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

