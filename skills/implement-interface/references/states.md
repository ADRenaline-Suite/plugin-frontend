# States

<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="states.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Frontend](../../../README.md)

Only the happy path is built, so the first failure has no screen.

## Steps

1. Include loading, empty, error, and success even when the handoff only drew the happy path. Say they were added because a screen is not delivered without its states.
2. On error, keep what the person typed.
3. Permission denied, offline, and validation are included when the handoff or the use case names them. Do not invent a state to look thorough.
4. The words of each state come from `plugin-ux-writing`.

## Rules

1. Do not clear the form when the error is shown.

## Template

## Screen

## Loading

## Empty

## Error

## Success

## Other states

## Assumed

## Done

- [ ] The use case or the source this piece requires is named, or the file was not written.
- [ ] Every heading above is filled or marked as a gap. `proposed` when a gap remains.
- [ ] Nothing was invented: no field, no error, no date, no role, no legal basis.
- [ ] The subject folder and `STATUS.md` follow the skill.

Close the reply with what was written, where, and what is still a gap.
