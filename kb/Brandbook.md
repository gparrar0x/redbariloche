# Brandbook — Red Bariloche

Este documento consolida los lineamientos de marca y UI para Red Bariloche. Sirve como guía para diseño, contenidos y desarrollo front-end.

## Identidad
- Red colaborativa local que conecta comercios, experiencias y comunidad.
- Tono: cercano, claro, optimista. Evitar tecnicismos innecesarios. Priorizar verbos de acción.

## Paleta cromática
- Morado principal: `#5B2C83`
- Morado acento: `#7300A0`
- Blanco: `#FFFFFF`
- Overlay oscuro: `rgba(0,0,0,0.55)`
- Panel translúcido: `rgba(255,255,255,0.45)` hasta `rgba(255,255,255,0.70)` según contraste

Recomendaciones de contraste:
- Texto sobre morado: usar blanco puro y aumentar peso tipográfico (500–700).
- Panel translúcido sobre imagen: subir opacidad a 0.6–0.7 si el fondo es complejo.

## Tipografía
- Primaria: Roboto (100–900). Import ya presente en el sitio (`Liberty`).
- Jerarquías sugeridas:
  - H1/H2: 600–700.
  - H3/H4: 500–600.
  - Párrafos/labels: 400–500.

## Logo
- Archivo principal: `Liberty/assets/images/logo-transparente.png` (origen en `Helios/images/logo-transparente.png`).
- Usos recomendados: sobre fondo blanco o sobre overlay oscuro.
- Área de seguridad: margen mínimo igual a la altura de la “R”.
- No distorsionar, no cambiar colores, no aplicar sombras extras.

## Componentes UI

### Header
- Clases: `header-area header-sticky rb-transparent`.
- Comportamiento: transparente en top; al scrollear, se quita `rb-transparent` y aparece gradiente morado.
- Enlaces del menú: todos con el mismo estilo de “Home” (blanco, subrayado/acento en hover/activo).

### Hero
- Fondo por defecto (`Liberty`): `assets/images/heading-bg.jpg`.
- Alternativa (`Helios`): `Helios/images/header.jpg`.
- Overlay: `rgba(0,0,0,0.55)`.
- Panel “glass”: fondo translúcido + blur, bordes 16 px.
- CTAs:
  - Primario: fondo morado principal, hover acento.
  - Secundario ghost: borde morado, fondo transparente.

### Cards translúcidas
- Fondo: `rgba(255,255,255,0.45)`; ajustar 0.60–0.70 cuando el fondo lo requiera.
- Sombra suave: `0 10px 30px rgba(0,0,0,0.25)`.

### Carousel de comercios
- Ítems actuales: Superhotdog, Panadería Maná, Meraki Café, Vani Gambarte Studio.
- Imágenes: actualmente referenciadas desde `Helios/images/*.jpg`. Sugerido migrarlas a `Liberty/assets/images/` para independencia.
- Cada ítem incluye logo, título, breve descripción y CTA “Ir a …”.

## Accesibilidad
- Contraste mínimo AA para texto y botones.
- Tamaño de fuente base ≥ 16 px. No depender del color para transmitir estado.
- Foco visible en enlaces/CTAs (outline o subrayado reforzado).

## Voz y contenido
- Hablar en plural (“conectamos, impulsamos”).
- Priorizar beneficios y claridad: qué obtiene el usuario/comercio.
- Evitar lorem ipsum y textos genéricos en producción.

## Assets y rutas
- Logos comercios: `Helios/images/` (migrar a `Liberty/assets/images/` cuando se consolide).
- Fondos hero: `Liberty/assets/images/heading-bg.jpg`.
- Webfonts e íconos: ya incluidos por template (`vendor`, `assets/webfonts`).

## Tokens de marca (CSS variables usadas en `index.html`)
```css
:root {
  --rb-purple: #5B2C83;
  --rb-accent: #7300A0;
  --rb-white: #FFFFFF;
  --rb-overlay: rgba(0,0,0,0.55);
  --rb-card: rgba(255,255,255,0.45);
}
```

## Do/Don’t
**Hacer**
- Usar overlay en fotografías de hero para legibilidad.
- Mantener el header transparente en top y sólido al scrollear.
- Reutilizar tokens/variables de color.

**No hacer**
- Cambiar colores corporativos sin revisión.
- Forzar sombras/efectos que alteren legibilidad del logo.
- Mezclar tipografías sin criterio.

## Exportar a PDF
- Abrir este documento y exportar a PDF desde el editor (Markdown → Export/PDF), o usar:
```bash
pandoc kb/Brandbook.md -o kb/Brandbook.pdf
```

## Contacto
Para nuevas piezas o dudas de implementación, actualizar `Liberty/index.html` y este Brandbook.





