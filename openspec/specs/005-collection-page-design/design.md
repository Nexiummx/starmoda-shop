# Design: Collection page

## Layout

### Desktop (≥990px)
- **Sidebar izquierda (240px):** filtros y orden
- **Área principal:** grid de 3 columnas

### Móvil (<990px)
- **Filtros:** drawer que se abre con un botón "Filtrar y ordenar"
- **Grid:** 2 columnas

## Filtros disponibles

- **Por talla** — checkbox list
- **Por color** — swatches visuales si los productos tienen color metadata, sino checkbox
- **Por precio** — slider con rango min-max
- **Por disponibilidad** — checkbox: "En stock" / "Próximamente"

Los filtros deben usar el sistema de filters nativo de Shopify (`collection.filters`).

## Product card

### Estructura
- Imagen del producto (aspect ratio 3:4, vertical)
- Nombre del producto (peso regular, no bold, size 14px)
- Precio (peso medium, size 14px)
- Hover en imagen: cambiar a segunda imagen si existe (con fade 0.3s)
- Quick add discreto: botón "+" pequeño en esquina inferior derecha de la imagen, aparece en hover

### Badges
- **"Última pieza"** — esquina superior izquierda, scheme-4, mostrar si `inventory == 1`
- **"Agotado"** — esquina superior izquierda, scheme-2, mostrar si `available == false`
- Solo uno a la vez (prioridad: agotado > última pieza)

### Estilo
- Sin border, sin shadow, sin background
- Solo imagen y texto debajo
- Spacing entre cards: 24px desktop, 12px móvil

## Detalles de estilo

- **Sort dropdown:** debajo del título de la colección, alineado a la derecha
- **Contador de productos:** "X productos" arriba a la derecha
- **Paginación:** infinite scroll o "Cargar más" button (preferible button)
- **Sin productos:** estado vacío con texto "No hay productos que coincidan con los filtros. Ajusta tu búsqueda."

## Restricciones

- Filtros deben funcionar con la API nativa de Shopify
- Quick add no debe abrir el producto, solo agregar al carrito con la talla default
- Si el producto tiene variantes, quick add abre un mini-selector de talla
