# Portafolio - Rodrigo Sebastián Laura Moreno

Una landing page y portafolio personal moderno y elegante, enfocado en mostrar mi filosofía de trabajo, experiencia laboral y los proyectos más destacados en los que he participado como Desarrollador FullStack.

## 🚀 Tecnologías que utilicé

- **[Astro](https://astro.build/)**: Framework web enfocado en la velocidad y optimización en la entrega de contenido estático.
- **[Tailwind CSS](https://tailwindcss.com/)**: Framework de utilidades para un desarrollo visual rápido, estructurado y completamente responsivo.
- **TypeScript & JavaScript**: Para el tipado riguroso de interfaces y la lógica ligera manejada en el cliente (menús dinámicos, eventos).
- **Vite**: Para la construcción ultra-rápida nativa de Astro.

## 🎯 Propósito del Proyecto

El objetivo de este proyecto es servir como mi propia carta de presentación digital en internet (Landing Page/CV Interactivo). Está diseñado intencionalmente para:
1. **Reflejar mi estilo y sobriedad técnica**: Con un esquema oscuro de acentos granate y estética minimalista.
2. **Presentar claramente mi trayectoria**: Exponiendo mi filosofía de código ("simples, organizadas y flexibles"), mi paso por diversas empresas y proyectos con impacto.
3. **Facilitar el reclutamiento**: Proveer puntos de contacto ágiles, desde la rápida descarga de mi Currículum Vítae, hasta la comunicación instantánea vía WhatsApp integrada en un moderno formulario de contacto.

## 🏛️ Arquitectura del Sistema

El portafolio hace uso de una arquitectura fuertemente orientada a dar orden, ligereza y escalabilidad empleando el patrón clásico y natural de **Astro**.

- **Enfoque basado en Componentes Reutilizables:**
  - `src/components/`: Piezas particulares de UI correspondientes a cada sección del portafolio (p.ej. `Hero.astro`, `Experience.astro`, `Projects.astro`).
  - `src/shared/components/`: Componentes abstractos reutilizables en todo el sitio, como un contenedor general `Section.astro` que aplica estandarizaciones de espaciado dinámico.
- **Layouts Centrales (`src/layouts/`):** La plantilla maestra `BaseLayout.astro` encapsula directivas estándar del estándar HTML, importaciones estáticas globales, y monta el `Header` y `Footer` persistentemente.
- **Flujo de datos Top-Down:** Toda la "base de datos" (formación académica, tecnologías, y URLs a redes) reside concentrada en la página que la renderiza (`src/pages/index.astro`). Esto se inyecta directamente como **Props fuertemente tipadas** hacia los subcomponentes. Gracias a esta delegación orientada a interfaces estrictas, el código está listo por si en un futuro quiero migrar a un headless CMS moderno.
- **Patrón Mobile-First:** Utilización de las utilidades lógicas escalonadas de Tailwind (`sm:`, `md:`, `lg:`) para construir todo partiendo por el acomodo perfecto en teléfonos y garantizando fluidez hacia monitores grandes.
- **Hidratación Cero (Zero JS by Default):** Al ser construido con Astro, carece de bibliotecas reactivas pesadas de lado del cliente (React/Vue/Svelte se obviaron voluntariamente para esta landing pura), inyectando JavaScript imperativo únicamente donde es estrictamente necesario (ej. menú móvil y API de WhatsApp).
