# Design: Homepage structure

## Orden y propósito de cada sección

### 1. Announcement bar
- **Sección Dawn:** `announcement-bar`
- **Scheme:** scheme-4 (negro)
- **Texto:** "Envíos a todo México · Últimas piezas disponibles"
- **Sin link**
- **Rol:** Comunicar confianza (envíos) y urgencia sutil (últimas piezas)

### 2. Header
- **Sección Dawn:** `header`
- **Scheme:** scheme-1
- **Logo:** centrado, width 120px
- **Menú:** Inicio · Tienda · Nuevos ingresos · Sobre nosotros · Contacto
- **Iconos:** búsqueda, cuenta, carrito drawer
- **Sticky:** activado
- **Rol:** Navegación principal y branding

### 3. Image banner (Hero)
- **Sección Dawn:** `image-banner`
- **Scheme:** scheme-4 (texto blanco sobre imagen oscurecida)
- **Altura desktop:** large (75vh aprox)
- **Altura móvil:** medium
- **Overlay opacity:** 20%
- **Heading:** "Nueva temporada"
- **Subheading:** "Piezas únicas, encontradas una sola vez"
- **Button label:** "Descubrir colección"
- **Button link:** `/collections/all`
- **Imagen:** placeholder Unsplash (foto editorial de mujer con ropa neutra)
- **Rol:** Primera impresión, comunicar exclusividad

### 4. Rich text — Bienvenida
- **Sección Dawn:** `rich-text`
- **Scheme:** scheme-1
- **Heading:** "Star Moda"
- **Texto:** "Curamos cada prenda con intención. Modelos seleccionados a mano, en cantidades limitadas. Cuando se va, se va."
- **Alineación:** centrada
- **Width:** medium
- **Rol:** Establecer el manifiesto de la marca

### 5. Collection list — Categorías
- **Sección Dawn:** `collection-list`
- **Scheme:** scheme-1
- **Heading:** "Compra por categoría"
- **Collections to show:** 3
- **Card style:** standard
- **Rol:** Dar entrada al catálogo desde categorías

### 6. Featured collection — Nuevos ingresos
- **Sección Dawn:** `featured-collection`
- **Scheme:** scheme-2 (beige arena)
- **Heading:** "Recién llegado"
- **Description:** "Lo más nuevo de la semana"
- **Products to show:** 8
- **Columns desktop:** 4
- **Columns móvil:** 2
- **View all button:** visible, texto "Ver todo"
- **Rol:** Mostrar producto fresco, generar deseo

### 7. Image with text — Sobre Star Moda
- **Sección Dawn:** `image-with-text`
- **Scheme:** scheme-1
- **Layout:** image left, text right
- **Heading:** "Una pieza, una historia"
- **Texto:** "Star Moda nace de la idea de que la moda no debe ser desechable. Cada prenda que llega a la tienda fue elegida pensando en una mujer que valora lo único sobre lo masivo. Sin reposiciones. Sin temporadas que se repiten. Solo piezas que llegaron para encontrar a su persona."
- **Button label:** "Conoce más"
- **Button link:** `/pages/about`
- **Rol:** Profundizar el storytelling

### 8. Multicolumn — Diferenciadores
- **Sección Dawn:** `multicolumn`
- **Scheme:** scheme-3 (rosa nude)
- **Heading:** "Lo que nos hace diferentes"
- **3 columnas:**
  - **Piezas únicas** — "Cada modelo se sube una sola vez. Lo que ves es lo que hay."
  - **Calidad curada** — "Seleccionamos cada prenda a mano antes de subirla."
  - **Envíos seguros** — "Envíos a todo México con paquetería de confianza."
- **Rol:** Razones de compra explícitas

### 9. Newsletter
- **Sección Dawn:** `newsletter`
- **Scheme:** scheme-4 (negro)
- **Heading:** "Únete a la lista"
- **Subheading:** "Sé la primera en saber cuando lleguen modelos nuevos"
- **Rol:** Captar email para retargeting

### 10. Footer
- **Sección Dawn:** `footer` (global, no se mete en index.json — se configura en `sections/footer-group.json`)
- **Scheme:** scheme-1
- **3 columnas:** branding, links rápidos, redes
- **Copyright:** "© 2026 Star Moda · Tecnología por Nexium"

## Estructura de templates/index.json

```json
{
  "sections": {
    "image_banner": { ... },
    "rich_text_welcome": { ... },
    "collection_list_categories": { ... },
    "featured_collection_new": { ... },
    "image_with_text_about": { ... },
    "multicolumn_diff": { ... },
    "newsletter": { ... }
  },
  "order": [
    "image_banner",
    "rich_text_welcome",
    "collection_list_categories",
    "featured_collection_new",
    "image_with_text_about",
    "multicolumn_diff",
    "newsletter"
  ]
}
```

(El announcement bar, header y footer se configuran en sus respectivos `*-group.json`, no en `index.json`.)

## Imágenes placeholder

Usar imágenes de Unsplash con URLs directas. Marcar con comentarios `// TODO: foto real de Mariana` en el JSON donde aplique. Sugerencias:
- Hero: foto editorial de mujer con ropa neutra
- Image with text: foto de detalle de prenda (textura, costura)
- Collection list: 3 fotos de outfits diferentes para representar categorías

## Restricciones

- No modificar `layout/theme.liquid`
- Mantener IDs de sección legibles para que el editor visual los muestre bien
