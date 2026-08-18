# Notion paper workspace schema

The paper page is primary. Databases exist to resolve and track missing paper support.

## Research Space shared libraries

The Research Space root contains three separate linked Gallery views: Research Projects, Paper Areas, and Idea Areas. Keep their source databases on a private data page.

Both Papers and Ideas require:

| Property | Type | Meaning |
|---|---|---|
| 큰 분야 / Big Area | Select | Exactly one broad family: World Models, MLLM, Generative Modeling, Continual Learning, Robotics, Representation Learning, or Other |
| 관련 분야 / Related Areas | Multi-select | Zero or more finer workspace-specific topics such as JEPA, replay, online adaptation, or evaluation |

Create separate Paper Areas and Idea Areas databases with one page per broad area. Each area database needs only a human title, short description, and numeric display order by default. Inside each Paper Area page, create a linked Table of Papers filtered where `Big Area` equals the page's area. Do the same with Ideas inside each Idea Area page. The Research Space Galleries show these area pages; they do not show individual Paper or Idea records directly.

## Adding a broad area

Treat the Paper and Idea taxonomies as one synchronized vocabulary. Before adding an option, fetch both asset schemas and query both area databases. Reuse an existing canonical label when the candidate differs only by case, spacing, abbreviation, or singular/plural form.

For a genuinely new field-level family:

1. Alter both `Big Area` selects to include the new value while retaining every existing option and color.
2. Add matching Paper Area and Idea Area records with the next numeric order.
3. Create a Table inside each new card using an exact `Big Area = new value` filter against the corresponding asset database.
4. Match the visible columns and sort order used by existing area cards.
5. Update the triggering Paper or Idea records, then verify both schemas, both cards, and both filtered views.

Do not use this workflow for narrow topics; add those only to `Related Areas`.

## Required structure

1. One paper HQ following real paper sections.
2. One Research Projects database.
3. One Daily Progress database.

Research Decisions is recommended. Evidence and Paper Claims are optional audit indexes and should not interrupt the paper.

## Research Projects

One record represents one experiment, analysis, proof, figure/table, literature check, or writing clarification.

| Property | Type | Meaning |
|---|---|---|
| 연구 프로젝트 | Title | Human-readable unanswered question |
| 유형 | Select | 실험, 분석, 이론 검증, 문헌 확인, 그림/표, 글쓰기 |
| 관련 논문 섹션 | Multi-select | 초록, 서론, 관련 연구, 연구 질문, 방법, 실험, 결과, 논의, 한계, 결론 |
| 사람이 보는 상태 | Select | 아직 시작 안 함, 진행 중, 답을 얻음, 막힘, 결론 불가, 중단 |
| 논문에서 필요한 이유 | Rich text | Why the paper cannot finalize the content yet |
| 현재 답 | Rich text | One readable sentence; say when unknown |
| 논문에 반영할 내용 | Rich text | Exact paragraph, claim, figure, or table impact |
| 다음 행동 | Rich text | Concrete completion condition |
| 이야기 순서 | Number | Order in the paper argument |

Keep Stable Key, internal ID, branch, commit, config, job, dates, raw metrics, artifact location, and audit relations as hidden technical properties.

Default views: `논문 이야기 순서`, `지금 할 프로젝트`, `답을 얻은 프로젝트`.

## Daily Progress

| Property | Type | Meaning |
|---|---|---|
| 날짜와 초점 | Title | Date plus readable paper focus |
| 날짜 | Date | User-local date |
| 오늘의 목표 | Rich text | Intended research or writing outcome |
| 달라진 논문 내용 | Rich text | Sections, claims, figures, or conclusions changed |
| 관련 논문 섹션 | Multi-select | Paper sections advanced today |
| 연구 프로젝트 | Relation | Research Projects advanced today |
| 새롭게 이해한 것 | Rich text | Observations and interpretation in readable form |
| 막힌 점 | Rich text | Current blockers |
| 다음 결정적 행동 | Rich text | Next action that changes paper evidence |

Keep Stable Key, commits, jobs, and technical references hidden. Default views: `최근 진행`, `달력`, `막힌 날`.

## Stable identity

Use hidden Stable Key properties for safe upserts. Never put stable keys or internal IDs in human titles or prose.

## Bootstrap order

1. Write the paper HQ sections first.
2. Create Research Projects and Daily Progress.
3. Create project pages for every experiment, analysis, proof, figure/table, or citation need already present in the paper.
4. Insert real project page mentions beside the relevant paper statements.
5. Add compact database views after the paper.
6. Fetch the HQ and project pages and verify that the paper is understandable without opening technical sources.
