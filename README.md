# Repost Studio — Landing

Sitio estático (HTML + CSS + JS) listo para GitHub Pages.

## Estructura de la página

1. **Hero** — "Estudio creativo y estratégico para negocios" + video de presentación del equipo + cinta de marcas
2. **Quiénes somos** — con foto del equipo
3. **Qué hacemos** — 6 servicios en acordeón: Creación de contenido · Consultoría y desarrollo de negocios · Estrategia y campañas digitales · Cobertura audiovisual de eventos · Gestión de redes sociales · Diseño y desarrollo web
4. **Trabajos** — carrusel de reels y fotos de distintas marcas
5. **Metodología** — rueda interactiva de 5 etapas + cierre "Porque creemos que los mejores resultados se construyen en equipo"
6. **Testimonios** — 3 videos verticales
7. **Contacto** — "Hay mucho por hacer. ¿Por dónde empezamos?" + botón Hablemos

## Archivos y carpeta assets/

```
index.html   style.css   script.js   favicon.svg
assets/
  presentacion.mp4 / presentacion.jpg   ← video del equipo (máx. 1 min) y su portada
  equipo.jpg                            ← foto del equipo (se define más adelante)
  logos/                                ← cinta de marcas (PNG o SVG)
    karun.png  mistral.png  elnino.png  jmc.png  orsino.png  carnico.png  repost.png
  servicio-contenido.mp4                ← 01 Creación de contenido
  servicio-ads.jpg                      ← 03 Campañas
  servicio-eventos.mp4                  ← 04 Eventos
  servicio-redes-1.jpg / -2.jpg         ← 05 Redes
  servicio-web.jpg                      ← 06 Web
  cliente-elnino.mp4  cliente-orsino.mp4  cliente-jmc.mp4  cliente-carnico.mp4  cliente-mistral.mp4   ← reels (Trabajos)
  cliente-ceramica.jpg  cliente-karun.jpg                                                        ← fotos (Trabajos)
  testimonio-1.mp4 / .jpg  testimonio-2.mp4 / .jpg  testimonio-3.mp4 / .jpg
```

Si falta un archivo, la página muestra un bloque rojo con su etiqueta (o el nombre de la marca en la cinta, si falta un logo).

## Cinta de marcas

- Por defecto: banda **blanca** con los logos tal cual los exportes (con su fondo original, por ejemplo rojo sobre blanco).
- Variante oscura: en `index.html`, cambiá `class="ribbon"` por `class="ribbon ribbon--dark"`. Muestra los logos como siluetas blancas y necesita PNG/SVG con fondo transparente.
- Para sumar una marca: copiá un `<li>` del grupo en `#ribbonTrack` y cambiá el nombre y el archivo.

## Sumar un trabajo al carrusel

Copiá una tarjeta de `#trabajos` y cambiá nombre, tipo y archivo. Todas las tarjetas tienen el mismo tamaño vertical (9:14); los videos y fotos se recortan al centro.

## Cosas para editar rápido

- **WhatsApp:** buscá `5491125465526` en `index.html` (hay varios links).
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
