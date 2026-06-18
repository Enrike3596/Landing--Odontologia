# Clínica Dental - Landing Page

Landing page profesional para una clínica odontológica, diseñada para presentar los servicios, el equipo médico y facilitar el contacto con pacientes potenciales.

## 🌐 Sitio en vivo

El portafolio se encuentra publicado en **Azure Static Web Apps**:

👉 [https://lemon-pond-0de0b710f.7.azurestaticapps.net](https://lemon-pond-0de0b710f.7.azurestaticapps.net)
## Problemática

Las clínicas dentales necesitan una presencia digital que transmita confianza y profesionalismo. Una landing page bien diseñada permite:
- Presentar servicios y especialidades de forma clara
- Mostrar credenciales del equipo médico
- Facilitar la reserva de citas mediante formulario de contacto
- Proveer información de contacto y ubicación
- Mejorar la visibilidad y captación de pacientes

## Solución Tecnológica

Aplicación web SPA (Single Page Application) construida con Vue 3, migrada desde un HTML estático con Bootstrap a una arquitectura moderna basada en componentes. La página incluye navegación suave por secciones, slider interactivo, animaciones al scroll y diseño responsivo.

## Tecnologías Utilizadas

- **Vue 3** — Framework progresivo con Composition API (`<script setup>`)
- **Vite** — Bundler y servidor de desarrollo rápido
- **Vue Router** — Enrutamiento SPA
- **Pinia** — Manejo de estado
- **Bootstrap 5** — Sistema de grillas y utilidades CSS
- **Tiny Slider** — Slider de hero interactivo
- **WOW.js + Animate.css** — Animaciones al hacer scroll
- **LineIcons** — Iconos vectoriales

## Instalación

```sh
npm install
```

## Desarrollo

```sh
npm run dev
```

Servidor en `http://localhost:5173`

## Producción

```sh
npm run build
```

El output se genera en la carpeta `dist/`.

## Linter

```sh
npm run lint
```
