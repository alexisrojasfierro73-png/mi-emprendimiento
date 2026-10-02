# Spec de diseño — Lienzo Vivo

**Tablero de Wireframes en Whimsical:** https://whimsical.com/lienzo-vivo-wireframes-and-screens-board

![Wireframes de Lienzo Vivo](img/wireframes.png)

---

## Prompts por pantalla para Google Stitch

### 1. Pantalla: Landing Page (Inicio — Versión Desktop)
```text
Pantalla: Landing Page (Inicio) de Lienzo Vivo, versión desktop. Usa el design system del proyecto (DESIGN.md).
Objetivo: Que Sofía entienda en segundos que son cuadros de arte originales hechos a mano con relieve y se sienta inspirada para explorar la galería o solicitar un cuadro a medida.
Componentes, de arriba hacia abajo:
1. Navbar con logo "Lienzo Vivo", enlaces (Inicio [activo], Tienda, Cuadros a Medida, Blog, Taller), buscador y botón de carrito con badge (0).
2. Hero Section: fondo color neutral (#FAF7F2), a la izquierda titular h1 en Fraunces "Obras de arte hechas a mano que dan vida y textura a tus muros", bajada en Inter "Cuadros originales al óleo y pasta texturada de autor. Creados para transformar tus espacios con calidez, relieve y exclusividad.", botón button-primary "Explorar Galería de Obras" y button-secondary "Encargar Cuadro a Medida". A la derecha, fotografía en gran formato de cuadro texturado "Duna Serena" montado sobre sofá de lino beige con marco de roble natural.
3. Barra de Valor Artesanal: fila de 4 módulos con ícono lineal y texto: "100% Pintado a Mano", "Textura Real en Relieve", "Madera Nativa y Lino", "Despacho Seguro a todo Chile".
4. Sección Obras Destacadas: h2 "Colección en Stock para Entrega Inmediata", bajada "Piezas únicas listas para montar en tu hogar". Grilla de 3 columnas con card-product:
   - Obra 1: Imagen de "Duna Serena", badge-technique "Textura en Relieve", nombre "Duna Serena", medida "100 x 120 cm", precio "$189.000 CLP", botón button-secondary "Ver Obra & Medidas".
   - Obra 2: Imagen de "Follaje Calmo", badge-technique "Óleo Botánico", nombre "Follaje Calmo", medida "80 x 120 cm", precio "$165.000 CLP", botón button-secondary "Ver Obra & Medidas".
   - Obra 3: Imagen de "Bruma & Terracota", badge-technique "Abstracto Cálido", nombre "Bruma & Terracota", medida "90 x 90 cm", precio "$145.000 CLP", botón button-secondary "Ver Obra & Medidas".
5. Sección El Taller y Proceso: bloque dividido con foto de la artista aplicando pasta con espátula sobre lienzo en bastidor, texto sobre el proceso de secado natural de 3 semanas y sello de autenticidad firmado.
6. Módulo de Captación de Leads (lead-form): caja destacada con fondo surface (#F0EAE1) y borde suave, h3 "Descarga gratis la Guía de Interiorismo: Cómo elegir el tamaño y paleta ideal para tus cuadros" + campo de correo electrónico + button-primary "Recibir Guía + 10% Dcto" + texto legal "No enviamos spam. Respetamos tu privacidad."
7. Footer completo: enlaces a Tienda, Blog, Cuadros a Medida, Contacto, Preguntas Frecuentes, Términos y Condiciones, Política de Privacidad y redes (@lienzovivo.arte).
```

---

### 2. Pantalla: Tienda / Galería de Catálogo (Versión Desktop)
```text
Pantalla: Tienda y Catálogo de Obras de Lienzo Vivo, versión desktop. Usa el design system del proyecto (DESIGN.md).
Objetivo: Que Sofía pueda filtrar y encontrar cuadros según la técnica artesanal, orientación y gama de colores que combinen con su pared.
Componentes, de arriba hacia abajo:
1. Navbar global de Lienzo Vivo.
2. Cabecera de Tienda: h1 en Fraunces "Galería de Obras Originales", buscador integrado con placeholder "Buscar por nombre, técnica o color (ej. texturado, salvia, díptico)...".
3. Barra superior de categoría con filter-chip horizontales: "Todos los Cuadros" (activo con filter-chip-active), "Texturados & Relieve", "Óleos Botánicos", "Abstractos Contemporáneos", "Dípticos & Grandes Formatos".
4. Layout de 2 columnas:
   - Columna izquierda (Sidebar de filtros, ancho 260px): Filtro por Orientación (checkboxes: Vertical, Horizontal, Cuadrado, Díptico), Filtro por Paleta de Color (swatches circulares: Neutro/Arena, Terracota, Verde Salvia, Monocromático), Rango de Precio (slider $80.000 a $350.000 CLP), Disponibilidad ("En Stock inmediato" / "A pedido").
   - Columna derecha (Grilla de Obras, 3 columnas): 6 card-product completas con fotos de cuadros en alta resolución, badges distintivos, medidas en cm, precios en CLP y botón "Ver Obra & Medidas".
5. Banner interactivo al pie del catálogo: "¿Necesitas una medida especial para tu pared? Creamos tu cuadro a pedido con la paleta de tu espacio" + botón button-primary "Cotizar Cuadro a Medida".
6. Footer global.
```

---

### 3. Pantalla: Ficha de Producto / Detalle de Obra (Versión Desktop)
```text
Pantalla: Ficha de Detalle de Producto "Duna Serena — Textura Orgánica" de Lienzo Vivo, versión desktop. Usa el design system del proyecto (DESIGN.md).
Objetivo: Que Sofía aprecie los detalles del relieve, entienda la escala en el muro, seleccione el tipo de enmarcado y agregue la obra al carrito con total seguridad.
Componentes, de arriba hacia abajo:
1. Navbar global con migas de pan (Breadcrumbs: Inicio > Tienda > Texturados > Duna Serena).
2. Layout principal de 2 columnas:
   - Columna izquierda (Galería visual): Imagen principal en alta resolución con zoom interactivo de textura, carrusel inferior de 4 miniaturas (1. Foto frontal iluminada, 2. Primer plano de espátula y relieve, 3. Montaje a escala sobre sofá de 3 cuerpos en living, 4. Detalle de marco flotante de roble).
   - Columna derecha (Información y configuración):
     - Badge badge-technique "Textura en Relieve sobre Lino".
     - h1 "Duna Serena — Textura Orgánica".
     - Precio en Fraunces "$189.000 CLP" (incluye IVA).
     - Medidas fijas de bastidor: "100 cm de ancho x 120 cm de alto x 4 cm de profundidad".
     - Selector de Enmarcado (frame-selector): 3 opciones con selector visual tipo radio:
       a) "Solo Bastidor de Madera Listo para Colgar" (+$0)
       b) "Marco Flotante de Madera Roble Natural" (+$38.000 CLP - Recomendado)
       c) "Marco Flotante Negro Mate" (+$38.000 CLP)
     - Botón button-primary "Agregar al Carrito de Compras".
     - Botón button-secondary con ícono de WhatsApp "Consultar dudas sobre esta obra con la artista".
     - Bloque informativo desplegable (Acordeón):
       - "Técnica y Materiales": Pasta de modelar con arena volcánica, acrílico mate y barniz protector UV sobre lino crudo.
       - "Embalaje y Despacho Seguro": Caja de madera reforzada y esquineros acolchados con seguro de transporte.
       - "Certificado de Autenticidad": Obra única firmada a mano por la artista con número de serie.
3. Módulo "Obras que combinan en este espacio": 3 card-product sugeridas para crear dípticos o galerías de pared.
4. Footer global.
```

---

### 4. Pantalla: Carrito de Compras y Cotizador de Despacho (Versión Desktop)
```text
Pantalla: Carrito de Compras de Lienzo Vivo, versión desktop. Usa el design system del proyecto (DESIGN.md).
Objetivo: Que Sofía revise las obras seleccionadas, calcule el despacho exacto por comuna y proceda al pago sin sorpresas de costos ocultos.
Componentes, de arriba hacia abajo:
1. Navbar global.
2. Cabecera con h1 "Tu Carrito de Obras de Arte" e indicador de compra segura (ícono de candado y garantía de embalaje).
3. Layout de 2 columnas:
   - Columna izquierda (Lista de productos, ancho 65%):
     - Tarjeta de obra seleccionada con miniatura, título "Duna Serena — Textura Orgánica", detalle "Marco Flotante Roble Natural (100x120 cm)", selector de cantidad (1), precio unitario "$227.000 CLP" y botón para eliminar.
     - Nota de embalaje: "Tu obra incluye esquineros de protección y embalaje especial en caja de madera rígida sin costo adicional."
   - Columna derecha (cart-summary, ancho 35%):
     - Caja destacada con fondo surface (#F0EAE1) y borde suave.
     - Desglose de costos: Subtotal ($227.000 CLP).
     - Calculador de despacho: Selector desplegable de Región y Comuna (ej. "Región Metropolitana - Providencia") -> Calcula "$8.900 CLP (Entrega protegida en 2 a 4 días hábiles)".
     - Campo para cupón de descuento con botón "Aplicar" (ej. "GUIA10").
     - Total final destacado en Fraunces bold ($235.900 CLP).
     - Botón button-primary "Continuar al Pago Seguro con Webpay / Débito / Crédito".
     - Sellos de confianza: "Garantía de Llegada Intacta", "Obras 100% Originales", "Pago Seguro SSL".
4. Footer global.
```

---

### 5. Pantalla: Blog y Taller de Inspiración (Versión Desktop)
```text
Pantalla: Blog "El Taller & Inspiración" de Lienzo Vivo, versión desktop. Usa el design system del proyecto (DESIGN.md).
Objetivo: Que Sofía descubra artículos sobre proporción de cuadros en paredes, tendencias decorativas y técnicas manuales.
Componentes, de arriba hacia abajo:
1. Navbar global.
2. Cabecera del Blog: h1 en Fraunces "Inspiración, Guías de Decoración & Taller", bajada "Aprende a combinar texturas, elegir las medidas perfectas y cuidar tus obras de arte".
3. Barra de filtros de categoría: filter-chip "Todos los Artículos" (activo), "Guías de Decoración & Escala", "Texturas & Técnicas", "Procesos del Taller".
4. Artículo Destacado Principal: tarjeta horizontal de gran formato con imagen de living moderno, badge "Guías de Decoración", título h2 "Guía definitiva: ¿Qué tamaño de cuadro poner sobre el sofá para no achicar tu living?", resumen y enlace button-secondary "Leer Guía Completa (4 min de lectura)".
5. Grilla de 3 columnas con article-card:
   - Card 1: "La magia del relieve: por qué un cuadro texturado cambia con la luz del día", categoría "Texturas & Técnicas".
   - Card 2: "Cómo limpiar y conservar un cuadro al óleo con textura sin dañar la pintura", categoría "Procesos del Taller".
   - Card 3: "5 paletas de color japandi para crear un living sereno y elegante", categoría "Guías de Decoración".
6. Bloque lead-form para suscripción a la guía descargable.
7. Footer global.
```

---

### 6. Pantalla: Artículo Individual de Blog (Versión Desktop)
```text
Pantalla: Artículo de Blog "Guía definitiva: ¿Qué tamaño de cuadro poner sobre el sofá?" de Lienzo Vivo, versión desktop. Usa el design system del proyecto (DESIGN.md).
Objetivo: Brindar contenido de alto valor técnico sobre interiorismo a Sofía y conectarla de forma natural con los cuadros recomendados de la tienda.
Componentes, de arriba hacia abajo:
1. Navbar global con migas de pan (Inicio > Blog > Guías de Decoración > Tamaño de cuadro sobre sofá).
2. Cabecera de artículo: badge-technique "Guías de Decoración & Escala", h1 en Fraunces "Guía definitiva: ¿Qué tamaño de cuadro poner sobre el sofá para no achicar tu living?", datos de autoría "Por Taller Lienzo Vivo · 4 min de lectura · Actualizado en Octubre 2026".
3. Imagen principal del artículo en formato 16:9 con pie de foto sobre proporciones de sala.
4. Cuerpo del artículo (ancho legible 760px centrado):
   - Párrafos estructurados con subtítulos h2 y h3.
   - Regla de los 2/3 (el cuadro debe ocupar entre el 60% y 75% del ancho del sofá).
   - Diagrama explicativo de alturas de montaje (colgar el centro del cuadro a 150 cm del suelo).
   - Botones para compartir el artículo en redes sociales (WhatsApp, Pinterest, Instagram).
5. Módulo comercial "Obras recomendadas para este formato de living": Grilla de 2 card-product ("Duna Serena 100x120 cm" y "Bruma & Terracota 90x90 cm").
6. Sección de Comentarios: Lista de 2 comentarios de usuarias con respuestas del taller + formulario para dejar una nueva consulta.
7. Footer global.
```

---

### 7. Prompt para la versión Mobile (Todas las pantallas)
```text
Pantalla: Versión Mobile (375px a 430px) de [Nombre de Pantalla] de Lienzo Vivo. Usa el design system del proyecto (DESIGN.md) respetando la sección ## Layout.
Reglas de adaptación mobile:
1. Navbar colapsada: Logo centrado o a la izquierda, ícono de menú hamburguesa a la izquierda y botón de carrito de compras con contador badge a la derecha.
2. Disposición a 1 sola columna vertical en todo el contenido (imágenes de obra arriba del texto y precio).
3. Barra de filtros de tienda con scroll horizontal táctil mediante filter-chip deslizable.
4. Botones de acción principales (button-primary "Agregar al Carrito" o "Ver Obra") con ancho del 100% y área táctil mínima de 48px de altura para facilitar el toque con el pulgar.
5. Ficha de producto con carrusel swipeable de fotos y selector de marco en lista vertical clara.
6. Carrito con resumen sticky o posicionado debajo de la lista de productos sin provocar scroll horizontal.
7. Tipografía de títulos h1 ajustada a 34px y espaciados laterales de contenedor fijados en 16px.
```
