# Angular checklist

<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle"> <a href="angular.es.md"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle"></a></p>

Read this only when `angular.json` or `@angular/core` is already in the project. It does not choose Angular.

- New components are standalone. `ChangeDetectionStrategy.OnPush`. `inject()` in new code.
- New templates use `@if`, `@for`, `@switch`. Do not add `*ngIf` or a new `NgModule`.
- Signals for state that is not an event stream. `HttpClient` lives in a service, not in the template's component logic inline.
- Routes that the project already lazy-loads stay lazy (`loadComponent` or `loadChildren`).
- Use the component library the project already depends on. Taiga UI only when that dependency exists.
- Visible strings and accessible names come from the copy. When the product named `es` and `en`, both entries exist. Do not add a language.
- Do not hand-roll a widget the library already has.

## Done

- [ ] Angular was detected before this file was applied.
- [ ] No new framework and no new UI library.
