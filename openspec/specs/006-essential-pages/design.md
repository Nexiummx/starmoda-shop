# Design: Essential pages

## Páginas a crear

### 1. Sobre nosotros (`/pages/about`)
- **Template:** `templates/page.about.json`
- **Secciones:**
  - Image banner pequeño con tagline "Star Moda · Boutique con intención"
  - Rich text: historia de Mariana y la tienda (placeholder con texto editable después)
  - Multicolumn: 3 valores (Curación, Exclusividad, Atención personal)
  - Newsletter al final
- **Scheme principal:** scheme-1

### 2. Envíos (`/pages/envios`)
- **Template:** `templates/page.shipping.json`
- **Contenido:**
  - Heading: "Política de envíos"
  - Texto:
    - Tiempos de entrega por zona (Durango ciudad: 1-2 días · Resto del país: 3-5 días)
    - Costos (envío gratis a partir de $1,500 MXN · costo estándar $150 MXN)
    - Paqueterías: Estafeta, FedEx (placeholder hasta confirmar con Mariana)
    - Empaque seguro
- **Scheme:** scheme-1
- **Layout:** rich text centrado, width medium

### 3. Devoluciones (`/pages/devoluciones`)
- **Template:** `templates/page.returns.json`
- **Contenido:**
  - Heading: "Cambios y devoluciones"
  - Texto:
    - Plazo: 7 días desde la entrega
    - Condiciones: prenda sin uso, con etiqueta original
    - Proceso paso a paso:
      1. Contactar por WhatsApp
      2. Enviar fotos de la prenda
      3. Recibir guía prepagada
      4. Crédito en tienda o reembolso (definir)
    - Excepciones: prendas de oferta no aplican cambio
- **Scheme:** scheme-1
- **Layout:** rich text centrado, width medium

### 4. Contacto (`/pages/contacto`)
- **Template:** `templates/page.contact.json`
- **Contenido:**
  - Heading: "Háblanos"
  - Subheading: "Estamos aquí para ayudarte"
  - Formulario de contacto (usar form de Dawn)
  - Datos:
    - WhatsApp directo: link `wa.me/52XXXXXXXXXX` (placeholder)
    - Instagram: `@starmoda` (placeholder)
    - Horario de atención: Lunes a Sábado 10am-7pm
    - Dirección de tienda física (cuando Mariana la dé)
- **Scheme:** scheme-1

## Estilo común

- Width centrado: medium (max-width 720px en texto)
- Tipografía: heading grande, body legible
- Spacing generoso entre párrafos (24px)
- Listas con bullets discretos (•)
- CTAs en botones scheme-4 cuando aplique

## Restricciones

- Los templates JSON deben ser válidos para Shopify (estructura `sections` + `order`)
- Las páginas mismas (no los templates) se crean en el admin de Shopify: Online Store → Pages → Add page, asignando el template correcto a cada una
- Esto último no es automatizable por código — queda como tarea manual
