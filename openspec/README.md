# OpenSpec — Star Moda

Specs y changes para el proyecto Star Moda (Shopify Dawn). Cada change es un cambio atómico al theme: una proposal, un set de tasks y un documento de design.

## Estructura

- `changes/` — propuestas activas, no ejecutadas todavía
- `specs/` — capacidades ya implementadas (registro permanente)

## Flujo

1. Leer `changes/XXX-nombre/proposal.md` para entender qué cambia y por qué
2. Revisar `changes/XXX-nombre/design.md` para decisiones técnicas
3. Ejecutar las tareas de `changes/XXX-nombre/tasks.md` en orden
4. Al terminar, mover la carpeta de `changes/` a `specs/` como registro

## Changes activos

| ID | Nombre | Estado |
|---|---|---|
| 001 | Color palette | Listo para ejecutar |
| 002 | Typography system | Listo para ejecutar |
| 003 | Homepage structure | Listo para ejecutar |
| 004 | Product page design | Listo para ejecutar |
| 005 | Collection page design | Listo para ejecutar |
| 006 | Essential pages | Listo para ejecutar |
| 007 | Global styles | Listo para ejecutar |

## Contexto del proyecto

Star Moda es una boutique de ropa de mujer en Durango, México. Modelo de inventario rotativo (cada pieza es única, no se repone). Theme: Shopify Dawn. Estética: clean girl minimalista.

Paleta:
- Negro espresso `#1C1B1A`
- Blanco crema `#F7F3EE`
- Beige arena `#DCCDB8`
- Rosa nude `#D8B6B6`
- Mocha latte `#9B7B6C`
- Dorado champagne `#D8B16A`

## Reglas para Claude Code

- No modificar `layout/theme.liquid` ni `config/settings_schema.json` (Shopify los protege)
- No instalar dependencias nuevas
- Mantener compatibilidad con el editor visual de Shopify
- Textos en español de México
- Verificar responsive (375px móvil, 1440px desktop)
