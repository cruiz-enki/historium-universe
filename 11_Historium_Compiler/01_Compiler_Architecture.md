# HISTORIUM — COMPILER ARCHITECTURE

**Versión:** 1.0  
**Estado:** Oficial

---

# Arquitectura completa

```text
Blueprint Loader
↓
Entity Loader
↓
Relationship Loader
↓
Context Assembler
↓
Prompt Compiler
↓
LLM Gateway
↓
Output Validator
↓
Markdown Generator
↓
GitHub Publisher
↓
Supabase Publisher
```

---

# Blueprint Loader

Carga la intención de producción.

Puede ser campaña, capítulo, nodo, entidad, prompt visual o lote.

Define el objetivo antes de tocar la IA.

---

# Entity Loader

Busca entidades existentes.

Consulta `03_Knowledge/` y `REGISTRY.yaml`.

Evita duplicados.

---

# Relationship Loader

Consulta `RELATIONSHIP_TYPES.md`.

Carga relaciones existentes y tipos permitidos.

No permite relaciones libres.

---

# Context Assembler

Selecciona contexto exacto.

No envía todo el repositorio.

Arma paquetes por tarea.

---

# Prompt Compiler

Convierte contexto en prompt final.

Incluye reglas, contrato de output, checklist y prohibiciones.

---

# LLM Gateway

Elige modelo según tarea.

Narrativa premium no usa el mismo modelo que validación YAML.

---

# Output Validator

Revisa IDs, frontmatter, tono, Markdown, relaciones, Museo e importabilidad.

---

# Markdown Generator

Convierte salida aprobada en Markdown canónico.

Debe producir archivos estables y legibles.

---

# GitHub Publisher

Crea rama, commit, PR y trazabilidad editorial.

---

# Supabase Publisher

Importa contenido validado al estado activo.

No decide Canon.

Ejecuta Canon.
