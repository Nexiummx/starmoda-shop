# Design: Color palette

## Mapeo de colores a schemes

Shopify Dawn maneja 5 color schemes (scheme-1 a scheme-5) que se asignan a secciones individuales. Cada scheme tiene: background, text, button, button_label, secondary_button_label, shadow.

| Scheme | Background | Text | Button | Button label | Uso recomendado |
|---|---|---|---|---|---|
| scheme-1 | `#F7F3EE` (blanco crema) | `#1C1B1A` | `#1C1B1A` | `#F7F3EE` | Principal — 80% del sitio |
| scheme-2 | `#DCCDB8` (beige arena) | `#1C1B1A` | `#1C1B1A` | `#DCCDB8` | Secciones alternas |
| scheme-3 | `#D8B6B6` (rosa nude) | `#1C1B1A` | `#1C1B1A` | `#D8B6B6` | Promociones, acentos suaves |
| scheme-4 | `#1C1B1A` (negro espresso) | `#F7F3EE` | `#F7F3EE` | `#1C1B1A` | Hero dramático, badges |
| scheme-5 | `#9B7B6C` (mocha latte) | `#F7F3EE` | `#D8B16A` | `#1C1B1A` | CTAs premium con dorado |

## Decisiones tomadas

- **Scheme-5 usa dorado champagne en el botón** en lugar del color de fondo para que sea el único contraste cálido especial. Diferencia visual clara entre CTAs normales y CTAs premium.
- **Shadow se mantiene en negro espresso** en todos los schemes para consistencia.
- **Sale badge usa scheme-4** (negro) para máximo contraste con el blanco crema del producto.
- **Sold out badge usa scheme-2** (beige) para señalizar agotado sin agresividad — encaja con la estética.

## Archivos afectados

- `config/settings_data.json` — sección `presets.Dawn.color_schemes`

## Restricciones

- No modificar `config/settings_schema.json` (Shopify lo protege)
- Mantener exactamente 5 schemes — Dawn no soporta más sin modificar el theme
