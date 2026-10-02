# Arquitectura de la información — Lienzo Vivo

## 1. Mapa de sitio (Sitemap)

```text
Inicio (index.html — Landing Page)
├── Tienda (tienda.html — Catálogo de Obras)
│   ├── Categoría: Cuadros Texturados & Relieve (filtrado en vista)
│   ├── Categoría: Óleos y Acrílicos Botánicos (filtrado en vista)
│   ├── Categoría: Abstractos & Minimalistas (filtrado en vista)
│   ├── Categoría: Dípticos y Grandes Formatos (filtrado en vista)
│   ├── Ficha de Producto (producto.html — Detalle de Obra y Enmarcado)
│   └── Carrito de Compras (carrito.html — Resumen y Despacho)
├── Blog & Inspiración (blog.html — Artículos de Taller y Decoración)
│   ├── Categoría: Guías de Decoración & Escala (filtrado en vista)
│   ├── Categoría: Texturas, Técnicas y Materiales (filtrado en vista)
│   ├── Categoría: Procesos del Taller y Cuidado de Obras (filtrado en vista)
│   └── Artículo Individual (articulo.html — Lectura y Productos Recomendados)
├── Sobre el Taller & Artista (nosotros.html — Manifiesto y Proceso Creativo)
├── Contacto & Cuadros a Medida (contacto.html — Formulario y WhatsApp)
├── Preguntas Frecuentes (preguntas-frecuentes.html — Envíos, Cuidados, Marcos)
├── Términos y Condiciones (terminos.html — Políticas de Compra y Garantía)
├── Política de Privacidad (privacidad.html — Tratamiento de Datos y Leads)
└── Página de Error 404 (404.html — Página no encontrada con retorno guiado)
```

---

## 2. Flujos de usuario (User Flows)

### Flujo 1: Flujo de compra (Adquisición de obra de arte original)

```text
Instagram (Historia con video mostrando la textura en relieve a la luz)
→ Landing Page (index.html)
→ [Clic en botón principal "Explorar Galería de Obras"]
→ Tienda (tienda.html)
→ [Aplica filtro por "Cuadros Texturados" y orientación "Vertical 100x120 cm"]
→ [Selecciona la obra "Duna Serena — Textura Orgánica"]
→ Ficha de Producto (producto.html)
→ [Revisa fotos en macro del relieve y visualiza la obra sobre un sofá de 3 cuerpos]
→ [Selecciona la opción de enmarcado: "Marco Flotante en Madera de Roble"]
◇ ¿Tiene dudas sobre la combinación o medidas de su muro?
   ├── Sí → [Clic en botón secundario "Consultar por WhatsApp"] → Conversación directa en WhatsApp con la artista
   └── No → [Clic en botón principal "Agregar al Carrito"]
→ Carrito de Compras (carrito.html)
→ [Ingresa su comuna (ej. "Providencia") y selecciona "Despacho Premium con Embalaje en Madera"]
→ Fin: Carrito listo para proceder al checkout y pago
```

### Flujo 2: Flujo de contenido (De artículo de blog a captación de lead y compra)

```text
Google / Pinterest ("cómo calcular la medida de un cuadro para el living")
→ Artículo de Blog (articulo.html: "Guía definitiva: ¿Qué tamaño de cuadro poner sobre el sofá?")
→ [Lee el artículo, revisa las proporciones recomendadas y las fotos de inspiración]
→ [Encuentra la sección "Obras destacadas para este formato" y hace clic en "Bruma y Terracota"]
→ Ficha de Producto (producto.html)
◇ ¿Decide comprar inmediatamente?
   ├── Sí → [Agrega al carrito] → Carrito de compras listo para pagar
   └── No → [Regresa al artículo o footer y completa el formulario: "Descarga la Guía de Interiorismo + 10% de descuento"]
          → Mensaje de confirmación: Lead captado exitosamente
```

---

## 3. Categorías de productos y filtros de la tienda

### Categorías principales

| Categoría | Obras incluidas en catálogo | Características y enfoque |
|---|---|---|
| **Cuadros Texturados & Relieve** | *Duna Serena (100x120cm)*, *Relieve Volcánico Arena (80x100cm)*, *Líneas Japandi en Yeso (90x90cm)*, *Blanco Escultórico (120x150cm)* | Obras trabajadas con espátula, arenas orgánicas y pasta texturizadora. Destacan por su tridimensionalidad y juego de sombras. |
| **Óleos y Acrílicos Botánicos** | *Follaje Calmo (80x120cm)*, *Eucalipto en Óleo Suave (70x100cm)*, *Hojas de Salvia y Arcilla (100x100cm)* | Pinturas con pigmentos puros inspiradas en la flora nativa y formas botánicas abstractas en tonos verdes oliva y tierra. |
| **Abstractos & Minimalistas** | *Bruma y Terracota (100x120cm)*, *Horizontes Neutros (80x120cm)*, *Pigmento y Pan de Oro (100x140cm)* | Composiciones contemporáneas de formas puras y paletas serenas para salas modernas y comedores. |
| **Dípticos y Grandes Formatos** | *Díptico Viento y Calma (2 piezas de 70x100cm)*, *Tríptico Tierra Madre (3 piezas de 50x80cm)* | Conjuntos pensados para muros amplios de doble altura o respaldo de camas king. |

### Filtros adicionales de la tienda
- **Orientación:** Vertical, Horizontal, Cuadrado, Conjunto (Díptico/Tríptico).
- **Paleta de color dominante:** Neutros/Beige, Terracota/Cálido, Verde Salvia/Oliva, Monocromático Negro/Blanco.
- **Rango de precio y disponibilidad:** Obras en stock para envío inmediato o disponibles para réplica por encargo.

---

## 4. Categorías del blog y estrategia de contenidos

| Categoría del Blog | Idea de artículo concreta | Necesidad o motivación de Sofía | Producto / Obra relacionada |
|---|---|---|---|
| **Guías de Decoración & Escala** | *"Guía definitiva: ¿Qué tamaño de cuadro poner sobre el sofá para no achicar tu living?"* | Sofía necesita resolver la inseguridad de medidas y proporciones exactas en su espacio. | *Bruma y Terracota (100x120 cm)* y *Díptico Viento y Calma* |
| **Texturas, Técnicas y Materiales** | *"La magia del relieve: por qué un cuadro texturado cambia por completo con la luz del día"* | Busca autenticidad y piezas con alma táctil, diferenciándolas de impresiones planas. | *Duna Serena — Textura Orgánica* |
| **Procesos del Taller y Cuidados** | *"Cómo limpiar y cuidar un cuadro al óleo o con textura sin dañar la pintura ni el bastidor"* | Quiere proteger su inversión artística y asegurar la máxima durabilidad de las obras. | *Líneas Japandi en Yeso* y kit de montaje con anclajes |
