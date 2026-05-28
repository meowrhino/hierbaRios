# hierbaRios

7 pruebas generativas de un fondo web responsive con tema **hierba y ríos**, inspirado en la vista de mapa de Los Sims / SimCity.

Cada prueba ataca el problema desde un stack y estética distintos. Todas son **HTML autocontenido**, **responsive**, y llevan **audio procedural** generado con Web Audio API (sin samples externos).

## Demo

→ **[https://meowrhino.github.io/hierbaRios](https://meowrhino.github.io/hierbaRios)**

## Las 7 pruebas

| # | Estética | Stack |
|---|----------|-------|
| 1 | Pixel art isométrico (Sims) | Canvas 2D · vanilla JS |
| 2 | Top-down animado | Pixi.js + fragment shader GLSL |
| 3 | 3D realista | Three.js (ortho-iso, briznas instanciadas, agua shader) |
| 4 | Acuarela / painterly | p5.js |
| 5 | Vectorial estilizado | SVG nativo + marching squares + filtros |
| 6 | Ilustrado a mano | rough.js (sketchy lines, hachured fills) |
| 7 | Y2K tropical paradise ★ | Canvas + CSS maximalista |

## Cómo se usa

- Click en el overlay inicial para activar el audio (política autoplay del navegador)
- Botón **nuevo seed** → regenera el mapa
- Botón **mute** → silencia el audio
- Refresca para una nueva semilla aleatoria

## Lo común a todas

- Generación basada en **simplex noise + fbm** (con seed reproducible)
- **Ridged noise** para los ríos (winding natural)
- **Decoración condicional**: árboles solo en hierba, lejos de orillas
- **Audio procedural**: agua (ruido marrón + bandpass), viento (ruido rosa + LFO), pájaros/grillos (osciladores cortos)
- **Responsive**: regenera o reajusta al resize

## Estructura

```
.
├── index.html                       # galería con previews
├── prueba-1-canvas-pixel-iso.html
├── prueba-2-pixi-shaders.html
├── prueba-3-threejs-3d.html
├── prueba-4-p5-acuarela.html
├── prueba-5-svg-vectorial.html
├── prueba-6-roughjs-ilustrado.html
└── prueba-7-y2k-tropical.html
```
