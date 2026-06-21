---
name: "solomon-support-map-builder"
description: "Build the Jordan/operator-authored Solomon support map template for a client. Use after a career-stage read and relationship graph seed exist."
compatibility: "Created for Zo Computer"
metadata:
  author: "solomonos1.zo.computer"
  category: Solomon
---

# Solomon Support Map Builder

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

Use this skill to create the support map artifact that Jordan/operator can approve, edit, or reject.

For the first 0–50 support maps, Solomon templates, pre-fills, stores, and tracks. Jordan/operator writes or approves the judgement.

## Required inputs

- career-stage read
- thin profile
- role and current ambition
- 8-function support sweep if available
- relationship graph seed
- trusted people and sensitive exclusions
- known opportunities or target rooms
- prior outcomes if any

## The 8 support functions

1. opportunity
2. representation
3. money
4. reputation
5. assets
6. legal / rights
7. network
8. operations

## Output format

```markdown
# support map - [client]

## current stage
[stage + one-line read]

## career gap
[highest-leverage missing support]

## strongest proof
[best existing signal]

## missing support function
[one of the 8 functions]

## relevant network nodes
1. [person] - [relationship/context/confidence/consent state]
2. [person] - [relationship/context/confidence/consent state]
3. [person] - [relationship/context/confidence/consent state]

If no real path exists, write: `no known path yet`.

## one proposed move
[exactly one intro/action/review/follow-up]

## evidence
- [source/evidence]
- [source/evidence]
- [source/evidence]

## what could be wrong
[uncertainty or risk]

## client-visible summary
[short, calm, no internal mechanics]

## operator notes
[private judgement, missing data, trust risks]

## approval state
[waiting for Jordan/operator approval / approved / edited / declined]
```

## Rules

- Exactly one proposed move.
- If the support map cannot support a move with evidence, the output is `not enough signal yet`.
- Do not present the map as final truth.
- Do not create a generic dashboard or career report.
- Do not expose support-suite mechanics to the client.
- Every proposed move must feed intro-rationale-builder before any outbound action.
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

