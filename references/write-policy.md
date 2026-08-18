# Notion research write policy

Read this before any Notion write, bulk synchronization, or schema change.

## Source-of-truth boundaries

| Information | Source of truth | Notion treatment |
|---|---|---|
| Paper content and section-level prose | Notion paper workspace | Keep enough content to draft the manuscript from Notion alone |
| Final formatted manuscript, code, and raw artifacts | Git or their original systems | Link or summarize; do not paste raw operational material into the paper page |
| Code and configuration | Git | Store commit and safe paths |
| Raw results, logs, checkpoints | Artifact storage | Store summaries and links |
| Paper storyline and current answer | Research Paper HQ | Write for human readers and update from reviewed evidence |
| Experiment index and verdict | Notion plus source artifacts | Verify before updating |
| Research decisions | Notion and repository ADRs | Link and preserve history |
| Daily progress | Notion | One record per project and local date |

Do not implement automatic two-way synchronization between Notion and manuscript files.

## Evidence grades

- Verified: directly inspected in a result, test, artifact, scheduler response, or reproducible source.
- Cited: supported by a linked or precisely identified source.
- Inferred: a reasoned interpretation not directly measured; state premises.
- Unmeasured: required information is absent or not evaluated.

Never upgrade Inferred or Unmeasured because it fits the preferred story.

## Idempotent upserts

Search by Stable Key before creation. Update one exact match. If several matches exist, stop and report duplicates.

- Daily: one per project and date.
- Experiment: prefer an explicit study, run, job, or manifest ID.
- Claim: use durable human-readable IDs.
- Evidence: use source-scoped deterministic IDs.
- Decision: prefer an ADR ID, otherwise stable date and slug.
- Broad area: one `area:<kebab-case-slug>` record in Paper Areas and one in Idea Areas; both records must share the same key.

Do not use titles alone as identifiers. For legacy area cards that have no Stable Key, match a unique normalized canonical title once, backfill the key, and use only the key for later upserts. If normalization finds multiple candidates, stop and report the duplicates.

## Write authorization

- Write when the user explicitly asks to create, update, log, sync, or record and the target is unambiguous.
- Keep audits and status questions read-only unless changes are requested.
- Ask before creating a parallel hub, choosing among parents, changing an incompatible schema, replacing the central thesis, or editing locked content.
- Preserve compatible custom properties and views during schema repair.

## Read-before-write procedure

1. Search for target hub and Stable Key.
2. Fetch destination database or data source and inspect schema.
3. Fetch an existing page before changing it.
4. Use exact, narrow edits where supported.
5. Create database-backed pages under the confirmed data source.
6. Verify with a fetch or search after writing.

Tool names vary by host. Use the available Notion search, fetch, create, update, relation, or view capability. Do not invent an unavailable tool.

## Content safety

- Never store credentials, tokens, private keys, cookies, or secret environment values.
- Remove secrets from copied commands and logs.
- Do not paste large logs, binary data, checkpoints, or full result tables.
- Preserve human context, negative results, contradictions, canceled work, and superseded decisions.
- Use the user's local timezone for daily records.

## Human-readable surface

- The HQ must contain enough section-level reasoning, prose, result placeholders, figure/table plans, and citation needs to draft the paper without repository access or database navigation.
- Use the user's language unless a project convention says otherwise.
- Explain internal arm names, metrics, and model jargon before using them.
- Never show local absolute paths, server directories, raw shell commands, or hashes in the storyline or default views.
- Keep technical provenance in hidden properties or a collapsed reproduction section.
- Prefer a real Notion page mention or friendly web link over a raw identifier.
- Database relations do not replace contextual Research Projects page links beside the paper statement they support.

## Partial failure

1. Stop before unrelated changes.
2. Identify successful objects.
3. Verify existing state.
4. Report missing relations, properties, views, or records.
5. Resume from verified state; do not replay the full bootstrap blindly.

For a broad-area update, reconcile the two select options, two keyed area cards, and two filtered views independently. Assign triggering records last. Preserve successful objects and repair only missing or incorrect pieces; never use destructive rollback for a partially completed taxonomy update.

If Notion tools are unavailable, return a dry-run payload with intended target, records, stable keys, relations, and evidence grades.

## Completion report

Report created and updated objects, skipped duplicates, ambiguities, partial failures, direct links, and items still Inferred or Unmeasured. Do not claim synchronization until records are verified.
