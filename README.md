
# Café Aurora — Versión Final

**Autor:** Diego Alonso Chiang Meléndez  
**Descripción:** Sitio web estático de una cafetería de especialidad. Implementa HTML5 semántico, CSS nativo (Grid/Flex) y uso selectivo de Bootstrap en partes clave para cumplir el criterio de framework sin perder la identidad visual. Incluye optimizaciones de SEO, accesibilidad y rendimiento.
**Link del repositorio de Github:** https://github.com/DiegoChiang/Coderhouse_Proyecto
**Link de la web alojada en servidor de Vercel:** https://coderhouse-proyecto-ecru.vercel.app/
**Link de la web alojada en servidor de Github Pages:** https://diegochiang.github.io/Coderhouse_Proyecto/
---

## Alcance y páginas

- **Inicio**: portada con hero, navegación y mosaicos; estilo propio con CSS Grid y Flexbox.  
- **Menú**: listado de productos y precios; se usan componentes y utilidades de Flexbox.  
- **Sedes**: presentación de locales; se emplean tarjetas y grilla responsiva de Bootstrap.  
- **Reservas**: formulario con controles accesibles y validación nativa; maquetación responsiva con el sistema de grillas de Bootstrap.  
- **Sobre** y **Contacto**: contenido institucional y formulario de contacto; mantienen el estilo nativo.

> Bootstrap se aplica **solo** en Sedes y Reservas, mientras que Inicio, Menú, Sobre y Contacto conservan el layout nativo para evidenciar dominio de CSS puro.

---

## Tecnologías y decisiones

- **HTML5 semántico**: estructura clara con encabezados jerárquicos y secciones bien delimitadas.  
- **CSS nativo (Grid/Flex)**: layouts propios, tipografía y diseño visual consistente con la marca.  
- **Bootstrap 5 **: uso acotado para tablas, formularios, tarjetas y grillas en 2 páginas.  
- **Hojas de estilo de apoyo**:  
  - *bootstrap-aurora.css*: adapta Bootstrap a la paleta/espaciados de la marca.  
  - *bootstrap-helpers.css*: utilidades ligeras para separar contenido y mejorar consistencia.  
  - *bootstrap-pages.css*: ajustes por página para integrar Bootstrap sin romper el estilo existente.  

---

## SEO aplicado (resumen)

- **Titulado y descripción únicos por página** para mejorar pertinencia en buscadores.  
- **URL canónica** autorreferente en cada documento para consolidar señales de ranking.  
- **Metadatos sociales** (Open Graph y Twitter) con título, resumen y una imagen compartible. 
- **Color de tema del navegador** para móviles, favicons e íconos para diferentes plataformas.  

---

## Accesibilidad (resumen)

- **Navegación por teclado** fluida con enfoque visible.  
- **Skip link** visible al enfocar.  
- **Menú móvil** con control anunciable para tecnologías de asistencia.  
- **Etiquetas de formularios** conectadas a sus campos y autocompletado activado.  
- **Tablas** con encabezados de columna identificados y descripciones breves.  
- **Texto alternativo** en imágenes significativas; imágenes decorativas marcadas como tales.

---

## Rendimiento y buenas prácticas

- **Imágenes**: tamaños adecuados, compresión y carga diferida en contenidos no críticos.  
- **Fuentes**: criterio en el número de variantes y comportamiento apropiado de carga.  
- **Orden de estilos**: el framework y las hojas de apoyo van antes del estilo principal para facilitar sobrescrituras controladas.  
- **Evitar desbordes**: pruebas en anchos comunes desde móvil pequeño hasta escritorio amplio.

---

## Estructura del repositorio (descripción)

- Carpeta en la raíz con la página principal.  
- Carpeta de páginas con los documentos internos del sitio.  
- Carpeta de estilos con la hoja principal y los archivos de integración de Bootstrap.  
- Carpeta de assets con íconos y recursos gráficos.  

---

## Cambios destacados respecto a la versión previa

- Integración del framework en secciones seleccionadas para evidenciar su uso sin sustituir todo el diseño.  
- Metadatos SEO y sociales por página, con pautas de imágenes compartibles.  
- Mejoras de accesibilidad en navegación, formularios e imágenes.  
- Medidas de rendimiento enfocadas en estabilidad visual y tiempos de carga.  
- Organización de estilos en capas: framework, ayudas y hoja principal.

---

## Créditos y licencia

Proyecto académico con fines educativos.  
Diseño y desarrollo: Diego Alonso Chiang Meléndez.
