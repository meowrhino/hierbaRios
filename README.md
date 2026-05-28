# hierbaRios

12 pruebas generativas de un fondo web responsive con tema **hierba y ríos**, inspirado en la vista de mapa de Los Sims / SimCity, mapas ilustrados de parques de atracciones, la app Forest, y estética Y2K.

Cada prueba ataca el problema desde un stack y estética distintos. Todas son **HTML autocontenido**, **responsive**, y llevan **audio procedural** generado con Web Audio API (sin samples externos).

## Demo

→ **[https://meowrhino.github.io/hierbaRios](https://meowrhino.github.io/hierbaRios)**

## Las 12 pruebas

### 🎮 Videojuego / Pixel
| # | Stack | Estética |
|---|-------|----------|
| 01 | Canvas 2D · vanilla JS | Pixel iso Sims (sombras, 4 variantes de árbol, agua animada) |
| 02 | Pixi.js + GLSL | Top-down animado con shaders |

### 🌿 3D / Realista
| # | Stack | Estética |
|---|-------|----------|
| 03 | Three.js | Ortho-iso, briznas instanciadas, agua shader |
| 08 | Three.js + GLSL | Iso 3D con todo el terreno animado (híbrido 02+03) |
| 11 | Three.js | **Forest hex-tile** — hexágonos flotantes con clusters multi-bioma |
| 12 | Three.js | Variante primavera: cerezos en flor + pétalos cayendo |

### 🎨 Diseño / Arte
| # | Stack | Estética |
|---|-------|----------|
| 04 | p5.js | Acuarela painterly |
| 05 | SVG nativo | Marching squares + patrones + filtros de turbulencia |

### 🖍️ Ilustrado a mano
| # | Stack | Estética |
|---|-------|----------|
| 06 | rough.js | Mapa de parque estilo PortAventura |
| 09 | rough.js | **Bosque denso** sin río, con estanque |
| 10 | rough.js + canvas | **Nocturno** con luna, linternas y luciérnagas |

### ★ Y2K / Web-culture
| # | Stack | Estética |
|---|-------|----------|
| 07 | canvas + CSS | Paradise maximalista (marquee, badges, contador) |
| 07b | canvas | **Paradise limpio** — solo fondo, sin chrome |

## Cómo se usa

- Click en el overlay inicial para activar el audio (política autoplay del navegador)
- Botón **nuevo seed** → regenera el mapa
- Botón **mute** → silencia el audio
- Refresca para una semilla aleatoria

## Lo común a todas

- Generación basada en **simplex noise + fbm** con seed reproducible
- **Ridged noise** para los ríos (winding natural)
- **Decoración condicional**: árboles solo en hierba, lejos de orillas
- **Audio procedural** distinto por prueba (agua, viento, pájaros, grillos, ranas, búhos, koto, synth pad…)
- **Responsive**: regenera o reajusta al resize
