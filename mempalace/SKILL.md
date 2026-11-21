---
name: mempalace
description: "Long-term persistent memory, context retention across sessions, and semantic memory retrieval using MemPalace."
---

# MemPalace Long-Term Memory & Context Retention Skill

This skill defines the operational guidelines for storing, organizing, and retrieving persistent project knowledge, architectural decisions, and user preferences across conversation sessions using MemPalace.

## Categoría: 🪙 Tokens, Contexto & Memoria Persistente (Prioridad Operativa)

### Propósito
Mantener una memoria jerárquica a largo plazo basada en el "Método de Loci" (Palacio de la Memoria), almacenando información textual íntegra (verbatim) y recuperándola semánticamente con ChromaDB / SQLite para no olvidar decisiones previas ni desperdiciar tokens recontextualizando al agente.

---

## Estructura Jerárquica de la Memoria
* **Alas (Wings):** Proyectos principales o áreas de trabajo (ej. `php-apps`, `vercel-frontend`, `mobile-capacitor`).
* **Habitaciones (Rooms):** Módulos o temas específicos dentro del proyecto (ej. `auth`, `database-schema`, `stripe-billing`).
* **Pasillos (Halls):** Tipo de conocimiento (hechos técnicos, arquitectura, decisiones).
* **Cajones (Drawers):** Registros individuales de memoria comprimidos con dialecto AAAK (~30x reducción de tokens).

---

## Comandos Principales de la CLI
* **Inicializar en un proyecto:** `mempalace init .`
* **Indexar archivos/transcripciones:** `mempalace mine`
* **Recuperar contexto inicial ligero (L0+L1 ~600 tokens):** `mempalace wake-up`
* **Buscar conocimiento específico:** `mempalace search "consulta"`
* **Comprimir memorias:** `mempalace compress`
* **Servidor MCP para agentes:** `mempalace-mcp`

---

## Directrices para el Asistente
1. **Inicio de sesión (Wake-up):** Antes de tareas complejas en un proyecto recurrente, ejecutar `mempalace wake-up` para absorber el contexto previo sin saturar el historial.
2. **Persistencia tras decisiones:** Registrar elecciones clave de arquitectura y librerías en el palacio para sesiones futuras.
