# Research portfolio template

Use this reference only for the workspace root, cross-project management, a new top-level research line, or migration from a redundant nested hub.

## Required hierarchy

```text
Research portfolio page
└── Research portfolio database
    ├── Project A — paper workspace
    │   ├── paper-form content
    │   ├── Research Projects database
    │   ├── Daily Progress database
    │   └── optional collapsed audit databases
    └── Project B — independent paper workspace
        ├── paper-form content
        ├── Research Projects database
        └── Daily Progress database
```

The database record is the project home. Do not insert a second generic HQ page between the portfolio record and the paper.

## Portfolio page reading order

1. A linked Gallery view of the research portfolio database, with one research line per card.

Do not add anything else to the main page by default. Keep instructions, papers, ideas, status dashboards, and archived structures elsewhere.

Place active cross-project Papers and Ideas databases on a separate top-level shared-assets page. They are working research assets, not migration debris.

## Human portfolio fields

Keep these properties visible in the default management views:

- `Research` or the workspace's human title property
- `Target conference`
- `Start date`
- `Last updated`
- `Priority`

Use the workspace's established language and property names. Do not carry old relations, summaries, next actions, blockers, stages, stable keys, or technical links into the visible portfolio schema.

## Required view

- **Research portfolio:** one Gallery view whose cards show the five human fields above. Keep the source database on a separate private data page so the main page contains only the Gallery.

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
6. Move the old portfolio database and redundant intermediate HQ to a recoverable private archive. Move active Papers and Ideas databases to a separate top-level shared-assets page instead of archiving them. Permanently delete only after explicit confirmation and only when the connector supports it safely.
