<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="README.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

# Frontend (`plugin-frontend`)

Implements one screen from a handoff, with its states and a Core Web Vitals budget. The framework is the one the project already uses.

The instructions are in English. The file the plugin saves follows the language of the request. Files go in `adrenaline/frontend/`.

## /front-structure

The regions the handoff already named, using the project's component library.

## /front-states

Loading, empty, error, and success. On error, what the person typed stays.

## /front-vitals

LCP, INP, and CLS targets at the 75th percentile, mobile and desktop apart. A number nobody measured stays a gap.

## Help

## /front-help

The catalog of this plugin. It does not write a file.

## Who it is for

Someone who is building a screen that already has a handoff, interface copy, and accessibility requirements. The handoff stays with `plugin-ui-ux-design`. The words stay with `plugin-ux-writing`. The audit stays with `plugin-accessibility`. This plugin does not copy their skills.

## What it includes

Portable, for any agent that follows [Agent Skills](https://agentskills.io/specification):

- `implement-interface` implements the structure, the states, and the vitals budget.

Cursor and Claude Code: the commands above. In Cursor, `/front-structure`. In Claude Code, `/plugin-frontend:front-structure`.

Cursor only: rules `output-folder`, `handoff-before-code`. Claude Code does not load rules. The same restrictions are in the skills.

## Install

In Cursor, install the plugin from this repository in Customize.

In Claude Code:

```text
claude plugin marketplace add ADRenaline-Suite/plugin-frontend
claude plugin install plugin-frontend@plugin-frontend
```

To try a local copy, start Claude Code with `claude --plugin-dir <path to this repository>`.

## Example

Ask `/front-states` and name the screen. The record lists the four states. `references/angular.md` is read only when the project already has Angular. Taiga UI is used only when the project already depends on it.

## Configuration

The numbered record goes in `adrenaline/frontend/`. The screen code stays in the project's source tree. One named app goes in `<subject>/`.

## License

MIT. Copyright (c) 2026 Ricardo Plascencia.

