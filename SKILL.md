---
name: notion-track-research
description: Build and maintain a multi-project Notion research portfolio whose project pages are paper workspaces that follow real paper sections and contain enough reasoning, evidence, and section-level prose for a human to write each manuscript from Notion alone. Use when an agent needs to initialize or revise the research portfolio or a paper, create an independent project home for a new research line, connect claims that require experiments, analysis, proof, or literature checks to research project pages, track those projects, capture daily paper progress, or audit missing support. Keep technical provenance available but out of the main reading path; never turn a paper page into a database dashboard or a mirror of server directories.
---

# Track Research as a Paper Workspace in Notion

Make the Notion page sufficient for a researcher to understand and write the paper without opening a terminal or reconstructing the argument from project files.

## Core contract

- Treat the workspace root as one **Research Space** with three separate linked Galleries: Research Projects, Papers, and Ideas. Each project card is one independent **paper workspace**.
- Make the portfolio record itself the research home. Opening it must lead directly to the paper, not through a redundant intermediate HQ.
- Treat each project home as the canonical paper workspace: it follows the final paper's section order and contains the full argument, section intent, claims, current evidence, and missing support.
- Write enough connected prose and structured detail that the manuscript can be drafted from Notion alone.
- When a statement needs an experiment, analysis, proof, figure, or literature check, link a research project page immediately beside that statement.
- Make every research project page explain why the paper needs it, what would count as an answer, and how each outcome changes the relevant section.
- Put one compact project-local Daily Progress calendar at the very top of the project home. Keep the Research Projects database and full database links as supporting navigation after the paper content.
- Keep code, commands, commits, jobs, storage paths, and raw artifacts in Git or their original systems. Put compact provenance in a collapsed technical section or hidden database properties.
- Preserve negative results, contradictions, uncertainty, alternative explanations, and limitations.
- Never invent metrics, job state, citations, or completion.

## Human surface versus agent metadata

### Human surface

Use the reader's language and ordinary research terms. Show:

- the problem and why it matters;
- what is already known;
- the unresolved question;
- the paper's explanation or hypothesis;
- the sequence of supporting research projects and why each is necessary;
- what has actually been learned;
- what remains unknown;
- the current conclusion and its limits.

### Agent metadata

Stable keys, branch names, commits, job IDs, configuration paths, and artifact locations support reliable updates. Do not place them in paper prose, research-project titles, or default human views. Keep them in hidden properties or a collapsed `재현 정보` section.

Do not expose local absolute paths, server directory trees, shell commands, hashes, or storage plumbing unless the user explicitly asks. Prefer a clickable report, paper, figure, or repository link. If no friendly link exists, describe the source in plain language and retain the exact path only in technical metadata.

## Required references

- Read `references/paper-flow-template.md` before creating or rewriting the paper workspace.
- Read `references/research-project-page-template.md` before creating or materially updating a research project page.
- Read `references/notion-schema.md` before creating or repairing databases and views.
- Read `references/daily-progress-template.md` before writing daily progress.
- Read `references/write-policy.md` before every Notion write or schema change.
- Read `references/research-portfolio-template.md` before creating, migrating, or restructuring the workspace root or adding a new top-level research project.

## Establish context

1. Locate the project and read applicable agent instructions.
2. Identify the authoritative research outline, specifications, reviewed result summaries, decisions, and current Git state.
3. Search Notion for the research portfolio and an existing project home before creating anything.
4. Fetch the portfolio, project home, experiment pages, and relevant database schemas before editing.
5. If multiple portfolios or project homes remain plausible, ask the user to choose. Never create a parallel portfolio or hub by guessing.
6. If Notion is unavailable, return a structured dry run and say that nothing was written.

Prefer research summaries and manifests to raw logs. Do not crawl large artifact trees without a concrete need.

## Unified multi-project research space

Keep the root visually simple and useful: under the minimal headings `Research Projects`, `Papers`, and `Ideas`, show exactly three separate linked Notion databases in Gallery views. Do not add an explanatory callout, field guide, status dashboard, board, table, linked summary views, or “what to look at” section unless the user explicitly asks.

Keep Papers and Ideas as distinct Galleries. Group both Galleries by one single-select `Big Area` property whose values are broad research families, not narrow method tags. Use this default vocabulary unless the workspace already has a deliberate equivalent: `World Models`, `MLLM`, `Generative Modeling`, `Continual Learning`, `Robotics`, `Representation Learning`, `Other`. Do not create database records, gallery cards, or intermediate pages for these broad areas.

Also keep a `Related Areas` multi-select for finer tags such as JEPA, replay, online adaptation, evaluation, or other workspace-specific topics. Show both `Big Area` and `Related Areas` on Paper and Idea cards. Each record gets exactly one best-fit Big Area and may get multiple Related Areas. Keep all three source databases on the private data page; the root contains only their linked Gallery views.

The default portfolio table shows only the human project title, target conference, start date, last update, and priority. Do not add paper relations, research summaries, next actions, blockers, stage, repository paths, or stable keys to the visible portfolio schema. Prefer a fresh minimal database over carrying legacy properties and views into the main surface; move the old database to a recoverable archive after migrating its project pages.

Create one portfolio record per independent paper or research line. Inside that record, create project-local Research Projects and Daily Progress databases. Do not mix the support tasks or daily logs of unrelated papers into one shared table.

When migrating an older nested structure, promote the existing portfolio record into the paper workspace, move its child databases under it, verify the new hierarchy, and archive the redundant intermediate page. Preserve recoverability unless the user explicitly confirms permanent deletion.

## Default project-home architecture

Create or maintain this reading order:

1. **Daily Progress calendar** — one project-local calendar linked to the daily database, with the date as its calendar field.
2. **한눈에 보는 논문** — question, answer so far, status.
3. **논문 본문** — Abstract, Introduction, Related Work, Research Question, Method, Experiments, Results, Discussion, Limitations, and Conclusion in the project's appropriate order.
4. **본문 속 연구 프로젝트 링크** — experiments, analyses, proofs, figures, and literature checks placed beside the content they support.
5. **현재 결론과 남은 질문** — evidence-calibrated ending and unresolved writing inputs.
6. **연구 운영** — Research Projects, Daily Progress, decisions, and optional audit indexes.

The Daily Progress calendar is the only database view allowed before the paper. Do not lead with schema explanations, stable keys, repository state, a table of contents, or any other linked database.

## Write the paper in paper form

1. Reconstruct the beginning-to-end argument from authoritative sources.
2. Organize it under real paper headings. Combine or rename sections to match the venue or project, but do not replace them with a generic dashboard.
3. For every section, include the section's purpose, the argument it must make, the evidence currently available, and the prose or bullet structure needed to draft it.
4. Write connected prose rather than a checklist of labels such as Phenomenon, Gap, and Contribution.
5. Define unavoidable technical terms once in plain language.
6. Include every major story step even when its evidence is missing. Write `아직 확인하지 못했다` or equivalent instead of omitting the step.
7. After a statement that requires support, add a contextual research-project link:

   `이 내용을 뒷받침할 연구 프로젝트: <project page> — 무엇을 확인해야 이 문장을 쓸 수 있는지 한 문장으로 설명한다.`

8. After results exist, write what was observed and how it changes the actual paragraph, figure, result claim, or conclusion. Link the project page for detail.
9. End with the strongest defensible conclusion, serious alternative explanations, limitations, and the next decisive project.

The workspace may contain section-level draft prose, planned figures and tables, result sentences, and citation needs. Do not paste raw logs or duplicate a separately maintained manuscript verbatim. If Notion is the user's chosen writing source, completeness takes priority over artificial brevity.

## Create and update research project pages

Use one database record per unit of support the paper needs: conceptual experiment, analysis, proof, figure/table, literature check, or writing clarification. Runs, orders, and seeds may be subordinate records or technical metadata unless they answer different scientific questions.

For each project:

1. Use a descriptive human title. Keep internal IDs in properties, not the title.
2. Name the exact paper section or statement that needs this work.
3. Explain why the paper cannot make that statement yet.
4. Describe the comparison, proof obligation, literature question, or figure requirement in plain language.
5. State the paper fork: what permits the target sentence, what forces revision, and what remains inconclusive.
6. Separate `관찰한 사실` from `해석`.
7. State the current status in reader language: not started, running, answer available, blocked, or inconclusive.
8. Put metrics in small readable tables only when they help interpretation.
9. Put commit, job, config, command, and artifact details in a collapsed `재현 정보` section or hidden properties.
10. Link the project back into every relevant paper location; a database relation alone is not enough.

## Record daily progress

Maintain one entry per project and local calendar date. Write for a collaborator, not for a scheduler:

- today's research goal;
- what changed in the paper's understanding;
- research projects advanced;
- observed facts versus interpretation;
- blockers and next decisive action.

Keep commits, jobs, and paths in a compact technical footer. Do not make them the daily summary.

Expose the daily database through a calendar linked view at the top of its project home. Keep calendar cards compact: title/focus, goal, manuscript change, and blocker are sufficient by default.

## Record evidence and decisions

- Use evidence records when atomic provenance or contradiction audits are useful; do not force the reader to navigate them to understand the paper.
- Grade evidence as Verified, Cited, Inferred, or Unmeasured.
- Use Context for relevant results that do not decide the main claim.
- Record decisions with context, alternatives, rationale, consequences, and revisit condition.
- Summarize a linked ADR in plain language; do not paste its repository path into the storyline.

## Read before writing and upsert safely

1. Search by project key and stable key.
2. Fetch the exact page and current schema.
3. Preserve human-authored wording and locked blocks.
4. Update the smallest exact region possible.
5. Never replace a storyline silently when evidence changes the thesis; explain the change first unless the user explicitly requested the rewrite.
6. Verify all created or materially changed pages after writing.

## Quality gate

Before completion, read the HQ as a researcher and check:

- Can a person draft every paper section from the HQ without reconstructing missing logic elsewhere?
- Does each unsupported statement link to a research project that can resolve it?
- Does every linked project say exactly which paper text it enables or changes?
- Are missing results stated plainly?
- Are facts and interpretations separated?
- Are jargon, IDs, code paths, server directories, and operational metadata absent from the main reading path?
- Are negative results, alternatives, and limitations visible?
- Do default views use human-readable columns and labels?
- Does the Research Space root contain exactly three separate Gallery views in this order: Research Projects, Papers, and Ideas?
- Do project cards show project, target conference, start date, last update, and priority?
- Are Papers and Ideas kept separate, grouped by one broad Big Area, and still tagged with finer Related Areas?
- Are broad areas values rather than database records or intermediate pages?
- Does each portfolio record open directly into one paper workspace with its own Research Projects and Daily Progress?
- Is the project-local Daily Progress calendar the first content block in every project home?

If any answer is no, revise before reporting completion.

## Completion report

Report the portfolio or paper sections changed, research project pages linked, daily records updated, and writing inputs still unknown. Return the portfolio link and the changed project-home link. Mention technical metadata only when it blocked or materially constrained the work.
