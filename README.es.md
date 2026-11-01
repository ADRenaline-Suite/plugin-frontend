<p align="right">Idioma:&emsp;<a href="README.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

# Frontend (`plugin-frontend`)

Implementa una pantalla desde un handoff, con sus estados y un presupuesto de Core Web Vitals. El framework es el que el proyecto ya usa.

Las instrucciones están en inglés. El archivo que guarda el plugin sigue el idioma del pedido. Los archivos van en `adrenaline/frontend/`.

## /front-structure

Las regiones que el handoff ya nombró, con la biblioteca de componentes del proyecto.

## /front-states

Carga, vacío, error y éxito. En el error, lo que la persona escribió se conserva.

## /front-vitals

Objetivos de LCP, INP y CLS en el percentil 75, móvil y escritorio por separado. Un número que nadie midió queda en hueco.

## Ayuda

## /front-help

El catálogo de este plugin. No escribe un archivo.

## Para quién es

Quien está construyendo una pantalla que ya tiene handoff, textos de interfaz y requisitos de accesibilidad. El handoff queda en `plugin-ui-ux-design`. Las palabras quedan en `plugin-ux-writing`. La auditoría queda en `plugin-accessibility`. Este plugin no copia sus skills.

## Qué incluye

Portable, para cualquier agente que siga [Agent Skills](https://agentskills.io/specification):

- `implement-interface` implementa la estructura, los estados y el presupuesto de vitales.

Cursor y Claude Code: los commands de arriba. En Cursor, `/front-structure`. En Claude Code, `/plugin-frontend:front-structure`.

Solo Cursor: las rules `output-folder`, `handoff-before-code`. Claude Code no carga rules. Las mismas restricciones están en los skills.

## Instalar

En Cursor, instala el plugin desde este repositorio en Customize.

En Claude Code:

```text
claude plugin marketplace add ADRenaline-Suite/plugin-frontend
claude plugin install plugin-frontend@plugin-frontend
```

Para probar una copia local, arranca Claude Code con `claude --plugin-dir <ruta de este repositorio>`.

## Ejemplo

Pide `/front-states` y nombra la pantalla. El registro lista los cuatro estados. `references/angular.md` se lee solo cuando el proyecto ya tiene Angular. Taiga UI se usa solo cuando el proyecto ya depende de él.

## Configuración

El registro numerado va en `adrenaline/frontend/`. El código de la pantalla se queda en el árbol del proyecto. Una app nombrada va en `<subject>/`.

## Licencia

MIT. Copyright (c) 2026 Ricardo Plascencia.

