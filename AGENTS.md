# AGENTS.md

## Qué es este proyecto

Landing/catálogo de una sola página para B&M District (streetwear). No tiene backend: es HTML/CSS/JS estático, con pedidos gestionados vía enlaces `wa.me` de WhatsApp (no hay checkout ni base de datos).

## Estructura

- `index.html` — todo el marcado, estilos (`<style>` inline) y el JS de la página (filtro de productos, modal de zoom de imagen) viven en este único archivo.
- `img/` — imágenes reales de producto y logo. Antes vivían embebidas como `data:image/...;base64` dentro del HTML; se extrajeron a archivos para que el peso de la página y del repo sea razonable y las imágenes puedan optimizarse en el edge.
- `netlify.toml` — publica el sitio desde la raíz del repo, sin paso de build.

## Convenciones

- Todas las referencias a imágenes usan Netlify Image CDN: `/.netlify/images?url=/img/<archivo>&w=<ancho>&q=90`. Si se agregan imágenes nuevas, seguir el mismo patrón en vez de enlazar `img/<archivo>` directo, para mantener la optimización automática.
- Los anchos (`w=`) están calibrados por contexto: logo de nav/footer más pequeño, `hero-logo` más grande, fotos de producto en `w=900` para verse nítidas en pantallas retina dentro de la grilla de 4 columnas.
- No hay build ni framework: cualquier cambio de contenido es edición directa de `index.html`.

## Si se retoma este proyecto

No queda un PLAN.md pendiente: la página está completa según el diseño original. Posibles siguientes pasos naturales (no iniciados) serían activar Netlify Forms para capturar leads, o mover el catálogo de productos a Netlify Blobs/DB si se vuelve dinámico.
