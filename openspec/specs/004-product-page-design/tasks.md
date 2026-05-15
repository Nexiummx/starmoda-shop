# Tasks: Product page design

## Pasos

- [ ] Hacer backup de `sections/main-product.liquid` (copiar a `.bak`)
- [ ] Ajustar el layout para que en desktop sea galería 60% / info 40%
- [ ] Cambiar thumbnails a layout vertical en desktop
- [ ] Agregar zoom suave en hover sobre imagen principal (CSS, scale(1.05) con transition 0.4s)
- [ ] Crear snippet `snippets/last-piece-badge.liquid` que se renderice solo si `inventory_quantity == 1`
- [ ] Incluir el snippet en main-product.liquid antes del título
- [ ] Cambiar variant pills a `radius: 0` (heredar de settings_data.json scheme correcto)
- [ ] Asegurar que botón "Add to cart" use scheme-4
- [ ] Agregar botón "Comprar ahora" (Buy now button) outline
- [ ] Configurar acordeones para Descripción, Tallas y medidas, Envíos y devoluciones, Material y cuidados
- [ ] Agregar al final sección "Quizás te guste" con productos relacionados (usar `recommendations` de Shopify)
- [ ] Traducir todos los strings al español si hay alguno en inglés

## Validación

- [ ] Cargar un producto con `inventory: 1` → debe aparecer el badge "Última pieza disponible"
- [ ] Cargar un producto con `inventory: >1` → no debe aparecer el badge
- [ ] Probar selector de talla → debe actualizar precio e imagen si la variante lo requiere
- [ ] Probar "Add to cart" → debe agregar al carrito drawer
- [ ] Verificar responsive en 375px
