# Design: Product page

## Layout

### Desktop (≥990px)
- **Columna izquierda (60%):** galería de imágenes
  - Thumbnails verticales al lado izquierdo (80px wide)
  - Imagen principal grande a la derecha
  - Hover sobre imagen principal: zoom suave del 5%
- **Columna derecha (40%):** información del producto

### Móvil (<990px)
- **Stack vertical:**
  - Carrusel horizontal de imágenes con dots indicator
  - Info debajo

## Jerarquía de información

1. **Título del producto** — fuente fina, no bold, size grande
2. **Precio** — destacado, mismo tamaño que título pero peso medium
3. **Badge "Última pieza disponible"** — solo si `current_variant.inventory_quantity == 1`, scheme-4 (negro), pill shape no, esquinas rectas
4. **Selector de talla** — variant pills rectangulares (no radius)
5. **Botón "Agregar al carrito"** — full width, scheme-4
6. **Botón "Comprar ahora"** — full width, outline negro
7. **Acordeones:**
   - Descripción
   - Tallas y medidas
   - Envíos y devoluciones
   - Material y cuidados

## Productos relacionados

Sección al final de la página con heading "Quizás te guste" mostrando 4 productos de la misma colección. Si no hay 4, mostrar los que haya. Layout: 4 columnas desktop, 2 móvil.

## Detalles de estilo

- **Variant pills:** rectangulares (radius 0), border 1px, hover invierte colores
- **Botones:** sin radius, transition 0.3s en hover
- **Acordeones:** sin background, separados por línea sutil 0.5px
- **Badge última pieza:** texto blanco crema sobre fondo negro espresso, padding 6px 14px, fuente caps con letter-spacing

## Restricciones

- Mantener compatibilidad con el editor visual de Shopify
- Variant selector debe seguir funcionando con el JS de Dawn (no romper la lógica)
- Inventory tracking debe estar activo en los productos para que el badge funcione
