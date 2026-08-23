# PFO1 — Landing Page de Portafolio Personal

**Estudiante:** Christian Albornoz  
**Carrera:** Desarrollo de Software — IFTS 29  
**Materia:** Desarrollo Web Front End  
**Despliegue en producción:** [https://christianalbornoz-portfolio.vercel.app](https://christianalbornoz-portfolio.vercel.app)  
**Perfil de GitHub:** [https://github.com/albor77](https://github.com/albor77)

---

##  Descripción del Proyecto

Este proyecto corresponde a la primera Práctica Formativa Obligatoria (PFO1). Consiste en una landing page estática de portafolio profesional desarrollada con **HTML5 y CSS3 puro**, sin librerías externas ni JavaScript. Su propósito es presentar mi perfil técnico, áreas de enfoque (Desarrollo de Software, QA & Testing y UX/UI), habilidades clave, proyectos destacados y vías de contacto.

---

##  Tecnologías y Herramientas

- **HTML5 Semántico:** Estructuración mediante etiquetas semánticas (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`).
- **CSS3 Avanzado:** Uso exhaustivo de Custom Properties (Variables CSS), pseudoclases dinámicas y efectos de iluminación neón.
- **Maquetación Híbrida:**
  - **Flexbox:** Implementado para la barra de navegación, el alineamiento bidireccional del Hero, la disposición interna de las tarjetas y el pie de página.
  - **CSS Grid:** Utilizado en las grillas de _Habilidades_ y _Proyectos Destacados_ con la función fluida `repeat(auto-fit, minmax(...))` para garantizar adaptabilidad automática sin depender exclusivamente de media queries.
- **Tipografía:** Integración de Google Fonts (_Plus Jakarta Sans_ en variantes 400, 600, 700 y 800).
- **Control de Versiones & Despliegue:** Git, repositorio en GitHub y despliegue continuo en Vercel.

---

##  Decisiones de Diseño y Arquitectura Técnica

### 1. Identidad Visual y Accesibilidad (Dark & Neon Theme)

Se optó por una estética oscura minimalista (`#14161d` y `#171923`) con acentos verde neón (`#22c55e`), buscando transmitir una impronta tecnológica y moderna. Para asegurar el cumplimiento de accesibilidad (WCAG AA):

- Se preservaron ratios de contraste superiores a 4.5:1 entre el texto y los fondos.
- Se agregaron atributos `aria-label` en todos los enlaces con íconos vectoriales SVG sin texto visible.
- Los elementos del formulario cuentan con `<label>` vinculados explícitamente mediante `for` e `id`.

### 2. Feedback de Formulario sin JavaScript (Técnica `:target`)

Para evitar el error HTTP 405 común en entornos estáticos al enviar formularios sin backend, se configuró el formulario con método `GET` apuntando al ancla `#mensaje-enviado`. La ventana modal de confirmación se activa puramente con CSS mediante la pseudoclase `:target` y efectos de transición de opacidad y visibilidad.

### 3. Responsive Design

Se establecieron breakpoints en `992px`, `768px` y `480px`, asegurando que:

- En dispositivos móviles, la imagen de perfil se reposicione por encima del texto de presentación mediante `order: -1`.
- Los campos de texto mantengan un tamaño de fuente de `1rem` para evitar el zoom automático no deseado en navegadores iOS Safari.
- Los elementos interactivos tengan áreas de toque cómodas para pantallas táctiles.

---

##  Proyectos Destacados Enlazados

1. **SePrice — Turnos:** Sistema de gestión de consultorios externos y asignación de turnos médicos desarrollado en TypeScript. ([Repositorio](https://github.com/albor77/seprice-turnos))
2. **Club Deportivo:** Aplicación móvil nativa en Kotlin para administración de socios y cuotas, con versión complementaria en C# / .NET. ([Repositorio](https://github.com/albor77/club-deportivo-mobile))

---

##  Declaración de Uso de Inteligencia Artificial

En cumplimiento con los requerimientos éticos y pedagógicos de la PFO1, se documenta el uso de herramientas de IA generativa durante el desarrollo del proyecto:

- **Herramienta utilizada:** Google Gemini (Gemini 2.5 / Web).
- **Plan utilizado:** Plan Gratuito.
- **Experiencia previa:** Familiaridad media en consultas de depuración de código, sintaxis y asistencia en estructuración de software.
- **Para qué se utilizó:**
  - Consulta técnica para implementar el modal de confirmación 100% en CSS puro mediante `:target` sin requerir JavaScript.
  - Auditoría de accesibilidad semántica (etiquetado ARIA en SVGs y estructura de formularios).
  - Validación y ajuste fino de los rangos de media queries responsivos.
- **Criterio propio, adaptaciones y cambios realizados:**
  - Se revisó y adaptó todo el código sugerido para que coincidiera de forma estricta con la estructura de clases del proyecto (`.card`, `.modal-box`, `.hero-image-wrapper`).
  - Se ajustaron manualmente los valores de encuadre, dimensiones y posición focal (`object-position`) de la imagen de perfil dentro del contenedor con arco neón.
  - Se personalizaron los enlaces directos a los repositorios de GitHub (`albor77`), descartando ejemplos genéricos e integrando descripciones reales de proyectos personales.
