Café Aurora — Proyecto estático (HTML + CSS)

Créditos
--------
Diseño y desarrollo: Diego Alonso Chiang Meléndez

Resumen
-------
Sitio web estático para un café de especialidad, pensado como entrega de Coderhouse. Sin JavaScript: toda la interactividad es con HTML/CSS (checkbox hack). Diseño desktop-first con adaptación mobile.

Puntos clave de esta versión
----------------------------
- Navbar desktop con variante mobile (hamburguesa → “X”) sin JS.
- Menú mobile desplegable a **todo el ancho**, pegado al header (sin gaps) y con una **línea superior negra**.
- Tablas del Menú con encabezado `position: sticky`, envoltorio `.table-wrap` y **scroll horizontal solo en mobile** (`min-width` condicional).
- Paleta y tipografía en CSS tokens y valores fijos; animaciones suaves (`fade-up`) y transiciones en CTA/cards.
- Formularios accesibles (focus visible, labels, `fieldset/legend`), sin validación JS.
- Rutas relativas consistentes en todas las páginas.

Estructura del proyecto
-----------------------
- **Raíz**
  - `index.html`
  - `css/`
    - `style.css` — archivo único de estilos compilados
  - `scss/` — fuentes Sass (opcional)
    - `_variables.scss` — tokens (colores, radios, sombras, BP, fuentes)
    - `_mixins.scss` — mixin container, utilidades
    - `_base.scss` — reset, tipografía, elementos base y :root (literal)
    - `_layout.scss` — header/nav, hero, grids, mosaico
    - `_components.scss` — cards, CTA, tablas, listas, formularios, sedes
    - `_utilities.scss` — `.table-wrap`, helpers de espaciado, `.flow`
    - `_animations.scss` — keyframes y transiciones
    - `main.scss` — punto de entrada
  - `pages/`
    - `menu.html`, `sedes.html`, `reservas.html`, `sobre.html`, `contacto.html`
  - `assets/`
    - `wireframes/` — imágenes de wireframe / placeholders
    - `img/` — logos, fotos, mapas, etc.

Tecnologías
-----------
- HTML5 semántico
- CSS3 (Grid/Flex, `clamp`, `position: sticky`)
- Sass (opcional): sintaxis SCSS para modularizar
- Sin JavaScript

Guía de estilos (tokens)
------------------------
- Colores base:
  - Texto: #1C1C1C
  - Fondo: #F7F4F0
  - Superficie (tarjetas): #FFFFFF
  - Muted: #6A6A6A
  - Borde: #E5E1DC
  - Acents: #7A4E2D / #A1663D (hover)
- Radios: 14px (cards/tablas), 10px (chips/list items)
- Sombra base: 0 1px 2px rgba(0,0,0,.06), 0 6px 24px rgba(0,0,0,.06)
- Tipografía: sistema (system-ui stack)

Comportamiento responsive
-------------------------
- Desktop-first. Punto de quiebre principal: 48rem (~768px).
- Navbar:
  - Desktop: lista horizontal.
  - Mobile (<48rem): input `#nav-toggle` + label `.burger`. El menú:
    - Ocupa todo el ancho (`left:0; right:0; top:100%`), sin `100vw` (evita overflow).
    - Links centrados y espaciados.
    - Ícono hamburguesa anima a “X” con `::before/::after`.
- Tablas del Menú:
  - Wrapper `.table-wrap` con `overflow-x:auto` y `-webkit-overflow-scrolling:touch`.
  - `.tabla-menu` usa `min-width:560px` **solo en mobile**.
  - `thead th` sticky.

Accesibilidad
-------------
- Enlaces y botones con `:focus-visible` notorio.
- Contraste adecuado en textos/CTAs.
- Navegación por teclado en el menú (checkbox + label).
- Semántica: `header/nav/main/section/footer`, `fieldset/legend`, `caption` en tablas.

Animaciones y transiciones
--------------------------
- Keyframe `fade-up` en `.hero .hero-texto` y `.card` (0.45s, ease).
- Transiciones en `.cta`/`.card`/links (color, sombra). `.cta:active` aplica leve `scale(0.98)`.
- El menú mobile aparece/desaparece sin animación del panel (opcional agregar opacidad/translate).

Convenciones HTML/CSS adoptadas
-------------------------------
- Sin JS, sin frameworks CSS.
- Desktop-first con media queries a `max-width:47.99rem` y `min-width` donde corresponde.
- Rutas relativas entre páginas: `../pages/...`, `../css/style.css` desde `/pages`.
- `main > *` aplica el contenedor; por eso cada sección cuelga **directamente** de `<main>` (sin un wrapper extra).
