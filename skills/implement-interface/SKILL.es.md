---
name: implement-interface
description: Implementa una pantalla desde un handoff: su estructura, sus estados y su presupuesto de vitales.
---

<p align="right">Idioma:&emsp;<a href="SKILL.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 Frontend](../../README.md)

# Implementa una pantalla desde un handoff: su estructura, sus estados y su presupuesto de vitales

La pantalla que se construye es la que el handoff nombra. Los estados son parte de la pantalla, no un paso posterior.

Source: Core Web Vitals como los publica web.dev (LCP, INP, CLS, percentil 75). El handoff es la fuente del layout. La práctica de la comunidad que coincide: elementos semánticos antes que ARIA, la biblioteca de componentes del proyecto antes que un widget nuevo, cada cadena visible sale del texto, y carga, vacío, error y éxito están antes de dar la pantalla por hecha.

## Antes de escribir

1. Lee solo la referencia que nombra este command: [structure](references/structure.md), [states](references/states.md) o [vitals](references/vitals.md).
2. Si el proyecto ya es Angular, lee también [angular](references/angular.md).
3. Detente si faltan el handoff, los textos o los requisitos de accesibilidad.

References: [structure](references/structure.md), [states](references/states.md), [vitals](references/vitals.md).

## Entrega

El código va en el árbol que el proyecto ya compila, en el framework que ese árbol ya usa. El registro numerado va en la carpeta de salida. No elijas Angular, React ni otro framework.

Cada archivo de este skill va en `adrenaline/frontend/`, o en `outputDirs["plugin-frontend"]` si `.cursor/adrenaline.json` da una ruta relativa válida. Si `adrenaline/frontend/` aún no existe y `frontend/` en la raíz del proyecto ya tiene el `ORIGIN.json` o el `STATUS.md` de este plugin, sigue escribiendo ahí y dilo.

Si la persona nombra un proyecto, una app, un servicio o un dominio, el archivo de ese asunto va en `<subject>/`. Un archivo de todo el producto se queda en la raíz de la salida. `<NNN>` es el siguiente número libre en toda la carpeta. La celda `archivo` es `<subject>/<file>` cuando hay asunto (`doc/arch/adr-008-asunto-subcarpeta.md`).

Escribe `ORIGIN.json` junto a `STATUS.md` al crear la carpeta, y otra vez solo si falta o un campo difiere. Campos: `suite` `ADRenaline-Suite`, `plugin` `plugin-frontend`, `repository` `https://github.com/ADRenaline-Suite/plugin-frontend`, `convention` `adr-001`. No es un archivo `<NNN>` y no tiene fila en `STATUS.md`.

No inventes un dato que la persona no dio. Un título obligatorio sin dato queda como hueco y el archivo sigue `proposed`. "None." llena un título.

## Done

- [ ] Solo se aplicó la referencia de este command.
- [ ] La carpeta de salida, la subcarpeta del asunto, `ORIGIN.json` y `STATUS.md` coinciden con las reglas de entrega.
- [ ] Un dato obligatorio que falta es un hueco. El archivo sigue `proposed`.

## Example

Un pedido que nombra la pieza y su fuente escribe un archivo. Un pedido sin esa fuente no escribe nada y nombra el hueco.
