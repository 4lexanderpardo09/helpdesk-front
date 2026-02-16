# DeskFlow Frontend

Bienvenido al frontend de **DeskFlow**, el sistema moderno de Mesa de Ayuda.
Este proyecto fue inicializado con [Vite](https://vitejs.dev/) y [React](https://react.dev/), utilizando TypeScript para robustez y seguridad de tipos.

## 🚀 Inicio Rápido

1.  **Instalar dependencias:**
    ```bash
    pnpm install
    ```

2.  **Modo Desarrollo:**
    ```bash
    pnpm dev
    ```
    La aplicación correrá en `http://localhost:5173`.

3.  **Producción:**
    ```bash
    pnpm build
    pnpm preview
    ```

## 🛠️ Stack Tecnológico

*   **Core:** React 19, TypeScript
*   **Estilos:** Tailwind CSS v3.4 (con tema personalizado en `tailwind.config.js`)
*   **Iconos:** Material Symbols Outlined, Tabler Icons.
*   **Navegación:** React Router DOM v7.
*   **HTTP:** Axios (con interceptores para JWT).
*   **Fuentes:** Manrope (Google Fonts).

## 📂 Estructura del Proyecto

*   `src/components/ui/`: Componentes base reutilizables (Button, Input).
*   `src/layout/`: Estructuras de página (LoginLayout).
*   `src/pages/`: Vistas principales (LoginPage, Dashboard).
*   `src/lib/`: Utilidades y servicios (API, Auth, Utils).
    *   `api.ts`: Cliente Axios centralizado.
    *   `auth.ts`: Servicio de autenticación.

## 🔑 Autenticación

El sistema utiliza **JWT (JSON Web Tokens)**.
- El token se almacena en `localStorage` tras un login exitoso.
- `src/lib/api.ts` intercepta cada petición e inyecta el header `Authorization: Bearer <token>`.
- `src/App.tsx` protege las rutas privadas redirigiendo al login si no hay token.

## 🎨 Diseño

El diseño sigue una paleta de colores personalizada definida en `tailwind.config.js`:
- `brand-blue`: Azul principal
- `brand-red`: Rojo de acción (Botones)
- `brand-teal`: Acentos

---
© 2026 DeskFlow Inc.
# helpdesk-front
