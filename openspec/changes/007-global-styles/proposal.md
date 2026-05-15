# Proposal: Global styles

## Qué cambia

Crear un archivo `assets/star-moda.css` con overrides globales que apliquen la estética clean girl en todo el theme: radius 0 universal, sin sombras, spacing generoso, hover states refinados, iconos outline 1.5px. Incluirlo en el theme desde el snippet o asset apropiado.

## Por qué

Hay detalles de estilo que deben ser consistentes en TODO el sitio (no solo en una sección): nada de border-radius, ninguna sombra, animaciones suaves, iconos estilo outline. Centralizarlos en un solo archivo CSS hace más fácil mantenerlos y modificarlos después.

## Alcance

- Crea `assets/star-moda.css`
- Modifica el include de assets para cargarlo (probablemente en `layout/theme.liquid`, pero NO se puede tocar — alternativa: cargarlo desde una sección o snippet)
- Ajusta `config/settings_data.json` para que valores como `buttons_radius`, `card_corner_radius`, etc. estén en 0

## Restricciones críticas

- **No tocar `layout/theme.liquid`** — Shopify lo protege
- Cargar el CSS desde un snippet incluido en `theme.liquid` ya existente, o aprovechar `assets/base.css` directamente (ojo: base.css se sobrescribe en updates de Dawn)
- Mejor opción: modificar `settings_data.json` para valores estructurales y dejar `star-moda.css` para overrides muy específicos cargado desde una sección global
