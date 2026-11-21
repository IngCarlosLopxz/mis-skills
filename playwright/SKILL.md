---
name: playwright
description: "End-to-End (E2E) browser testing, UI visual verification, and automated web app quality assurance using Playwright."
---

# Playwright Web Testing & UI Verification Skill

This skill defines the standard operating procedure for testing web applications, verifying UI designs, and ensuring frontend stability before deploying or committing changes.

## Categoría: 🎨 Diseño y Verificación de UI / Testing E2E

### Propósito
Garantizar que las interfaces (UI), formularios, flujos de usuario y rutas web de proyectos (Vercel, Node.js, PHP) funcionen sin errores visuales ni de lógica interactiva.

---

## Directrices de Uso

### 1. Inicialización en Nuevos Proyectos Web
Cuando un proyecto web requiera pruebas o validación de interfaz:
```bash
npx playwright install --with-deps
npm init playwright@latest
```

### 2. Flujo de Verificación Pre-Entrega
Antes de dar por completado un cambio en la interfaz o backend:
1. **Pruebas de Componentes y Páginas:** Ejecutar pruebas automáticas de navegación, renderizado y respuesta de APIs.
2. **Pruebas en Múltiples Viewports:** Validar diseño móvil (mobile viewports), tablet y desktop.
3. **Captura de Estados Visuales:** Usar screenshots o comparaciones visuales para asegurar que los estilos de diseño no sufran regresiones.

### 3. Comandos Esenciales
* Ejecutar tests: `npx playwright test`
* Modo UI interactivo: `npx playwright test --ui`
* Generar código de test navegando: `npx playwright codegen <url>`
* Ver reporte detallado: `npx playwright show-report`

### 4. Reglas para el Asistente de IA
* **Sin romper flujos existentes:** Toda nueva funcionalidad de interfaz debe incluir o pasar pruebas de Playwright para validar que los elementos clave (`data-testid`, roles accesibles, botones) respondan correctamente.
* **Integración con Graphify:** Verificar primero los módulos afectados en el grafo antes de escribir los casos de prueba de Playwright.
