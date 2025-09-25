# SEPAL International — Documentación de la página

Landing estática desarrollada con HTML, CSS y JavaScript para presentar la información institucional de SEPAL International.

## Contenido de la página
La página está organizada en secciones ancladas dentro de una sola vista:
- Inicio (Hero): titular, descripción breve y botón de contacto.
- Quiénes Somos: texto introductorio y lista de líneas de trabajo.
- Misión: objetivos y enfoque de impacto.
- Visión: aspiración y principios rectores.
- Contacto: formulario básico (nombre, correo, mensaje) sin envío a servidor.

Cada elemento del menú navega a la sección correspondiente mediante anclas (#id). El encabezado es fijo (sticky) para mantener la navegación visible en todo momento.

## Características clave
- Responsive: diseño adaptable desde móviles hasta escritorio.
- Accesibilidad: enlace “Saltar al contenido”, estados de foco visibles y etiquetas de formulario.
- Navegación móvil: botón hamburguesa que abre/cierra el menú.
- Microinteracciones: efecto “ripple” en botones y transiciones sutiles.
- Modo oscuro: activación automática con `prefers-color-scheme: dark`.
- Desplazamiento suave y ajuste de anclajes con `scroll-margin-top` para compensar el header fijo.

## Estructura del proyecto
- index.html: estructura, contenido y secciones.
- styles.css: estilos base, variables, responsive, accesibilidad y modo oscuro.
- script.js: lógica de navegación móvil y efecto ripple en botones.

## Cómo ejecutar / visualizar
No requiere compilación ni dependencias.
- Opción rápida: abrir el archivo index.html con doble clic.
- Servidor local (recomendado):
  - Extensión Live Server (VS Code), o
  - Ejecutar `npx serve` en la carpeta del proyecto y abrir la URL indicada.

## Cómo publicarla (deploy) gratis
- GitHub Pages (recomendado):
  1) Crea un repo y sube estos 3 archivos: index.html, styles.css, script.js (y README.md).
  2) En Settings > Pages, elige “Deploy from a branch” y la rama “main” en la carpeta root.
  3) Espera 1–2 minutos: tendrás una URL pública del tipo https://usuario.github.io/nombre-repo.
- Alternativas: Netlify o Vercel (arrastra la carpeta o conecta el repo; framework: “Vanilla”).
- Hosting propio: sube los archivos al public_html de tu servidor.

## Personalización
- Marca (logo y colores): se controlan con variables CSS (paleta en :root). Puede reemplazar el logo referenciado desde https://cepalinternational.com/public/img/logo.png por un archivo local si lo desea.
- Secciones: edite los textos y listas en index.html según las necesidades de la organización.
- Interacciones: puede desactivar el efecto ripple si el usuario prefiere menos movimiento (se respeta `prefers-reduced-motion`).

## Limitaciones
- El formulario de contacto no envía datos por sí mismo. Si necesita recepción de mensajes:
  - Conéctelo a un servicio (Formspree, Netlify Forms, etc.), o
  - Implemente un endpoint propio y cambie el atributo action del formulario.

## Licencia
© SEPAL International. Todos los derechos reservados.
