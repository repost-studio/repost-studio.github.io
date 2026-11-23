# Repost Studio — Landing

Sitio estático (HTML + CSS + JS) listo para GitHub Pages.

## Estructura

```
index.html
style.css
script.js
favicon.svg
assets/
  hero.mp4                  ← video del hero (10–15 s, sin audio, ~3–6 MB)
  hero.jpg                  ← imagen de respaldo / poster del hero
  servicio-contenido.mp4    ← reel vertical (sección 01)
  servicio-redes-1.jpg      ← feed de un cliente (sección 02)
  servicio-redes-2.jpg      ← historias destacadas (sección 02)
  servicio-web.jpg          ← captura de una web (sección 03)
  servicio-ads.jpg          ← resultados de campaña (sección 04)
  cliente-elnino.mp4
  cliente-ceramica.jpg
  cliente-orsino.jpg
  cliente-jmc.mp4
```

Los nombres son sugeridos: si no existe un archivo, la página muestra un bloque rojo con la etiqueta, así que se ve bien mientras vas cargando contenido. Para cambiar un archivo, editá su ruta en `index.html`.

## Publicar en GitHub Pages

1. Creá un repo (ej. `repost-studio`) y subí todos los archivos a la raíz.
2. En **Settings → Pages**, elegí **Deploy from a branch → main → / (root)**.
3. En un par de minutos queda en `https://TU-USUARIO.github.io/repost-studio/`.

## Consejos para los videos

- Comprimilos (HandBrake o `ffmpeg -i in.mp4 -vf scale=-2:720 -crf 28 -an out.mp4`). Idealmente < 5 MB cada uno.
- Imágenes en `.jpg` o `.webp`, ancho máximo ~1400 px.
- Pedí permiso a cada cliente para usar su contenido.

## Editar rápido

- **WhatsApp:** buscá `5491125465526` en `index.html` (aparece en 3 links). El texto precargado está en el parámetro `?text=`.
- **Colores:** variables al inicio de `style.css` (`--red`, `--ink`, `--paper`).
- **Duración del loader:** `1600` en `script.js`.
