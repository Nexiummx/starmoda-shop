# Tasks: Essential pages

## Crear templates

- [ ] Crear `templates/page.about.json` con: image-banner, rich-text (historia), multicolumn (3 valores), newsletter
- [ ] Crear `templates/page.shipping.json` con: rich-text centrado (política de envíos)
- [ ] Crear `templates/page.returns.json` con: rich-text centrado (devoluciones)
- [ ] Crear `templates/page.contact.json` con: rich-text (heading + subheading), main-contact (form), rich-text (datos)

## Contenido inicial

- [ ] Llenar el rich-text de about con placeholder editable
- [ ] Llenar el rich-text de envíos con la información del design.md
- [ ] Llenar el rich-text de devoluciones con la información del design.md
- [ ] Llenar el rich-text de contacto con WhatsApp/Instagram placeholders

## Tareas manuales (no automatizables)

- [ ] En el admin de Shopify ir a Online Store → Pages → Add page
- [ ] Crear página "Sobre nosotros", asignar template `page.about`
- [ ] Crear página "Envíos", asignar template `page.shipping`
- [ ] Crear página "Cambios y devoluciones", asignar template `page.returns`
- [ ] Crear página "Contacto", asignar template `page.contact`
- [ ] Agregar las páginas al menú principal (Navigation → Main menu)
- [ ] Agregar las páginas al menú del footer

## Validación

- [ ] Visitar `/pages/about` → debe cargar con la estructura definida
- [ ] Visitar `/pages/envios` → debe cargar el contenido
- [ ] Visitar `/pages/devoluciones` → debe cargar el contenido
- [ ] Visitar `/pages/contacto` → form debe enviar correctamente (probar)
- [ ] Links del footer deben llevar a las páginas correctas
