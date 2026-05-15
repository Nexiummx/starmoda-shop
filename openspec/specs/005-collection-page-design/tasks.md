# Tasks: Collection page design

## Pasos

- [ ] Hacer backup de `sections/main-collection-product-grid.liquid`
- [ ] Configurar layout sidebar+grid en desktop
- [ ] Configurar drawer de filtros en móvil
- [ ] Habilitar filtros: talla, color, precio, disponibilidad
- [ ] Configurar grid a 3 columnas desktop / 2 móvil
- [ ] Modificar `snippets/card-product.liquid`:
  - [ ] Aspect ratio 3:4 vertical en la imagen
  - [ ] Hover swap a segunda imagen con fade 0.3s
  - [ ] Quick add button en esquina inferior derecha (visible en hover)
  - [ ] Badges "Última pieza" o "Agotado" en esquina superior izquierda
- [ ] Configurar sort dropdown a la derecha del título
- [ ] Configurar paginación tipo "Cargar más" en lugar de páginas numeradas
- [ ] Estado vacío con texto custom en español

## Validación

- [ ] Cargar `/collections/all` con productos → debe verse el grid
- [ ] Filtrar por talla → debe filtrar correctamente
- [ ] Producto con 1 unidad → badge "Última pieza"
- [ ] Producto agotado → badge "Agotado"
- [ ] Hover sobre product card → swap a segunda imagen si existe
- [ ] Quick add → agrega al carrito drawer
- [ ] Responsive 375px → 2 columnas, filtros en drawer
