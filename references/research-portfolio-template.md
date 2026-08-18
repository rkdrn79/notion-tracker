# Research portfolio template

Use this reference only for the workspace root, cross-project management, a new top-level research line, or migration from a redundant nested hub.

## Required hierarchy

```text
Research Space page
├── Research Projects Gallery
│   └── Research portfolio database
│       ├── Project A — paper workspace
│       │   ├── paper-form content
│       │   ├── Research Projects database
│       │   ├── Daily Progress database
│       │   └── optional collapsed audit databases
│       └── Project B — independent paper workspace
├── Papers Gallery — grouped by Big Area
└── Ideas Gallery — grouped by Big Area
```

The database record is the project home. Do not insert a second generic HQ page between the portfolio record and the paper.

## Portfolio page reading order

1. `Research Projects` — a linked Gallery of the research portfolio database, with one research line per card.
2. `Papers` — a separate linked Gallery grouped by `Big Area`.
3. `Ideas` — a separate linked Gallery grouped by `Big Area`.

Do not add anything else to the main page by default. Keep instructions, status dashboards, archived structures, and source databases elsewhere.

Keep Papers and Ideas as separate databases and separate Galleries. Give both a single-select `Big Area` and a multi-select `Related Areas`. Group each Gallery by Big Area, while displaying the finer Related Areas on its cards.

Use genuinely broad Big Area values by default: `World Models`, `MLLM`, `Generative Modeling`, `Continual Learning`, `Robotics`, `Representation Learning`, and `Other`. Assign exactly one best-fit Big Area to each Paper or Idea. Use Related Areas for narrower concepts such as JEPA, replay, online adaptation, or evaluation. Do not create a Research Areas database, area cards, or area pages merely to implement grouping.

## Human portfolio fields

Keep these properties visible in the default management views:

- `Research` or the workspace's human title property
- `Target conference`
- `Start date`
- `Last updated`
- `Priority`

Use the workspace's established language and property names. Do not carry old relations, summaries, next actions, blockers, stages, stable keys, or technical links into the visible portfolio schema.

## Required views

- **Research Projects:** Gallery cards show the five human fields above.
- **Papers:** Gallery grouped by Big Area; cards show title, Big Area, Related Areas, classification, year, authors, reading state, and one-line summary when those fields exist.
- **Ideas:** Gallery grouped by Big Area; cards show title, Big Area, Related Areas, state, rationale, and date when those fields exist.

Keep all source databases on a separate private data page so the Research Space contains only linked Galleries and their three minimal headings.

## Bootstrap a new project home

1. Create one record in the research portfolio database.
2. Fill the target conference, start date, last update, and priority. Use `미정` instead of inventing a venue.
3. Create project-local Research Projects and Daily Progress databases using `notion-schema.md`.
4. Put a linked Daily Progress calendar at the very top of the record body.
5. Write the rest of the record body in paper form using `paper-flow-template.md`.
6. Add optional Claims, Evidence, and Decisions only when auditability warrants them; place them after the human surface or in a collapsed section.
7. Link unsupported paper statements to the project-local Research Projects pages.
8. Verify that the portfolio record opens directly to the paper and that its child databases have the correct ancestor.

## Safe migration from a nested hub

1. Fetch the portfolio database, project record, intermediate HQ, and every child database.
2. Create a fresh five-field portfolio database when the old database carries unwanted properties or views.
3. Move the project record and child databases into the new hierarchy.
4. Copy the paper-form content into the project record and put its Daily Progress calendar first.
5. Verify paper sections, links, relations, visible fields, and database ancestors.
6. Create and verify the three linked Galleries on the Research Space before archiving any redundant shared-assets page or intermediate HQ.
7. Move old views and legacy portfolio structures to a recoverable private archive, but keep the active Papers and Ideas source databases on the private data page. Permanently delete only after explicit confirmation and only when the connector supports it safely.
