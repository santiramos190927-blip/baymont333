# B&M District | Urban Wear

Sitio de catálogo para B&M District, una marca de streetwear. Presenta la colección de sudaderas disponible, categorías próximas a lanzar (camisetas, relojes, gorras) y un flujo de pedidos directo por WhatsApp, con vista ampliada de cada producto.

## Tecnologías

- HTML, CSS y JavaScript estáticos, sin build ni dependencias.
- Imágenes servidas a través de Netlify Image CDN (`/.netlify/images?url=...`) para entregar cada foto de producto y el logo optimizados, sin perder nitidez frente al archivo original.

## Estructura

- `index.html` — página única con todas las secciones (inicio, categorías, catálogo de sudaderas, próximamente, contacto).
- `img/` — fotos de producto y logo en su resolución original.
- `netlify.toml` — configuración de publicación (sitio estático servido desde la raíz).

## Cómo ejecutarlo localmente

```bash
netlify dev
```

Esto sirve `index.html` con emulación local del Image CDN y del resto de funciones de Netlify.

## Pedidos

Los botones "PEDIR POR WHATSAPP" abren un mensaje prellenado hacia el número de contacto de la marca (318 939 8381) con el producto y talla elegidos.
