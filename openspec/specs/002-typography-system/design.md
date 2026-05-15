# Design: Typography system

## Stack actual (provisional)

- `type_header_font`: `assistant_n4`
- `type_body_font`: `assistant_n4`
- `heading_scale`: `110`
- `body_scale`: `100`

## Stack ideal (futuro)

Para cuando se resuelvan los handles correctos de Shopify:

- **Títulos:** Cormorant Garamond Light o Playfair Display — serif elegante, editorial, femenino
- **Body:** Jost o Inter — sans-serif limpio, alta legibilidad

## Por qué Assistant ahora

Los handles de fuentes en Shopify siguen el formato `nombrefuente_weight_style` pero no todas las fuentes están disponibles para todos los themes. `assistant_n4` es el default seguro que viene con Dawn y funciona sin error. Cambiar a Cormorant o Jost requiere verificar el handle exacto desde el admin de Shopify.

## Cómo migrar a las fuentes ideales

1. Entrar al admin de Shopify
2. Online Store → Themes → Customize → Theme settings → Typography
3. Cambiar la fuente de headings/body desde el selector visual
4. Guardar
5. Exportar `config/settings_data.json` actualizado desde Actions → Edit code
6. Pegar el nuevo handle en el repo local

## Escalas

- `heading_scale: 110` — títulos un 10% más grandes para presencia editorial
- `body_scale: 100` — body al tamaño default para legibilidad estándar

## Archivos afectados

- `config/settings_data.json` — propiedades `type_header_font`, `type_body_font`, `heading_scale`, `body_scale`
