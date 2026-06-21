---
name: "solomon-outcome-tracker"
description: "Track Solomon state movement after a proposed move, writing outcomes back to the client profile, relationship edge, support map, and future recommendation memory."
compatibility: "Created for Zo Computer"
metadata:
  author: "solomonos1.zo.computer"
  category: Solomon
---

# Solomon Outcome Tracker

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

Use this skill after a proposed Solomon move changes state.

Track movement by state, not volume.

## Canonical states

```text
proposed → approved → bridge ask sent → bridge accepted → intro made → conversation booked → opportunity created → closed / declined / archived
```

## Required inputs

- client
- proposed move
- current state
- new state
- date
- owner
- source evidence
- notes from client / bridge / recipient / operator
- next follow-up date if needed

## Output format

```markdown
# outcome update - [client] - [move]

## state change
[from] → [to]

## date
[YYYY-MM-DD]

## evidence
[source, message, calendar event, operator note, or client confirmation]

## result
[what happened in plain language]

## relationship edge update
[person_a, person_b, state, strength/confidence change, consent state]

## support map update
[what this outcome changes about the map]

## client profile update
[career context learned]

## future recommendation memory
[what Solomon should remember next time]

## next follow-up
[date + owner, or none]
```

## Write-back targets

Every state update should update or prepare updates for:

- client profile
- relationship edge
- support map
- future recommendation memory

## Rules

- If there is no evidence, mark the outcome `unverified`.
- If the move is declined, capture why without arguing.
- If the relationship cools or trust risk appears, lower confidence.
- Do not count a proposed move as useful until it has advanced with consent or created learning.
- The weekly primary metric is clients with one consented useful move advanced this week.
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

