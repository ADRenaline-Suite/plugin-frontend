---
name: implement-interface
description: Implements one screen from a handoff: its structure, its states, and its vitals budget.
---

<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="SKILL.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Frontend](../../README.md)

# Implements one screen from a handoff: its structure, its states, and its vitals budget

The screen that gets built is the screen the handoff names. States are part of the screen, not a follow-up.

Source: Core Web Vitals as published on web.dev (LCP, INP, CLS, 75th percentile). The handoff is the source of layout. Community practice that matches it: semantic elements before ARIA, the project's component library before a new widget, every visible string from the copy, loading empty error and success present before the screen is called done.

## Before writing

1. Read only the reference this command names: [structure](references/structure.md), [states](references/states.md), or [vitals](references/vitals.md).
2. When the project is already Angular, also read [angular](references/angular.md).
3. Stop if the handoff, the copy, or the accessibility requirements are missing.

References: [structure](references/structure.md), [states](references/states.md), [vitals](references/vitals.md).

## Delivery

Code goes in the tree the project already compiles, in the framework that tree already uses. The numbered record goes in the output folder. Do not choose Angular, React, or any other framework.

Every file this skill writes goes in `adrenaline/frontend/`, or in `outputDirs["plugin-frontend"]` when `.cursor/adrenaline.json` gives a valid relative path. If `adrenaline/frontend/` does not exist yet and `frontend/` at the project root already has this plugin's `ORIGIN.json` or `STATUS.md`, keep writing there and say so.

When the person names one project, app, service, or domain, put that subject's file in `<subject>/`. A file about the whole product stays at the output root. `<NNN>` is the next free number in the whole output folder. The `archivo` cell is `<subject>/<file>` when there is a subject (`doc/arch/adr-008-asunto-subcarpeta.md`).

Write `ORIGIN.json` beside `STATUS.md` when the folder is created, and again only if it is missing or a field differs. Fields: `suite` `ADRenaline-Suite`, `plugin` `plugin-frontend`, `repository` `https://github.com/ADRenaline-Suite/plugin-frontend`, `convention` `adr-001`. It is not an `<NNN>` file and it has no row in `STATUS.md`.

Do not invent a fact the person did not give. A required heading with no fact stays a gap and the file stays `proposed`. "None." fills a heading.

## Done

- [ ] Only the reference for this command was applied.
- [ ] The output folder, the subject subfolder, `ORIGIN.json`, and `STATUS.md` match the delivery rules.
- [ ] A missing required fact is a gap. The file stays `proposed`.

## Example

A request that names the piece and its source writes one file. A request missing that source writes nothing and names the gap.
