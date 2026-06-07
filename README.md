# Gustavo Gonik — landing

Landing page en español para Gustavo Gonik: tasación de obras de arte,
cursos y asesoramiento para espacios. Astro estático, desplegado en
Cloudflare Workers (static assets).

## Comandos

```sh
npm install
npm run dev       # desarrollo en http://localhost:4321
npm run build     # genera ./dist
npm run deploy    # build + wrangler deploy (requiere `npx wrangler login` la primera vez)
```

## Contenido a reemplazar antes de publicar

Todo el contenido provisorio está marcado con `REEMPLAZAR` en el código.

1. **Datos de contacto** — un solo lugar: la constante `CONTACTO` en
   `src/pages/index.astro` (WhatsApp, email, teléfono).
2. **Dominio real** — `site` en `astro.config.mjs`.
3. **Retrato de Gustavo** — `src/components/Sobre.astro` (hoy usa una foto
   de stock) y la bio / credenciales reales.
4. **Programa de cursos** — títulos, formatos y fechas en
   `src/components/Cursos.astro`.
5. **Imágenes** — hoy se sirven desde Unsplash (URLs verificadas). Para
   producción conviene descargarlas a `public/` o reemplazarlas por fotos
   propias de obras tasadas.
6. **Formulario** — compone un email en el cliente del visitante (sitio
   estático). Cuando haya backend, cambiar el handler en
   `src/components/Contacto.astro` por un POST (por ejemplo, a un Worker).

## Sistema visual

Definido en `src/styles/global.css` (tokens OKLCH). Documento estratégico
en `PRODUCT.md`. Tinta violeta profunda + paredes blancas de galería;
acento: el punto rojo de "vendida". Tipografía: Gloock (display) +
Schibsted Grotesk (texto), autoalojadas vía Fontsource.
