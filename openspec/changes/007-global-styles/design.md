# Design: Global styles

## Valores en settings_data.json

Para todos los radius, valor 0:

| Propiedad | Valor |
|---|---|
| `buttons_radius` | 0 |
| `variant_pills_radius` | 0 |
| `inputs_radius` | 0 |
| `card_corner_radius` | 0 |
| `collection_card_corner_radius` | 0 |
| `blog_card_corner_radius` | 0 |
| `text_boxes_radius` | 0 |
| `media_radius` | 0 |
| `popup_corner_radius` | 0 |
| `badge_corner_radius` | 0 |

Para todas las sombras, opacity 0:

| Propiedad | Valor |
|---|---|
| `buttons_shadow_opacity` | 0 |
| `variant_pills_shadow_opacity` | 0 |
| `inputs_shadow_opacity` | 0 |
| `card_shadow_opacity` | 0 |
| `collection_card_shadow_opacity` | 0 |
| `blog_card_shadow_opacity` | 0 |
| `text_boxes_shadow_opacity` | 0 |
| `media_shadow_opacity` | 0 |
| `popup_shadow_opacity` | 0 |
| `drawer_shadow_opacity` | 0 |

Para borders en cards/medias, ponerlos en 0 (sin border visible):

| Propiedad | Valor |
|---|---|
| `card_border_thickness` | 0 |
| `card_border_opacity` | 0 |
| `media_border_thickness` | 0 |
| `media_border_opacity` | 0 |

Para spacing entre secciones:

| Propiedad | Valor |
|---|---|
| `spacing_sections` | 0 (sin padding extra entre secciones, cada sección controla el suyo) |
| `spacing_grid_horizontal` | 12 |
| `spacing_grid_vertical` | 12 |

Para animaciones:

| Propiedad | Valor |
|---|---|
| `animations_reveal_on_scroll` | true |
| `animations_hover_elements` | "image" (hover en imágenes con zoom) |

## Archivo star-moda.css

Crear `assets/star-moda.css` con overrides puntuales para cosas que no se controlan desde settings_data.json:

```css
/* Botones — hover invertido suave */
.button:not([disabled]) {
  transition: background-color 0.3s ease, color 0.3s ease;
}

.button--primary:hover {
  background-color: #F7F3EE;
  color: #1C1B1A;
  border: 1px solid #1C1B1A;
}

.button--secondary:hover {
  background-color: #1C1B1A;
  color: #F7F3EE;
}

/* Iconos — outline más fino */
.icon {
  stroke-width: 1.5px;
}

/* Cards — sin background ni decoración */
.card-wrapper .card,
.card-wrapper .card__inner {
  background: transparent;
  border: none;
  box-shadow: none;
}

/* Imágenes producto — hover zoom suave */
.card-wrapper .card__media img,
.product-media-modal__content img {
  transition: transform 0.4s ease;
}

.card-wrapper:hover .card__media img {
  transform: scale(1.05);
}

/* Spacing entre secciones */
.shopify-section + .shopify-section {
  margin-top: 0;
}

.shopify-section {
  padding-top: 5rem;
  padding-bottom: 5rem;
}

@media (max-width: 749px) {
  .shopify-section {
    padding-top: 3rem;
    padding-bottom: 3rem;
  }
}

/* Badges custom Star Moda */
.badge--last-piece {
  background-color: #1C1B1A;
  color: #F7F3EE;
  padding: 6px 14px;
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  font-weight: 500;
}

.badge--sold-out {
  background-color: #DCCDB8;
  color: #1C1B1A;
  padding: 6px 14px;
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 0.08em;
}
```

## Cómo cargar el CSS

Opción A (preferida): incluirlo desde un snippet que ya esté cargando en `theme.liquid`. Buscar `{{ 'base.css' | asset_url | stylesheet_tag }}` o similar, y poner justo después:

```liquid
{{ 'star-moda.css' | asset_url | stylesheet_tag }}
```

Esto requiere editar `theme.liquid`, lo cual está prohibido. Alternativa:

Opción B (real): cargar el CSS desde una sección que aparezca en todas las páginas (ej. el `header`). Modificar `sections/header.liquid` para incluir al inicio:

```liquid
{{ 'star-moda.css' | asset_url | stylesheet_tag }}
```

Como header.liquid no es protegido, se puede modificar.

## Restricciones

- No editar `theme.liquid` ni `settings_schema.json`
- `star-moda.css` debe ser idempotente (cargarlo dos veces no debe causar problemas)
- Mantener selectores específicos para no romper otros themes en caso de update de Dawn
