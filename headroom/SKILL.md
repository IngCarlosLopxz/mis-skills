---
name: headroom
description: "Context optimization, prompt compression, and token reduction layer for AI agents and LLMs using Headroom."
---

# Headroom Token & Context Compression Skill

This skill defines the strategy and tools to compress chat history, tool logs, large JSON payloads, and code context before forwarding them to the LLM, reducing token consumption by up to 20%-90%.

## Categoría: 🪙 Tokens, Gateway LLM & Optimización (Prioridad Operativa)

### Propósito
Actuar como capa de optimización de contexto inteligente. Elimina redundancias estructurales en salidas de terminal, respuestas de herramientas y fragmentos de código sin perder información crítica como errores, excepciones o firmas de funciones.

---

## Directrices de Uso

### 1. Cuándo Aplicar Compresión
* **Salidas extensas de comandos y terminal:** Traces de build, logs de pruebas o salidas JSON repetitivas.
* **Historiales largos de conversación:** Conversaciones complejas con múltiples turnos antes de enviar al modelo.
* **Archivos masivos de código:** Reducción de ruido sintáctico conservando definiciones clave.

### 2. Uso en Scripts y Workflows
```python
from headroom import compress

# Optimiza mensajes manteniendo estructura idéntica
result = compress(messages, model="gpt-4o")
optimized_messages = result.messages
print(f"Tokens reducidos: {result.tokens_saved}")
```

### 3. Modo Proxy Local
Headroom puede levantarse como proxy local (`headroom proxy`) para interceptar y comprimir el tráfico de herramientas CLI y agentes locales, integrándose con OmniRoute.
