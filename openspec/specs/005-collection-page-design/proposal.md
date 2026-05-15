# Proposal: Collection page design

## Qué cambia

Ajustar `sections/main-collection-product-grid.liquid` para tener filtros (talla, color, precio, disponibilidad), grid de 3 columnas en desktop / 2 en móvil, product cards minimalistas con hover effect, y badges de "agotado" o "última pieza".

## Por qué

El modelo de inventario rotativo de Star Moda hace crítico que el usuario pueda filtrar fácilmente y vea claramente qué está disponible. El default de Dawn tiene filtros pero el diseño no comunica la urgencia ni la exclusividad que necesita la boutique.

## Alcance

- Modifica `sections/main-collection-product-grid.liquid`
- Modifica `snippets/card-product.liquid` para el hover effect y badges
- No toca homepage ni página de producto
