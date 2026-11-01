# Lista Angular

<p align="right">Idioma:&emsp;<a href="angular.md"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle"></p>

Lee esto solo cuando `angular.json` o `@angular/core` ya están en el proyecto. No elige Angular.

- Los componentes nuevos son standalone. `ChangeDetectionStrategy.OnPush`. `inject()` en código nuevo.
- Las plantillas nuevas usan `@if`, `@for`, `@switch`. No añadas `*ngIf` ni un `NgModule` nuevo.
- Signals para el estado que no es un flujo de eventos. `HttpClient` vive en un servicio, no inline en la lógica del componente.
- Las rutas que el proyecto ya carga en diferido siguen así (`loadComponent` o `loadChildren`).
- Usa la biblioteca de componentes de la que el proyecto ya depende. Taiga UI solo cuando esa dependencia existe.
- Las cadenas visibles y los nombres accesibles salen del texto. Cuando el producto nombró `es` y `en`, existen las dos entradas. No añadas un idioma.
- No fabriques un widget que la biblioteca ya tiene.

## Done

- [ ] Se detectó Angular antes de aplicar este archivo.
- [ ] Ningún framework nuevo y ninguna biblioteca de UI nueva.
