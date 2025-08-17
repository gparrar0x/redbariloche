Red Bariloche – Sitio y Brandbook

Visión general
Red Bariloche es una red colaborativa que conecta comercios, experiencias y comunidad local. Este repositorio contiene dos implementaciones de front-end (Helios y Liberty) usadas como base para el sitio, además de los assets y el brandbook operativo.

Estructura del proyecto
- `Helios/`: template base (HTML5 UP) con assets y páginas de ejemplo.
- `Liberty/`: sitio activo con el branding de Red Bariloche.
  - `Liberty/index.html`: home con hero, comercios y servicios.
  - `Liberty/assets/`: estilos, imágenes y JS.
- `kb/`: conocimiento y documentación auxiliar.

Cómo correr localmente
```bash
python3 -m http.server 8000 --directory "."
# Abrir: http://localhost:8000/Liberty/
```

Brandbook (Guía rápida)
Identidad y propósito
- Somos una red colaborativa local: potenciamos comercios, experiencias y servicios en Bariloche.
- Tono: cercano, claro, en primera persona del plural. Enfoque en impacto local y comunidad.

Paleta de color
- Morado principal: `#5B2C83`
- Morado acento: `#7300A0`
- Blanco: `#FFFFFF`
- Overlay oscuro: `rgba(0,0,0,0.55)`
- Panel translúcido (card): `rgba(255,255,255,0.45)` con variantes a `0.70` según contraste

Tipografía
- Liberty: `Roboto` (Google Fonts)
- Helios: `Source Sans Pro` (Google Fonts)

Iconografía y webfonts
- Font Awesome ya incluido en ambos templates.

Logo y uso
- Principal: `Helios/images/logo-transparente.png` (copiado en `Liberty/assets/images/logo-transparente.png`).
- Usos recomendados: sobre fondo blanco o sobre overlay oscuro. Mantener área de respiro equivalente a la altura de la “R”.
- No alterar proporciones ni aplicar sombras adicionales (el header usa un sutil drop-shadow para legibilidad).

Componentes UI clave
- Header
  - En `Liberty/index.html` el header utiliza clases `header-area header-sticky rb-transparent`.
  - Comportamiento: transparente al inicio; al scrollear se vuelve sólido (gradiente morado). Lógica en `Liberty/assets/js/custom.js` (toggle de clase `rb-transparent`).
  - Navegación: todos los links comparten el estilo activo (color blanco + subrayado con acento morado en hover/activo).

- Hero
  - Fondo: `Liberty/assets/images/heading-bg.jpg` (en Helios existe `Helios/images/header.jpg`).
  - Overlay: `rgba(0,0,0,0.55)`.
  - Panel central translúcido con blur (glassmorphism) para título/CTAs.

- Botones
  - Primario: morado principal sobre fondo blanco (`#5B2C83` → hover `#7300A0`).
  - Secundario “ghost”: borde morado, fondo transparente.

- Cards translúcidas
  - Fondo: `rgba(255,255,255,0.45)` (elevar a 0.6–0.7 cuando el fondo sea complejo para asegurar contraste AA).

Secciones del sitio (Liberty)
- Comercios (carousel)
  - Items: Superhotdog, Panadería Maná, Meraki Café, Vani Gambarte Studio.
  - Imágenes de logo referenciadas desde `Helios/images/*.jpg` (pueden migrarse a `Liberty/assets/images/` si se desea independencia total).
  - Páginas por comercio en `Liberty/negocios/` (derivadas de Helios con títulos e imágenes ajustadas).

- Servicios de Red Bariloche
  - Ubicación: bloque “Servicios de Red Bariloche” en `Liberty/index.html` (antes “Create Your NFT …”).
  - Items actuales:
    1) Estrategia y Producto
    2) Activación de Comercios
    3) Marketing y Contenidos

Convenciones de código
- HTML/CSS/JS plano; mantener estilos locales dentro de `index.html` al mínimo y promover moverlos a hojas dedicadas si crecen.
- Evitar mezclar tabs/espacios; respetar el estilo existente.
- Usar rutas absolutas cuando se comparten assets entre `Helios/` y `Liberty/`.

Roadmap sugerido
- Migrar logos de comercios a `Liberty/assets/images/` y actualizar rutas.
- Internacionalización de textos (ES/EN) con llaves simples.
- SEO: metadatos, OG tags, favicon y sitemap.
- Accesibilidad: contraste y foco visible en todos los CTA.

Licencias y créditos
- Templates base: HTML5 UP (Helios) y TemplateMo (Liberty). Revisar licencias incluidas en sus directorios.

Contacto
- Para actualizaciones de branding o incorporación de nuevos comercios/servicios, editar `Liberty/index.html` y los archivos en `Liberty/negocios/`.


