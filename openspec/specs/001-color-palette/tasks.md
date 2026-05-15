# Tasks: Color palette

## Pasos

- [ ] Abrir `config/settings_data.json`
- [ ] Localizar la sección `presets.Dawn.color_schemes`
- [ ] Reemplazar scheme-1 con: background `#F7F3EE`, text `#1C1B1A`, button `#1C1B1A`, button_label `#F7F3EE`, secondary_button_label `#1C1B1A`, shadow `#1C1B1A`
- [ ] Reemplazar scheme-2 con: background `#DCCDB8`, text `#1C1B1A`, button `#1C1B1A`, button_label `#DCCDB8`, secondary_button_label `#1C1B1A`, shadow `#1C1B1A`
- [ ] Reemplazar scheme-3 con: background `#D8B6B6`, text `#1C1B1A`, button `#1C1B1A`, button_label `#D8B6B6`, secondary_button_label `#1C1B1A`, shadow `#1C1B1A`
- [ ] Reemplazar scheme-4 con: background `#1C1B1A`, text `#F7F3EE`, button `#F7F3EE`, button_label `#1C1B1A`, secondary_button_label `#F7F3EE`, shadow `#1C1B1A`
- [ ] Reemplazar scheme-5 con: background `#9B7B6C`, text `#F7F3EE`, button `#D8B16A`, button_label `#1C1B1A`, secondary_button_label `#F7F3EE`, shadow `#1C1B1A`
- [ ] Cambiar `sale_badge_color_scheme` a `scheme-4`
- [ ] Cambiar `sold_out_badge_color_scheme` a `scheme-2`
- [ ] Guardar el archivo
- [ ] Verificar en `http://127.0.0.1:9292` que el fondo es blanco crema y el texto negro espresso

## Validación

El servidor de Shopify CLI debe mostrar el mensaje `Synced » update config/settings_data.json` en la terminal después de guardar. Si no aparece, el servidor no está detectando el cambio.
