# Proposal: Typography system

## Qué cambia

Definir las fuentes para títulos y cuerpo en `config/settings_data.json` y ajustar la escala de tipografía para una estética clean girl editorial.

## Por qué

Dawn viene con Assistant Regular como default, que es funcional pero genérica. Star Moda necesita una tipografía que comunique elegancia editorial femenina: títulos finos y cuerpo legible. Aunque por ahora se mantiene `assistant_n4` por compatibilidad con Shopify, este change documenta el sistema y deja la base para migrar a fuentes premium después.

## Alcance

- Modifica `type_header_font`, `type_body_font`, `heading_scale`, `body_scale` en `config/settings_data.json`
- No toca colores, layout, secciones
- Deja documentado qué fuentes ideales se quieren cuando se resuelva el tema de handles de Shopify

## Resultado esperado

Tipografía consistente en todo el sitio. Títulos un 10% más grandes que el default para sensación editorial. Body al 100% para legibilidad estándar.
