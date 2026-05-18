# ActividadRA2
hola :3
# Dashboard de Inventario Administrativo

## Descripción del Proyecto:
Este proyecto es un dashboard administrativo diseñado para un sistema de gestión de inventarios. Presenta una interfaz moderna, intuitiva y completamente responsiva, permitiendo al usuario visualizar el estado del stock, estadísticas clave y listados de productos de manera eficiente en cualquier dispositivo.

## Tecnologías Utilizadas:
* **HTML5:** Estructura semántica avanzada y accesible.
* **CSS3:** Implementación de diseño moderno sin el uso de frameworks externos.
  * **CSS Grid:** Utilizado para definir la macro-estructura global del dashboard (`sidebar`, `header`, `main`, `footer`).
  * **Flexbox:** Utilizado para la alineación interna de componentes independientes, como menús, tarjetas de métricas y la distribución de elementos en el encabezado.
  * **Variables CSS (Custom Properties):** Centralización de la paleta de colores y fuentes para mantener la consistencia y facilitar un futuro escalado (como un modo oscuro).

## Decisiones de Diseño, Accesibilidad y Responsividad

### 1. Accesibilidad (a11y):
* Se incorporaron roles ARIA (`role="navigation"`, `role="banner"`, `role="main"`, `role="contentinfo"`) para garantizar una navegación semántica fluida en lectores de pantalla.
* Las imágenes de la interfaz cuentan con atributos `alt` descriptivos.
* Los elementos interactivos clave (como las tarjetas de resumen) incluyen `tabindex="0"` y estilos enfocados (`:focus`) para permitir una navegación completa mediante el teclado.

### 2. Contraste y Estética
* Se seleccionó una paleta basada en tonos pizarra (`#1e293b`) y un azul de énfasis (`#2563eb`) que cumple con los estándares de alto contraste, mejorando la legibilidad general y ofreciendo un aspecto limpio y profesional.

### 3. Optimizaciones de Responsividad (Media Queries Avanzadas)
El diseño se adaptó minuciosamente para ofrecer una experiencia fluida en tres entornos: escritorio, tablets y smartphones.

* **Estructura Dinámica en Tablets (Breakpoint 768px):** Para dispositivos como el *iPad Mini* o *Surface Duo*, el diseño Grid se reorganiza a una sola columna. Se implementó `grid-template-rows: auto auto 1fr auto;` para calcular dinámicamente la altura de las secciones, eliminando fallos de solapamiento de texto. Además, se aplicó `flex-wrap: wrap;` en el menú para evitar desbordamientos horizontales.
* **Ajustes Críticos para Teléfonos (Breakpoint 480px):** En pantallas muy estrechas (como *iPhone 14 Pro Max* o *Samsung Galaxy A51*), se optimizó el espacio ocultando elementos secundarios de texto (como el nombre del administrador), dejando únicamente el avatar. El buscador se expande al 100% para facilitar su uso táctil y los márgenes generales se redujeron para maximizar el área de datos.
* **Control de Desbordamiento en Tablas:** Para evitar que etiquetas de estado con texto compuesto (ej. *"Bajo Stock"*) se apilaran verticalmente una palabra sobre otra desfigurando el diseño, se aplicó la propiedad `white-space: nowrap;` combinada con un contenedor con desbordamiento controlado (`overflow-x: auto`). Esto garantiza que los textos se mantengan siempre horizontales, legibles y accesibles mediante un deslizamiento lateral suave en pantallas táctiles.
