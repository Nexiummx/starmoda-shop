# Proposal: Color palette

## Qué cambia

Aplicar la paleta de colores oficial de Star Moda en `config/settings_data.json`, distribuyendo los 6 colores de marca en los 5 schemes que Shopify Dawn maneja.

## Por qué

Dawn viene con una paleta default genérica (blanco/negro/azul). Star Moda tiene una identidad clean girl definida con 6 colores específicos. Mapear esos colores correctamente a los schemes es la base para que toda otra sección (homepage, productos, colecciones) tome los colores automáticamente.

## Alcance

- Solo modifica `config/settings_data.json` en la sección `color_schemes`
- No toca tipografías, layout, ni estructura
- No agrega secciones ni páginas

## Resultado esperado

Al recargar el preview en `http://127.0.0.1:9292`, todas las secciones deben tomar los colores correctos según el scheme asignado. Fondo principal: blanco crema. Texto: negro espresso. Sin cambios visuales más allá del color.
