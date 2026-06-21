---
name: "solomon-intro-rationale-builder"
description: "Build one provenance-backed Solomon intro or action rationale with consent requirements, confidence, risk, and client/operator approval copy."
compatibility: "Created for Zo Computer"
metadata:
  author: "solomonos1.zo.computer"
  category: Solomon
---

# Solomon Intro Rationale Builder

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

Use this skill to turn a proposed move into a trust-safe rationale.

Hard rule: no provenance, no recommendation.

## Required inputs

- client
- proposed recipient or bridge person
- target room / opportunity / action
- relationship path
- source evidence
- recency
- uncertainty
- consent state
- support map context

## Output format

```markdown
# intro rationale - [client] → [recipient/target]

## proposed move
[one action only]

## relationship_path
[client → bridge → recipient, or `no known path`]

## source_evidence
- [source / fact / date]
- [source / fact / date]

## recency
[fresh / dated / unknown + reason]

## confidence
[high / medium / low]

## why_now
[why this move matters now]

## value_for_client
[what the client gains]

## value_for_recipient
[why the recipient is not being used as a favour machine]

## what_could_be_wrong
[trust risk, weak path, stale info, mismatch, sensitive context]

## consent_required
[client approval / recipient double opt-in / Jordan-operator review]

## client-facing approval copy
[short copy asking the client to approve, edit, or decline]

## bridge ask draft
[only if consent allows drafting; never send automatically from the skill]

## operator note
[private judgement and handling instructions]
```

## Confidence rules

- **High:** direct relationship, recent evidence, clear mutual value, no sensitive context.
- **Medium:** plausible relationship path, some evidence, some uncertainty, needs operator judgement.
- **Low:** weak path, stale evidence, unclear benefit, or sensitive context.

Medium and low confidence require Jordan/operator review.

## Rules

- One rationale per move.
- Do not stack multiple intros.
- Do not overstate closeness.
- Do not expose sensitive client context.
- Do not imply representation, employment, or availability unless verified.
- If consent is missing, output the consent gap before the draft.
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

