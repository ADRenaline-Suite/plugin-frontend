---
name: front-help
description: "ADRenaline. Help: catalog of plugin-frontend (skills, rules, commands)."
---

# Help — ADRenaline Frontend

Print this catalog as the reply. Do not run any skill or command. Do not invent entries that are not listed. If a component was added to the plugin and is missing here, add one line from its frontmatter `description` and say the catalog was refreshed.

When this help command is the first command in the message, every command, skill, or rule named after it is the subject of the help. Do not run those names. Do not print the full catalog. For each name, in the order given, print its catalog line (the linked id and the sentence). When the README has a heading for that command, also print the paragraphs under that heading, up to the next heading. A skill name uses the skill's catalog line and the README group that names that skill, up to its first command heading. A name that is not in this catalog is one line: it is not in this plugin. Do not invent what it does, and do not write a file.

Write the sentences in the language of the request. Keep command names, file ids, and every URL unchanged. Every id is a markdown link to the GitHub URL on its line. Do not print a repository `name` as the visible label of a plugin.

Keep the section headings, in this order: Plugin, Commands, Skills, Rules, then Agents, Hooks, and MCP when the plugin has them, then Output, then Not in this plugin. The title and the Plugin line show `ADRenaline` plus the `displayName`, then one sentence on what the plugin does. Under Commands, group the lines by the skill named in the line. Each group opens with that skill name linked to its SKILL.md. One line per item: the linked id, then the sentence. Output links this plugin's GitHub repository under that same label. A plugin under Not in this plugin uses `ADRenaline` plus its short name, and links to `https://github.com/<owner>/<other-plugin>` only when that repository exists.

## Plugin

- [**ADRenaline Frontend**](https://github.com/ADRenaline-Suite/plugin-frontend/blob/main/README.md) — Implements one screen that already has a handoff, copy, and accessibility requirements.

## Commands

- [**/front-help**](https://github.com/ADRenaline-Suite/plugin-frontend/blob/main/README.md) — This help (one-line catalog of the plugin).
- [**implement-interface**](https://github.com/ADRenaline-Suite/plugin-frontend/blob/main/skills/implement-interface/SKILL.md) — Implements one screen from a handoff: its structure, its states, and its vitals budget.
- [**/front-structure**](https://github.com/ADRenaline-Suite/plugin-frontend/blob/main/skills/implement-interface/references/structure.md) — Structure: the regions and components the handoff already named.
- [**/front-states**](https://github.com/ADRenaline-Suite/plugin-frontend/blob/main/skills/implement-interface/references/states.md) — States: loading, empty, error, success, and the states the handoff adds.
- [**/front-vitals**](https://github.com/ADRenaline-Suite/plugin-frontend/blob/main/skills/implement-interface/references/vitals.md) — Vitals budget: LCP, INP, and CLS for this screen, mobile and desktop apart.

## Skills

- [**implement-interface**](https://github.com/ADRenaline-Suite/plugin-frontend/blob/main/skills/implement-interface/SKILL.md) — Implements one screen from a handoff: its structure, its states, and its vitals budget.

## Rules

- [**output-folder**](https://github.com/ADRenaline-Suite/plugin-frontend/blob/main/rules/output-folder.mdc) — Every file goes in `adrenaline/frontend/` (or in `outputDirs["plugin-frontend"]` of `.cursor/adrenaline.json`). The artifact follows the language of the request.
- [**handoff-before-code**](https://github.com/ADRenaline-Suite/plugin-frontend/blob/main/rules/handoff-before-code.mdc) — No screen is coded without a handoff, interface copy, and accessibility requirements. The visual design stays in its plugin.

## Output

- Repository: [**ADRenaline Frontend**](https://github.com/ADRenaline-Suite/plugin-frontend).
- Folder: `adrenaline/frontend/`. One named subject goes in `<subject>/`. `<NNN>` is monotonic across the whole folder.

## Not in this plugin

- Handoff and visual design → [**ADRenaline plugin-ui-ux-design**](https://github.com/ADRenaline-Suite/plugin-ui-ux-design).
- Interface copy → ADRenaline plugin-ux-writing.
- Accessibility → ADRenaline plugin-accessibility.
- Use case → ADRenaline plugin-project-manager.
