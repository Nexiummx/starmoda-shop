# Proposal: Essential pages

## Qué cambia

Crear las 4 páginas obligatorias para un ecommerce: Sobre nosotros, Envíos, Devoluciones, Contacto. Cada una con su template Liquid y contenido inicial en español.

## Por qué

Estas páginas son requeridas legalmente (envíos, devoluciones) y operacionalmente (sobre nosotros, contacto) para que la tienda comunique confianza y profesionalismo. Sin ellas, no se puede lanzar.

## Alcance

- Crea 4 templates en `templates/page.*.json` o `templates/page.*.liquid`
- Crea las páginas correspondientes en Shopify admin (no automatizable desde código — queda como tarea de admin)
- No toca homepage, productos, ni colecciones
