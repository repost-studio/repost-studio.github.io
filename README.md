# Repost Studio — Landing

Sitio estático (HTML + CSS + JS) listo para GitHub Pages.

## Estructura de la página

1. **Hero** — "Estudio creativo y estratégico para negocios" + video de presentación del equipo (1 min) + cinta de marcas
2. **Quiénes somos** — con foto del equipo
3. **Qué hacemos** — 6 servicios en acordeón + acceso a la consultoría
4. **Consultoría gastronómica** — 3 packs con precios y botón de WhatsApp por pack
5. **Trabajos** — carrusel de clientes (links a Instagram)
6. **Metodología** — rueda interactiva de 5 etapas
7. **Testimonios** — 3 videos verticales
8. **Contacto** — "Hay mucho por hacer. ¿Por dónde empezamos?" + botón Hablemos

## Archivos y carpeta assets/

```
index.html   style.css   script.js   favicon.svg
assets/
  presentacion.mp4 / presentacion.jpg   ← video del equipo (máx. 1 min) y su portada
  equipo.jpg                            ← foto del equipo
  logos/                                ← PNG o SVG con fondo transparente (se ven en blanco)
    karun.png  elnino.png  jmc.png  orsino.png  carnico.png  repost.png
  servicio-contenido.mp4                ← 01 Contenido (reel vertical)
  servicio-ads.jpg                      ← 03 Campañas
  servicio-eventos.mp4                  ← 04 Eventos
  servicio-redes-1.jpg / -2.jpg         ← 05 Redes
  servicio-web.jpg                      ← 06 Web
  cliente-elnino.mp4  cliente-ceramica.jpg  cliente-orsino.jpg
  cliente-jmc.mp4     cliente-carnico.jpg
  testimonio-1.mp4 / .jpg  testimonio-2.mp4 / .jpg  testimonio-3.mp4 / .jpg
```

Si falta un archivo, la página muestra un bloque rojo con su etiqueta (o solo el nombre en la cinta, si falta un logo).

## Cosas para editar rápido

- **WhatsApp:** buscá `5491125465526` en `index.html` (hay varios links).
- **Precios de los packs:** sección `#consultoria` en `index.html`.
- **Testimonios:** nombre y marca en cada `<figcaption>` de `#testimonios`.
- **Proporción del video del hero:** variable `--intro-ratio` al inicio de `style.css` (`4/5` vertical, `16/10` horizontal, `9/16` reel).
- **Colores:** variables al inicio de `style.css`.
- **Quitar el carrusel de Trabajos:** borrar la sección `#trabajos` y su link en el menú.

## Publicar en GitHub Pages

1. Subí todo a la raíz de un repo.
2. Settings → Pages → Deploy from a branch → `main` / root.

## Consejos para los videos

- Comprimilos: `ffmpeg -i in.mp4 -vf scale=-2:720 -crf 28 out.mp4` (con `-an` si no necesitan audio).
- El video de presentación y los testimonios necesitan audio; los demás pueden ir sin sonido.
- Pedí permiso a cada cliente para usar su contenido.
