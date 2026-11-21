---
name: omniroute
description: "AI model proxy, dynamic routing, quota management, and token/cost optimization using OmniRoute."
---

# OmniRoute LLM Gateway & Token Optimizer Skill

This skill defines the operational standards for routing LLM requests, avoiding rate limits, managing multiple AI providers, and optimizing token consumption.

## Categoría: 🪙 Tokens, Gateway LLM & Optimización (Prioridad Operativa)

### Propósito
Gestionar un gateway unificado compatible con OpenAI para enrutar consultas de modelos, implementar balanceo de carga, reintentos automáticos y reducir el gasto innecesario de tokens.

---

## Directrices de Uso

### 1. Funcionalidades Clave
* **Punto de Enlace Unificado:** Enruta herramientas (Cursor, CLI agents, SDKs) a través de un único proxy local/remoto.
* **Smart Routing & Fallback:** Si un proveedor agota cuota o responde lento, conmuta automáticamente a un modelo de respaldo sin interrumpir el flujo.
* **Optimización de Tokens y Costes:** Compresión de prompts, caché de respuestas frecuentes y control de límites por petición.
* **Observabilidad y Auditoría:** Registro de consumo de tokens y métricas de latencia de cada modelo.

### 2. Flujo de Trabajo para el Asistente de IA
1. **Priorizar Rutas Eficientes:** Dirigir tareas sencillas (linting, formateo, resúmenes) a modelos ligeros/rápidos y reservar modelos avanzados para razonamiento complejo y arquitectura.
2. **Prevención de Errores de Cuota:** Monitorear respuestas de error de proveedores y activar conmutación inmediata a través de OmniRoute.
3. **Caché y Reuso:** Evitar reenviar contextos completos idénticos si no han existido cambios en el código.
