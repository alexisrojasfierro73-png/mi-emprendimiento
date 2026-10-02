# Spec de desarrollo — Lienzo Vivo

## 0. Insumos y prompt para el asistente de IA

```text
Lee DESIGN.md, docs/09-spec-diseno.md y docs/10-spec-desarrollo.md.
En la carpeta stitch/ se encuentra el código exportado de Google Stitch de cada pantalla como referencia visual.
Construye el sitio web de Lienzo Vivo siguiendo exactamente docs/10-spec-desarrollo.md:
- Solo HTML5 semántico y CSS3 puro (sin Tailwind, sin frameworks pesados ni JavaScript externo).
- La estructura de archivos y nombres de páginas definidos en la spec.
- Las variables CSS en :root con los valores y tokens idénticos a DESIGN.md.
- La navegación completa y sin enlaces rotos entre Landing, Tienda, Ficha de Producto, Carrito, Blog, Artículo y páginas legales.
Al terminar, ejecuta la verificación de cada criterio de aceptación y reporta el estado de cumplimiento.
```

---

## 1. Estructura de archivos y carpetas

```text
lienzo-vivo/
├── index.html                  ← Landing page principal
├── tienda.html                 ← Catálogo de obras y galería con filtros
├── producto.html               ← Ficha de detalle de obra y selector de marco
├── carrito.html                ← Carrito de compras y calculador de despacho
├── blog.html                   ← Catálogo de artículos del taller y guías
├── articulo.html               ← Lectura de artículo individual
├── nosotros.html               ← Manifiesto del taller y proceso de la artista
├── contacto.html               ← Contacto y cotización de cuadros a medida
├── preguntas-frecuentes.html   ← Preguntas frecuentes (envíos, marcos, cuidados)
├── terminos.html               ← Términos, condiciones y garantías
├── privacidad.html             ← Política de privacidad y tratamiento de leads
├── 404.html                    ← Página de error 404
├── DESIGN.md                   ← Design system en formato YAML y especificaciones
├── README.md                   ← Portada y documentación del repositorio
├── css/
│   └── styles.css              ← Hoja de estilos centralizada con variables y responsive
├── docs/
│   ├── 01-brief.md
│   ├── 02-proto-personas.md
│   ├── 03-funcionalidades.md
│   ├── 04-tecnologias.md
│   ├── 05-arquitectura.md
│   ├── 06-moodboard.md
│   ├── 07-componentes.md
│   ├── 08-color-tipografia.md
│   ├── 09-spec-diseno.md
│   ├── 10-spec-desarrollo.md
│   ├── 11-qa.md
│   └── img/                    ← Imágenes del proyecto, avatares y mockups
└── stitch/                     ← Prototipos de referencia exportados desde Stitch
```

---

## 2. Páginas y navegación

- **Barra de navegación (`navbar`) presente en todas las páginas:** Logotipo con enlace a `index.html`, enlaces a `tienda.html`, `contacto.html`, `blog.html`, `nosotros.html` y acceso directo al carrito `carrito.html`.
- **Pie de página (`footer`) presente en todas las páginas:** Enlaces hacia `preguntas-frecuentes.html`, `terminos.html`, `privacidad.html`, formulario de contacto e información de Instagram y WhatsApp.

### Tabla de navegación entre pantallas

| Desde la página | Elemento interactivo | Conduce a la URL |
|---|---|---|
| `index.html` | Botón "Explorar Galería de Obras" en Hero | `tienda.html` |
| `index.html` | Botón "Encargar Cuadro a Medida" en Hero | `contacto.html` |
| `index.html` | Botón "Ver Obra & Medidas" en tarjetas de producto | `producto.html` |
| `index.html` | Formulario de leads ("Recibir Guía") | Confirmación visual en `index.html` |
| `tienda.html` | Botón "Ver Obra & Medidas" de cada cuadro | `producto.html` |
| `tienda.html` | Banner inferior "Cotizar Cuadro a Medida" | `contacto.html` |
| `producto.html` | Botón "Agregar al Carrito de Compras" | `carrito.html` |
| `producto.html` | Botón "Consultar por WhatsApp con la Artista" | `https://wa.me/569XXXXXXXX?text=Consulta-Duna-Serena` |
| `carrito.html` | Botón "Seguir Explorando Obras" | `tienda.html` |
| `carrito.html` | Botón "Continuar al Pago Seguro" | Simulación de pasarela de pago |
| `blog.html` | Tarjeta de artículo destacado y enlaces de lectura | `articulo.html` |
| `articulo.html` | Tarjeta de producto recomendado al final | `producto.html` |
| `articulo.html` | Botones "Compartir en WhatsApp / Pinterest" | Enlaces externos de compartir |
| `404.html` | Botón "Volver a la Galería Principal" | `index.html` |

---

## 3. Estructura semántica HTML5

### `index.html` (Landing)
```html
<header class="site-header">
  <nav class="navbar"> ... </nav>
</header>
<main>
  <section class="hero-section"> ... </section>
  <section class="values-bar"> ... </section>
  <section class="featured-artworks"> ... </section>
  <section class="studio-story"> ... </section>
  <section class="lead-capture-section"> ... </section>
</main>
<footer class="site-footer"> ... </footer>
```

### `tienda.html` (Catálogo)
```html
<header class="site-header"> <nav class="navbar"> ... </nav> </header>
<main class="store-layout">
  <header class="store-header">
    <h1>Galería de Obras Originales</h1>
    <div class="search-and-chips"> ... </div>
  </header>
  <div class="store-container">
    <aside class="store-filters"> ... </aside>
    <section class="artworks-grid">
      <article class="card-product"> ... </article>
      <!-- Repite para cada obra -->
    </section>
  </div>
</main>
<footer class="site-footer"> ... </footer>
```

### `producto.html` (Ficha de Detalle)
```html
<header class="site-header"> <nav class="navbar"> ... </nav> </header>
<main class="product-detail">
  <nav class="breadcrumbs" aria-label="Ruta de navegación"> ... </nav>
  <div class="product-layout">
    <section class="product-gallery"> ... </section>
    <section class="product-info">
      <header> <h1>...</h1> </header>
      <div class="frame-selector"> ... </div>
      <div class="purchase-actions"> ... </div>
      <div class="accordion-details"> ... </div>
    </section>
  </div>
</main>
<footer class="site-footer"> ... </footer>
```

---

## 4. Organización del CSS

### Declaración de Variables en `:root` (`css/styles.css`)

```css
:root {
  /* Paleta cromática idéntica a DESIGN.md */
  --color-primary: #B85D36;
  --color-primary-hover: #9C4A26;
  --color-on-primary: #FFFFFF;
  --color-secondary: #4A6B56;
  --color-secondary-hover: #3C5846;
  --color-on-secondary: #FFFFFF;
  --color-tertiary: #C88A3E;
  --color-tertiary-strong: #9E6723;
  --color-on-tertiary: #FFFFFF;
  --color-neutral: #FAF7F2;
  --color-surface: #F0EAE1;
  --color-surface-card: #FFFFFF;
  --color-border: #DFD5C7;
  --color-on-surface: #262320;
  --color-on-surface-muted: #665F58;
  --color-success: #3B7A57;
  --color-error: #B3392E;

  /* Tipografías de Google Fonts */
  --font-display: 'Fraunces', Georgia, serif;
  --font-body: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;

  /* Escala de espaciados */
  --space-xs: 4px;
  --space-sm: 8px;
  --space-md: 16px;
  --space-lg: 24px;
  --space-xl: 32px;
  --space-2xl: 48px;
  --space-3xl: 64px;

  /* Radios de borde */
  --radius-sm: 4px;
  --radius-md: 8px;
  --radius-lg: 16px;
  --radius-full: 9999px;

  /* Sombras y elevaciones sutiles */
  --shadow-card: 0 4px 16px rgba(38, 35, 32, 0.05);
  --shadow-card-hover: 0 10px 24px rgba(38, 35, 32, 0.10);
  --transition-smooth: all 0.25s ease-in-out;
}
```

### Convenciones y Breakpoints
- **Nomenclatura BEM/Modular en inglés o con guiones:** `.navbar`, `.hero`, `.btn-primary`, `.btn-secondary`, `.card-product`, `.frame-selector`, `.lead-form`.
- **Enfoque Mobile-First:** Reglas base aplicadas para móviles, expandiendo estilos mediante:
  - `@media (min-width: 768px)` (Tablets)
  - `@media (min-width: 1024px)` (Desktop)
  - `@media (min-width: 1200px)` (Grandes pantallas)

---

## 5. Criterios de aceptación (Checklist de QA)

### Navegación y Flujos
- [ ] La barra de navegación (`navbar`) y el pie de página (`footer`) son consistentes e idénticos en todas las páginas.
- [ ] Se puede completar el **Flujo de compra**: Landing (`index.html`) → Tienda (`tienda.html`) → Detalle de Obra (`producto.html`) → Carrito (`carrito.html`).
- [ ] Se puede completar el **Flujo de contenido**: Blog (`blog.html`) → Artículo (`articulo.html`) → Ficha de producto (`producto.html`).
- [ ] Todos los enlaces internos funcionan correctamente y no existen rutas rotas (404).

### Funcionalidades y Componentes
- [ ] La landing incluye el formulario de captación de leads con la oferta de la guía de decoración y el 10% de descuento.
- [ ] La tienda cuenta con chips de categoría interactivos, barra de búsqueda y selector de orientación y paleta de color.
- [ ] La ficha de producto cuenta con selector de tipo de marco (Bastidor, Roble, Negro), especificaciones técnicas de relieve y botón para agregar al carrito.
- [ ] La pantalla de carrito calcula el subtotal y permite ingresar comuna para cotizar el despacho seguro.
- [ ] El artículo del blog incluye botones para compartir en redes y módulo de comentarios.

### Diseño y Estilos
- [ ] Todos los colores y tipografías provienen de las variables de `:root` declaradas en `DESIGN.md`.
- [ ] El precio en pesos chilenos y las medidas en centímetros son visibles en todas las tarjetas de cuadro (`card-product`).
- [ ] Todos los botones cuentan con estados visuales `hover` y `active` accesibles.
- [ ] No se utilizan frameworks CSS pesados externos; todo el código es HTML5 y CSS3 nativo.

### Responsive y Accesibilidad
- [ ] En pantallas móviles (375px), el catálogo muestra 1 columna de obras y no presenta scroll horizontal involuntario.
- [ ] En pantallas desktop (1024px+), el catálogo se distribuye ordenadamente en 3 columnas con barra lateral de filtros.
- [ ] Todas las imágenes contienen atributos `alt` descriptivos de la obra y su técnica.
- [ ] Cada página HTML cuenta con un único encabezado principal `<h1>` con jerarquía semántica correcta.
- [ ] El sitio está preparado para su publicación en GitHub Pages.
