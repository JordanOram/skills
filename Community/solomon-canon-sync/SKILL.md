---
name: "solomon-canon-sync"
description: "Propagate Solomon (the product) identity from CANON.md out to every downstream record so they never drift. Use when Jordan updates what Solomon IS (category, wedge, the wheel, phase line, north star, hosting model, positioning), when he says \"sync the canon\" / \"update all records\" / \"propagate this\", or on the nightly Solomon Records Sync automation. Solomon = the product. (Zolomon = the persona; that is a different skill: zolomon-persona-sync.)"
compatibility: "Created for Zo Computer"
metadata:
  author: "solomonos1.zo.computer"
---

# Solomon Canon Sync

Keep every record that describes **Solomon the product** reconciled to one source of truth, automatically.

## The model

`CANON.md` is the **only** source of truth for what Solomon is. Everything else is **downstream** and gets reconciled *to* CANON. Records never edit CANON; CANON flows outward to them.

```
                 CANON.md  (source of truth)
                     │  propagate outward
   ┌─────────┬───────┼────────┬─────────────┐
 root      repo    repo    persona ref   satellite
AGENTS.md AGENTS.md CLAUDE.md   doc        visions
```

**Source of truth:**
`Once & For All/Solomon/docs/CANON.md` - specifically the dated repositioning banner at the top. The newest dated banner wins over everything below it and over every downstream record.

**Downstream targets (reconcile these TO canon, in order):**
1. `AGENTS.md` (root) - `Right Now` + `Business State → Solomon` + Language Conventions + rule-of-thumb + Reference Docs table
2. `Once & For All/Solomon/AGENTS.md` - active product frame block
3. `Once & For All/Solomon/CLAUDE.md` - identity/spine block
4. `Once & For All/Solomon/prompts/zo/solomon-cofounder-persona-v1.md` - Mission + Current Build Discipline (product-facing facts only; voice is owned by zolomon-persona-sync)
5. `Once & For All/Solomon/docs/VISION.md` and any `*vision*.md` satellites - flag if conflicting; do not silently rewrite vision prose, add a one-line "superseded by CANON YYYY-MM-DD" banner instead

## Procedure

1. **Read the canon banner.** Extract the current locked facts: category, one-sentence frame, the wheel (Set Up → Get Work → Stay Visible → Operate → Grow), day-one surface, phase-two line, north star, hosting model, company frame, external line, banned framings.

2. **Diff each downstream target** against those facts. Look for: old headline spine ("inbound text → propose intro → dispatch" as THE product rather than phase-two), retired category language, stale north-star numbers, retired stat combos (570K/90%), lab/portfolio/holding-company framing, anything contradicting the newest banner.

3. **Auto-edit** each drifted target with `edit_file_llm`, surgical changes only. Preserve unrelated content. Use `// ... existing code ...` placeholders. Do NOT rewrite whole files.

4. **Never invent.** If canon is silent on something, leave the downstream text alone. Only reconcile genuine conflicts with the banner.

5. **Stamp** root `AGENTS.md` `Last verified:` to today's date when run.

6. **Report** a short diff list: file → what changed. If nothing drifted, say "all records already match CANON (dated banner YYYY-MM-DD)" and stop.

## Guardrails

- CANON is read-only here. If Jordan wants to change what Solomon IS, he edits CANON (or tells you to), then this skill propagates it. Never edit CANON inside this skill.
- Voice/tone/persona facts are out of scope - that's `zolomon-persona-sync`. This skill touches the persona doc ONLY for product-fact corrections (e.g. the wheel), never voice.
- External-action guard still applies: this only edits internal records. No commits, no pushes, no public pages without Jordan's say-so.
## MCP Power Layer

These skills are the judgment layer. MCPs and integrations are the hands. Use them when they give Solomon real access, durable records, or live operating context. Do not use an MCP just to look sophisticated.

### Preferred connectors

- GitHub integration for docs branches, diffs, commits, and pull requests when canon lives in a repository.
- Notion MCP or Notion integration if any public-facing or internal wiki mirrors the canon.
- Google Drive for exported docs, decks, PDFs, or shared reference material that must be checked for stale language.
- Linear MCP or Linear integration for creating cleanup tasks when downstream systems need manual follow-through.

### Use MCP when

- canon changes must be propagated across repos, docs, decks, or operating systems.
- the skill needs a verifiable diff trail instead of a conversational summary.

### Fallback if unavailable

Patch workspace files directly and produce a diff summary. If external docs cannot be accessed, list them as follow-up targets instead of assuming sync is complete.

### Confirmation gates

Ask Jordan before using any connector to:

- send emails, DMs, SMS, or public posts.
- publish, deploy, merge, delete, or overwrite public or production surfaces.
- buy domains, change DNS, rotate secrets, modify billing, or create payment links.
- write private relationship intelligence into a public or shared system.
- commit Jordan, Once & For All, Solomon, or a client to an external obligation.

If the connector is not connected, say so plainly and either use the fallback or surface the correct connect path. Do not simulate external execution.

