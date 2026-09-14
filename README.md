# HELIOS — Explorador del Sistema Solar

Viaje 3D interactivo por los 8 planetas con órbitas, scroll cinematográfico y fichas de datos. Hecho con Three.js y desplegado en GitHub Pages.

🌍 Live: https://andyechc.github.io/lumen-site/

## Qué es

- Escena Three.js con Sol, 8 planetas, anillos de Saturno/Urano, nubes de la Tierra, estrellas y polvo orbital.
- La cámara viaja planeta por planeta al hacer scroll (click en un planeta o en los dots para saltar).
- Fichas con diámetro, gravedad, día, año, temperatura, lunas y distancia, en 4 idiomas (ES / EN / 中 / RU).
- Sonido ambiente drone opcional (Web Audio API).

## Tech stack

- Three.js r160 (ES Modules + Import Map vía unpkg + es-module-shims)
- HTML5 + CSS3 + JavaScript (un solo `index.html`, sin build)
- Texturas: `ofrohn/threex.planets` (MIT) · datos NASA/USGS · CC BY 4.0
- Hosting: GitHub Pages (rama `gh-pages`) · CI: workflow "Escucha de Push" en cada push a `main`

## Desarrollo local

```bash
# opción 1: abrir directo (los CDN necesitan internet)
open index.html
# opción 2: servir local
python3 -m http.server 8080
# -> http://localhost:8080/index.html
```

## Despliegue

- Rama de trabajo: `main`. Rama publicada: `gh-pages` (mirror de `main`).
- Cada push a `main` dispara el workflow `.github/workflows/push-listener.yml` y hay que espejar a `gh-pages`:

```bash
git push origin main
git push origin main:gh-pages
```

## Créditos

Hecho por [andyechc](https://github.com/andyechc) · HELIOS — Explorador del Sistema Solar.
