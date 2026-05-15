# Tasks: Global styles

## Pasos

### En settings_data.json

- [ ] Poner todos los `*_radius` en 0
- [ ] Poner todos los `*_shadow_opacity` en 0
- [ ] Poner `card_border_thickness` y `card_border_opacity` en 0
- [ ] Poner `media_border_thickness` y `media_border_opacity` en 0
- [ ] Verificar `spacing_grid_horizontal: 12` y `spacing_grid_vertical: 12`
- [ ] Verificar `animations_reveal_on_scroll: true`
- [ ] Verificar `animations_hover_elements: "image"`

### Crear archivo CSS

- [ ] Crear `assets/star-moda.css` con el contenido del design.md
- [ ] Modificar `sections/header.liquid` para incluir `{{ 'star-moda.css' | asset_url | stylesheet_tag }}` al inicio del archivo (después del schema y antes del HTML)

## Validación

- [ ] Inspeccionar elementos en el browser → botones deben tener `border-radius: 0`
- [ ] Inspeccionar cards → no deben tener `box-shadow`
- [ ] Hover sobre product card → imagen debe hacer zoom suave del 5%
- [ ] Hover sobre botón primario → debe invertir colores con transición de 0.3s
- [ ] Verificar que el CSS se carga (Network tab en DevTools)
- [ ] Verificar que no se rompió ningún layout existente
