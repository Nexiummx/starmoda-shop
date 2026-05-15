# Tasks: Homepage structure

## Pasos

- [ ] Hacer backup de `templates/index.json` actual (copiar a `templates/index.json.bak`)
- [ ] Reescribir `templates/index.json` con la estructura definida en design.md
- [ ] Crear sección `image_banner` con todos los settings del design.md (sección 3)
- [ ] Crear sección `rich_text_welcome` con copy "Star Moda" y manifiesto
- [ ] Crear sección `collection_list_categories` con heading "Compra por categoría", 3 collections
- [ ] Crear sección `featured_collection_new` con heading "Recién llegado", 8 productos, scheme-2
- [ ] Crear sección `image_with_text_about` con heading "Una pieza, una historia"
- [ ] Crear sección `multicolumn_diff` con 3 columnas (Piezas únicas, Calidad curada, Envíos seguros), scheme-3
- [ ] Crear sección `newsletter` con heading "Únete a la lista", scheme-4
- [ ] Definir el array `order` en el JSON con las 7 secciones en el orden correcto
- [ ] Guardar el archivo
- [ ] Configurar announcement bar en `sections/announcement-bar-group.json` o donde corresponda con texto "Envíos a todo México · Últimas piezas disponibles"
- [ ] Verificar en `http://127.0.0.1:9292` que cargan las 7 secciones en orden

## Imágenes

- [ ] Buscar imagen de Unsplash para hero (editorial mujer ropa neutra) y poner URL directa
- [ ] Buscar imagen de Unsplash para image-with-text (detalle de prenda) y poner URL directa
- [ ] Dejar collection_list sin imágenes hasta que existan colecciones reales

## Validación

- La página de homepage en `/` debe cargar sin errores 500
- Cada sección debe respetar el scheme asignado (verificar colores de fondo)
- Los textos deben estar en español
- En móvil (375px), todas las secciones deben verse correctamente sin overflow horizontal
