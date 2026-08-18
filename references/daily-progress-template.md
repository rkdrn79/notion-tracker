# Daily research progress template

Maintain one entry per project and user-local calendar date. Upsert the existing entry instead of creating one page per agent session.

## Page structure

~~~markdown
## Focus
The concrete research outcome intended for today.

## Completed
- Verified completed work with links.

## Observed
- Direct observations from inspected results, scheduler state, tests, or sources.
- Include units, aggregation, and evidence grade for quantitative statements.

## Interpreted
- What the observations may mean.
- Mark alternatives and uncertainty.

## Paper Impact
- Exact sections, paragraphs, claims, figures, tables, or conclusions strengthened, weakened, contradicted, added, or unchanged.

## Decisions
- Material decisions and rationale, linked to Research Decisions.

## Blockers
- What prevents the next inference or experiment.

## Next
- Concrete actions with clear completion conditions.

<details>
<summary>재현 정보 — 에이전트와 실행 담당자용</summary>
	- 코드 버전:
	- 실행 작업:
	- 결과 또는 보고서:
	- 문서 또는 인용:
</details>
~~~

## Capture rules

- Keep Completed separate from Observed; running a job is not a finding.
- Keep Observed separate from Interpreted.
- Record failed or inconclusive work when it changes next actions.
- Link material observations to Evidence and choices to Research Decisions.
- Use the user's timezone. Ask when a date boundary matters and timezone is unknown.
- Do not expose secrets or full command output.
- Summarize large logs and link their location.
- Keep server paths, commands, hashes, and job identifiers out of the human summary.
- Link the Research Projects advanced today and name the paper sections they unblock.

## Update behavior

1. Fetch the existing entry.
2. Merge new facts into relevant sections.
3. Remove exact duplicates.
4. Preserve human wording and locked blocks.
5. Change the title focus only when the primary objective changes.
6. Verify linked experiments, claims, evidence, and decisions.
