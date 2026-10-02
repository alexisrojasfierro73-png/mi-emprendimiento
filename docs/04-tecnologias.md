# Tecnologías del proyecto — Lienzo Vivo

## Stack y herramientas

| Área | Herramienta | Para qué la uso en este proyecto |
|---|---|---|
| **Construcción** | HTML5 semántico + CSS3 puro | Maquetación limpia, accesible y modular de todas las páginas del sitio sin depender de frameworks externos ni gestores de contenido pesados. |
| **Versionado** | Git y GitHub | Control de versiones paso a paso mediante commits atómicos y almacenamiento centralizado del proyecto en la nube. |
| **Publicación** | GitHub Pages | Despliegue continuo y hosting estático gratuito con URL pública accesible para revisión y evaluación. |
| **Diseño y Wireframing** | Whimsical | Creación del moodboard de inspiración, calco de componentes UI y prototipado de wireframes en baja fidelidad. |
| **Generación y Prototipo** | Google Stitch | Generación del prototipo de alta fidelidad basado en el archivo `DESIGN.md` y prompts pantalla por pantalla. |
| **Asistente de Código e IA** | Antigravity IDE | Generación y asistencia de especificaciones, maquetación CSS/HTML, revisión de contraste y buenas prácticas. |

## Qué es funcional y qué es prototipo visual

| Funcionalidad | Estado en esta versión | Descripción |
|---|---|---|
| **Navegación general** (Landing, Tienda, Ficha, Blog, Artículo, Carrito, Páginas legales) | **Funcional** | Los enlaces entre páginas, menús de navegación, botones y rutas internas funcionan de verdad en el navegador. |
| **Detalle de obra y selector de marco** | **Funcional** | Permite cambiar visualmente entre tipos de enmarcado y consultar la ficha técnica con medidas reales. |
| **Contacto y asesoría por WhatsApp** | **Funcional** | Enlace directo mediante `https://wa.me/569XXXXXXXX` con mensaje predeterminado de consulta sobre el cuadro. |
| **Compartir artículo en redes** | **Funcional** | Enlaces interactivos con intents de WhatsApp, Pinterest y Twitter/X. |
| **Formulario de captación de leads** (Guía + 10% dcto) | **Prototipo visual** | La interfaz del formulario y sus estados de validación se renderizan fielmente, pero no envían datos a un servidor backend. |
| **Buscador y filtros de la tienda** (por técnica y paleta) | **Prototipo visual** | Los controles de filtro y barra de búsqueda se muestran con sus estados interactivos (chips activos, checkboxes), listos para conectar en JavaScript/backend posterior. |
| **Carrito y cotizador de despacho** | **Prototipo visual** | La pantalla de carrito calcula y muestra el resumen visual de productos y tarifas por comuna sin procesar pagos reales. |
| **Comentarios del blog** | **Prototipo visual** | Formulario con campos de nombre y comentario estilizado según el design system, sin persistencia en base de datos. |

## Integraciones para una versión real (Producción)

1. **Pasarela de pago online:** Integración con **Webpay Plus (Transbank)** y **Mercado Pago** para compras con tarjetas de débito/crédito en cuotas sin interés.
2. **Cálculo automatizado de fletes y logística de arte:** Integración con API de couriers especializados (ej. **Starken, Chilexpress o Shipit**) con recargo automático para embalaje de alta seguridad en madera y seguro de transporte de obras.
3. **Email marketing y automatización de leads:** Conexión con **Mailchimp** o **Klaviyo** para almacenar los correos captados, enviar automáticamente el PDF de la guía de interiorismo y disparar secuencias de bienvenida con el cupón de descuento.
4. **Almacenamiento de obras y catálogo dinámico:** CMS desacoplado (Headless CMS como Strapi o Sanity) para que la artista pueda subir nuevas obras vendidas/disponibles y actualizar fotos de texturas sin tocar código.

## Restricciones

- **Plazo de entrega y desarrollo:** Fases evaluativas comprendidas entre el 29 de septiembre y el 14 de octubre de 2026.
- **Identidad visual de marca:** No existía manual corporativo previo; la identidad cromática, tipografías y reglas de diseño se definen integralmente en la Fase 2 en `DESIGN.md`.
- **Estrategia Mobile-First:** El diseño responsive prioriza dispositivos móviles (smartphones de 375px a 430px de ancho) debido a que la proto-persona (Sofía) navega mayoritariamente desde su teléfono en horarios nocturnos y traslados.
