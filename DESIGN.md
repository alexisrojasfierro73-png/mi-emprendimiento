---
version: alpha
name: Lienzo Vivo
colors:
  primary: "#1A4B75"
  primary-hover: "#0E3354"
  on-primary: "#FFFFFF"
  secondary: "#2B7A9E"
  secondary-hover: "#1E5C79"
  on-secondary: "#FFFFFF"
  tertiary: "#D98A3C"
  tertiary-strong: "#B56B24"
  on-tertiary: "#FFFFFF"
  neutral: "#FFFFFF"
  surface: "#F0F5F9"
  surface-card: "#FFFFFF"
  border: "#D2E0EB"
  on-surface: "#14212D"
  on-surface-muted: "#536B7E"
  success: "#267A5E"
  error: "#B83636"
typography:
  headline-display:
    fontFamily: Fraunces
    fontSize: 48px
    fontWeight: 600
    lineHeight: 1.15
  headline-lg:
    fontFamily: Fraunces
    fontSize: 34px
    fontWeight: 600
    lineHeight: 1.25
  title-md:
    fontFamily: Fraunces
    fontSize: 22px
    fontWeight: 600
    lineHeight: 1.3
  body-lg:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: 400
    lineHeight: 1.6
  body-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.6
  body-sm:
    fontFamily: Inter
    fontSize: 13px
    fontWeight: 500
    lineHeight: 1.4
  label-md:
    fontFamily: Inter
    fontSize: 15px
    fontWeight: 600
    lineHeight: 1.0
rounded:
  sm: 4px
  md: 8px
  lg: 16px
  full: 9999px
spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  2xl: 48px
  3xl: 64px
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 14px 28px
  button-primary-hover:
    backgroundColor: "{colors.primary-hover}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 14px 28px
  button-primary-active:
    backgroundColor: "{colors.primary-hover}"
    textColor: "{colors.on-primary}"
  button-primary-disabled:
    backgroundColor: "{colors.border}"
    textColor: "{colors.on-surface-muted}"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 12px 26px
  button-secondary-hover:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.primary-hover}"
  card-product:
    backgroundColor: "{colors.surface-card}"
    textColor: "{colors.on-surface}"
    typography: "{typography.title-md}"
    rounded: "{rounded.md}"
    padding: "{spacing.md}"
  badge-technique:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.on-secondary}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.full}"
    padding: 4px 12px
  tag-offer:
    backgroundColor: "{colors.tertiary-strong}"
    textColor: "{colors.on-tertiary}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.full}"
    padding: 4px 10px
  filter-chip:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.full}"
    padding: 8px 18px
  filter-chip-active:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.full}"
    padding: 8px 18px
---

## Overview

Lienzo Vivo es un taller y galería online de cuadros de autor pintados 100% a mano con relieves y texturas táctiles sobre lienzo. Su usuaria principal es Sofía Valenzuela, una arquitecta e interiorista que busca piezas con alma, autenticidad y calidez para proyectos residenciales y para su propio hogar.

El estilo visual es orgánico, cálido, contemporáneo, sobrio y refinado (*japandi / minimalismo cálido*), combinando la serenidad de tonos tierra con tipografía editorial de galería de arte.

## Colors

- **Primary (`#1A4B75` - Azul Océano Profundo):** Color insignia de la marca. Se utiliza en titulares destacados, botones de compra principales, llamadas a la acción y enlaces clave.
- **Primary Hover (`#0E3354` - Azul Marino Noche):** Variante de oscurecimiento para estados hover y botones activos.
- **Secondary (`#2B7A9E` - Azul Turquesa / Brisa Marina):** Badges de técnicas artesanales, sellos y detalles interactivos.
- **Tertiary Strong (`#B56B24` - Arena Dorada / Atardecer):** Etiquetas de promociones, insignias de "Pieza Única de Autor" y acentos cálidos.
- **Neutral (`#FFFFFF` - Blanco Puro):** Fondo principal del sitio web para proporcionar máxima luminosidad, limpieza y contraste.
- **Surface (`#F0F5F9` - Espuma Marina / Blanco Costero):** Fondo de contenedores secundarios, barras de filtros, módulos y pie de página.
- **On-Surface (`#14212D` - Azul Noche Carbón):** Color principal de títulos, encabezados y textos de párrafo de alta legibilidad.
- **On-Surface Muted (`#536B7E` - Gris Marino):** Medidas en centímetros, fechas, categorías y textos auxiliares.

## Typography

- **Títulos y Encabezados:** `Fraunces` — tipografía con serifa de corte artesanal y gran personalidad para titulares `h1`, `h2` y nombres de obras `h3`.
- **Cuerpo y Elementos de UI:** `Inter` — tipografía de alta legibilidad, empleada en descripciones de obra, fichas técnicas, formularios, botones y calculadores de despacho.
- **Jerarquía:** 
  - `headline-display`: 48px / 1.15 (Hero)
  - `headline-lg`: 34px / 1.25 (Secciones principales)
  - `title-md`: 22px / 1.3 (Títulos de tarjeta de producto y artículos)
  - `body-md`: 16px / 1.6 (Cuerpo de texto regular)
  - `body-sm`: 13px / 1.4 (Metadatos, medidas y badges)

## Layout

- **Ancho máximo del contenedor:** `1200px` centrado con márgenes laterales dinámicos.
- **Breakpoints responsive:**
  - **Mobile:** `< 768px` (1 columna en catálogo de productos, menú móvil colapsable, espaciado lateral de 16px).
  - **Tablet:** `768px` a `1023px` (2 columnas en catálogo de productos, espaciado lateral de 24px).
  - **Desktop:** `≥ 1024px` (3 columnas en catálogo de obras, barra lateral de filtros fija de 260px, espaciado lateral de 32px).
- **Espaciados consistentes:** Se utiliza la escala de espaciado `xs: 4px`, `sm: 8px`, `md: 16px`, `lg: 24px`, `xl: 32px`, `2xl: 48px`, `3xl: 64px`.

## Elevation & Depth

- **Superficies planas con bordes orgánicos:** La interfaz no abusa de sombras artificiales pesadas. Se prioriza la delimitación sutil mediante bordes de `1px solid #DFD5C7` y fondos `#F0EAE1`.
- **Hover de Tarjetas de Producto:** Elevación suave de `0 8px 24px rgba(38, 35, 32, 0.08)` combinada con un aumento de escala del 102% en la imagen de la obra.

## Shapes

- **Botones y Chips:** Redondeo completo tipo píldora (`rounded.full: 9999px`) para generar cercanía y suavidad visual.
- **Tarjetas de Producto y Módulos:** Redondeo medio (`rounded.md: 8px`) que enmarca las obras de arte emulando la geometría de un bastidor.
- **Imágenes de Cuadro:** Esquinas suavemente redondeadas (`rounded.sm: 4px`) para emular lienzos tensados sobre madera.

## Components

### 1. Barra de Navegación (`navbar`)
Contiene logotipo tipográfico "Lienzo Vivo", navegación (Inicio, Tienda, Cuadros a Medida, Blog, Taller), barra de búsqueda compacta e ícono de carrito con contador. Se fija en la parte superior con fondo semitransparente con desenfoque de fondo (*backdrop-filter: blur(8px)*).

### 2. Tarjeta de Producto (`card-product`)
- Contenedor con fondo blanco, borde sutil y padding de 16px.
- Imagen del cuadro en proporción cuadrada o 4:5 con zoom sutil al pasar el mouse.
- Badge de técnica artesanal (ej. "Textura en Relieve") posicionado sobre la esquina superior izquierda.
- Nombre de la obra en `title-md` (máximo 2 líneas).
- Dimensiones reales en cm (ej. `100 x 120 cm`) en `on-surface-muted`.
- Precio visible en pesos chilenos en negrita (ej. `$189.000 CLP`).
- Botón secundario "Ver Obra & Medidas".
- **Estado Agotado:** Imagen con filtro desaturado al 80% y botón deshabilitado "Vendido (Disponible por encargo)".

### 3. Filtros de Tienda (`filter-bar` y `filter-chip`)
Chips horizontales redondeados con estado normal (fondo arena) y estado activo (fondo terracota con texto blanco).

### 4. Selector de Enmarcado (`frame-selector`)
Muestrarios seleccionables en radio-buttons estilizados con fotos en miniatura de la madera (Bastidor simple, Marco Roble Natural, Marco Negro).

### 5. Formulario de Captación de Leads (`lead-form`)
Caja destacada con fondo `#F0EAE1`, borde orgánico, campo de entrada de texto con placeholder claro y botón de envío principal tipo píldora.

## Do's and Don'ts

### Do's (Prácticas recomendadas)
- ✅ **Mostrar siempre las dimensiones y técnica** en cada tarjeta de cuadro.
- ✅ **Usar imágenes reales** con iluminación natural donde se perciba el relieve de la pasta y las pinceladas.
- ✅ **Mantener los botones principales** con texto blanco sobre terracota (`#B85D36`) para asegurar accesibilidad WCAG AA.
- ✅ **Asegurar espaciados amplios** y blancos respirables entre secciones para emular la experiencia de una galería de arte física.

### Don'ts (Prácticas prohibidas)
- ❌ **No usar sombras negras intensas** o degradados de color chillones que desentonen con la estética orgánica y natural.
- ❌ **No usar tipografía `Fraunces` decorativa en textos largos de párrafo o formularios**, ya que reduce la legibilidad en pantallas pequeñas.
- ❌ **No ocultar el precio ni los costos de despacho** detrás de formularios o pop-ups intrusivos.
- ❌ **No vender impresiones digitales** ni referirse a las obras como "posters" o "láminas".
